# Test Reference

A complete reference for every test file in the suite, what it does, and when to use it.

---

## Architecture Overview

The test suite uses two authentication strategies:

| Strategy | Used By | How It Works |
|----------|---------|--------------|
| **Login-integrated** | `02_blackboard_audit.spec.ts` | Performs Microsoft login inline, then runs the audit in the same browser context. Most reliable. |
| **Storage-state** | `03_pulse.spec.ts`, `tests/qa/*` | Reads session cookies from `state.json`. Requires a prior login run. Faster but can expire. |

> [!TIP]
> The login-integrated approach (`npm run audit`) is the recommended default. Use the storage-state tests only when you need a quick check and already have a fresh session.

---

## Primary Tests (`tests/`)

### `01_login.spec.ts` — Standalone Login

| | |
|---|---|
| **Script** | `npm run login` |
| **Purpose** | Log in via Microsoft SAML and save cookies to `state.json` |
| **When to use** | Debugging auth issues, or refreshing the session for storage-state tests |

**Flow**:

1. Navigate to `/ultra/stream`
2. Detect if already logged in (profile link or URL check)
3. Click SAML login → handle Microsoft "Pick an account" or email entry
4. Enter password → handle "Stay signed in?" and "More info" prompts
5. Verify landing on the Blackboard dashboard
6. Save session cookies to `state.json`

---

### `02_blackboard_audit.spec.ts` — Full Course Audit ⭐

| | |
|---|---|
| **Script** | `npm run audit` |
| **Purpose** | Log in, navigate to the course, and verify all 18 required modules are visible |
| **When to use** | Primary test — run this for a full course verification |

**Flow**:

1. **Login Phase** — Same flow as `01_login.spec.ts`, but inline (no separate step needed)
2. **Navigate to Course** — Goes to `COURSE_URL` from `.env`
3. **Verify Modules** — Checks visibility of all 18 expected modules:
    - `Start Here`
    - `Student Resources`
    - `Start Course Orientation`
    - `Module 1` through `Module 15`

Each module is scrolled into view with a **10-second timeout** to accommodate Blackboard's lazy loading. Results are summarized at the end with ✅/❌ indicators.

---

### `03_pulse.spec.ts` — Quick Health Check

| | |
|---|---|
| **Script** | `npm run pulse` |
| **Purpose** | 20-second check that the session is alive and the course loads |
| **When to use** | Quick daily check before running the full audit |

**Flow**:

1. Navigate to `COURSE_URL`
2. Check if redirected to a login page → fail if session expired
3. Look for the "Start Here" module → pass if visible

> [!NOTE]
> This test requires an existing `state.json` session. Run `npm run login` or `npm run audit` first.

---

## Legacy / WIP Tests (`tests/qa/`)

These are earlier versions of the test specs, kept for reference. They all use `state.json` for authentication.

| File | Purpose | Status |
|------|---------|--------|
| `sanity.spec.ts` | Minimal no-op test to confirm Playwright works | ✅ Utility |
| `start_here.spec.ts` | Verify "Start Here" module visibility and contents | 🔄 Superseded by `02_blackboard_audit` |
| `unified_audit.spec.ts` | Earlier audit that checks Start Here + Student Resources | 🔄 Superseded by `02_blackboard_audit` |

---

## npm Scripts Reference

| Script | Command | Description |
|--------|---------|-------------|
| `npm run login` | `npx playwright test tests/01_login.spec.ts` | Login only, save session |
| `npm run audit` | `npx playwright test tests/02_blackboard_audit.spec.ts` | Full login + module audit |
| `npm run pulse` | `npx playwright test tests/03_pulse.spec.ts` | Quick session/course check |
| `npm run check` | `npm run pulse \|\| npm run audit` | Pulse first; if it fails, run full audit |
