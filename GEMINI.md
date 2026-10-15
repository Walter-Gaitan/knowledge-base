# Gemini Instructions: LMS QA Knowledge Base

This file provides context, rules, and guidelines for AI agents (including Gemini and Antigravity) working on the LMS QA Knowledge Base repository.

---

## 1. Project Overview

The **LMS QA Knowledge Base** is a centralized documentation site built for the Blackboard QA team. It documents processes, checklists, settings, edge cases, program-specific quirks, and automated test suites across all QA phases.

- **Site Generator:** Jekyll with the [Just the Docs](https://just-the-docs.github.io/just-the-docs/) theme (`just-the-docs/just-the-docs`).
- **Hosting / Deployment:** GitHub Pages (`gh-pages`).
- **Primary Audience:** QA Engineers, Instructional Designers, Course Reviewers, and automation contributors.

---

## 2. Directory Structure & Key Sections

```text
knowledge-base/
├── _config.yml               # Jekyll & Just-the-Docs site configuration
├── index.md                  # Landing page (redirects/links to docs/index.md)
├── README.md                 # Repository readme and quick links
├── GEMINI.md                 # Agent instructions and repository context
├── docs/
│   ├── index.md              # Documentation home
│   ├── getting-started/      # Onboarding guide, QA workflows & protocols
│   ├── tqa/                  # Teacher QA (Phase 1): checklists, advice, form mapping
│   ├── sqa/                  # Student QA (Phase 2): checklists, advice, review criteria
│   ├── psqa/                 # Post-Sync QA (Phase 3): checklists, form mapping
│   ├── reference/            # Course settings, edge cases, quirks, reporting formats, copilot prompt
│   └── automation/           # Playwright test suite setup, test reference, automation guides
```

---

## 3. Documentation Conventions

When creating or modifying markdown pages in `docs/`:

1. **Front Matter Required:**
   Every documentation page under `docs/` must start with YAML front matter adhering to `just-the-docs`:
   ```yaml
   ---
   title: Page Title
   parent: Parent Section Title (e.g., TQA, SQA, Reference)
   nav_order: 1
   ---
   ```
   For parent section indexes, include:
   ```yaml
   ---
   title: Section Title
   has_children: true
   nav_order: 2
   ---
   ```

2. **Checklist Formatting:**
   - Standardize checklist items with markdown tasks: `- [ ] **Item Number. Title** — Description and verification criteria.`
   - Keep item numbering sequential and aligned with form mapping documents where applicable.

3. **Tables and Cross-References:**
   - Use clean GitHub-flavored markdown tables for settings, form mappings, and quirks.
   - Use relative markdown links (`[text](../folder/file.md)`) for internal cross-referencing.

---

## 4. Key Domain Rules & Program Quirks

Keep these domain-specific QA rules in mind when updating checklists or documentation:

- **Grading Schemas:** "Pacific College Letter" (also known as "PCHS Letter Grade") has specific parameters:
  - A: 93.5–100%
  - A-: 89.5–93.5%
  - B+: 86.5–89.5%
  - B: 83.5–86.5%
  - B-: 79.5–83.5%
  - C+: 76.5–79.5%
  - C: 69.5–76.5%
  - F: 0–69.5%
- **Gradebook Order:**
  `Final Grade` → `Overall Grade` → `COA` → `Module activities in sequential order`.
- **ATI Resources:**
  - ATI resource links are exempt from the general "no raw links" rule.
  - ATI activities are hosted on the vendor platform; grades are manually entered into Blackboard by the instructor.
- **Due Date Conventions:**
  - Module schedules must properly account for skipped or holiday weeks.
  - Discussion board deadlines frequently require initial posts and response replies before specific meeting or end-of-module milestones.

---

## 5. Git Commit & Contribution Guidelines

- **Commit Style:** Use Conventional Commits with lowercase type prefixes:
  - `docs: update TQA and PSQA grading schema terminology`
  - `feat: add new course setting reference for program X`
  - `fix: correct module due date formula in checklist`
- **Clean Workspace:** Never commit OS artifacts like `.DS_Store` or Jekyll build artifacts (`_site`, `.sass-cache`, `.jekyll-cache`).
