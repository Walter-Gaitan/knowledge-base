# Automation Setup Guide

This guide walks you through setting up and running the Playwright-based Blackboard QA automation suite.

---

## Prerequisites

| Tool | Version | Purpose |
|------|---------|---------|
| **Node.js** | 18+ | JavaScript runtime |
| **npm** | 9+ | Package manager (bundled with Node) |
| **Playwright** | 1.57+ | Browser automation framework |

---

## Installation

```bash
# 1. Clone the repository
git clone https://github.com/Walter-Gaitan/Blackboard-testing-with-antigravity.git
cd Blackboard-testing-with-antigravity

# 2. Install dependencies
npm install

# 3. Install Playwright browsers
npx playwright install chromium
```

---

## Environment Configuration

Copy `.env.example` to `.env` and fill in your credentials:

```bash
cp .env.example .env
```

### Environment Variables

| Variable | Required | Description | Example |
|----------|----------|-------------|---------|
| `BASE_URL` | Yes | Blackboard base URL | `https://learn.pacificcollege.edu/ultra/admin` |
| `COURSE_URL` | Yes | Full URL to the course outline you want to verify | `https://learn.pacificcollege.edu/ultra/courses/_15238_1/outline` |
| `BLACKBOARD_USERNAME` | Yes | Your Blackboard / Microsoft login email | `studentqa@pacificcollege.edu` |
| `BLACKBOARD_PASSWORD` | Yes | Your Blackboard password | *(keep secret)* |
| `HEADLESS` | No | Run browser invisibly (`True`) or visibly (`False`) | `False` |
| `SLOW_MO` | No | Delay between actions in ms (default: `1000`) | `1000` |

> [!CAUTION]
> Never commit your `.env` file. It is already listed in `.gitignore`.

---

## Running Tests

### npm Scripts (Recommended)

```bash
# Run the full course audit (login + module verification)
npm run audit

# Run login only (saves session to state.json)
npm run login

# Quick health check (requires existing session)
npm run pulse

# Smart check: pulse first, falls back to full audit if pulse fails
npm run check
```

### Direct Playwright Commands

```bash
# Run a specific test file
npx playwright test tests/02_blackboard_audit.spec.ts

# Run with list reporter for cleaner output
npx playwright test tests/02_blackboard_audit.spec.ts --reporter=list

# Run headed (visible browser) — already default in config
npx playwright test tests/02_blackboard_audit.spec.ts --headed
```

---

## Configuration Reference

The Playwright configuration lives in `playwright.config.ts`. Key settings:

| Setting | Value | Notes |
|---------|-------|-------|
| `fullyParallel` | `false` | Tests run sequentially (required for login flow) |
| `workers` | `1` | Single browser instance |
| `headless` | `false` | Browser is visible by default |
| `actionTimeout` | `15s` | Fail fast if element not found |
| `navigationTimeout` | `30s` | Page load timeout |
| `slowMo` | `1000ms` | Delay between actions for visibility |
| `trace` | `retain-on-failure` | Saves traces when tests fail |

---

## Troubleshooting

### "Login verification failed: Success markers not found"
- **Cause**: Microsoft login flow changed, or credentials are wrong.
- **Fix**: Verify your `.env` credentials. Run `npm run login` in headed mode to watch the flow and identify where it stalls.

### "Session Expired" on pulse or legacy tests
- **Cause**: `state.json` contains an expired session cookie.
- **Fix**: Run `npm run audit` (which logs in fresh) or `npm run login` to refresh the session.

### Microsoft "Pick an Account" or MFA prompts
- **Cause**: Multiple Microsoft accounts cached in the browser profile.
- **Fix**: The login flow handles "Pick an account" automatically. If MFA is required, you must complete it manually while the browser is visible (`HEADLESS=False`).

### Modules 7+ fail with timeout
- **Cause**: Blackboard lazy-loads module content. The timeout may still be too short on slow connections.
- **Fix**: The audit test uses a 10-second scroll timeout. If issues persist, increase the timeout in `02_blackboard_audit.spec.ts` at the `scrollIntoViewIfNeeded({ timeout: 10000 })` call.

### Test report
After any test run, an HTML report is generated in `playwright-report/`. Open it with:
```bash
npx playwright show-report
```
