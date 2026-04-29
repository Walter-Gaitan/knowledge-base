# LMS QA Knowledge Base

Centralized documentation for the Blackboard QA team — processes, checklists, settings, and automation.

## Structure

```
docs/
├── getting-started/    ← Onboarding guide & QA protocols
├── tqa/                ← Teacher QA (Phase 1)
├── sqa/                ← Student QA (Phase 2)
├── psqa/               ← Post-Sync QA (Phase 3)
├── reference/          ← Settings, edge cases, quirks, reporting format
└── automation/         ← Playwright test suite setup & reference
```

## Quick Links

- **New to the team?** Start with [QA Onboarding Guide](docs/getting-started/onboarding-guide.md)
- **Running a TQA?** Open the [TQA Checklist](docs/tqa/checklist.md)
- **Running an SQA?** Open the [SQA Checklist](docs/sqa/checklist.md)
- **Running a PSQA?** Open the [PSQA Checklist](docs/psqa/checklist.md)
- **Need settings?** See [Course Settings](docs/reference/course-settings.md)

## Contributing

1. Clone the repository
2. Add or edit markdown files in the appropriate `docs/` subfolder
3. Add Just-the-Docs front matter (`title`, `parent`, `nav_order`) to new pages
4. Commit and push your changes

## License

This project is licensed under the MIT License.