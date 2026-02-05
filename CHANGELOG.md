# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [1.1.0] - 2026-02-05

### Added
- **Cognitive Walkthrough skill** - Task-specific deep-dive usability evaluation
  - Simulates novice user cognition step-by-step
  - 4 cognitive questions per action (goal clarity, discoverability, association, feedback)
  - Failure point identification and success probability estimation
  - Cognitive load assessment with actionable recommendations
- **UI Design Review skill** - Comprehensive visual design and aesthetics evaluation
  - 10 design dimensions: hierarchy, typography, color, spacing, consistency, imagery, layout, components, branding, modern standards
  - Component audit checklist and design system assessment
  - Competitive comparison and first impression analysis
  - Design quality scoring (0-100) and trend analysis (2026)

### Documentation
- Added CLAUDE.md with repository architecture and development guidelines
- Updated README with new skills
- Updated CONTRIBUTING with complete workflow examples

## [1.0.0] - 2026-02-05

### Added
- Initial release of @mastepanoski/claude-skills
- Agent Skills standard-compliant repository structure
- Example skill template showing Agent Skills standard structure
- UX/UI Evaluation Suite with three professional skills:
  - Don Norman Principles Audit - Human-centered design evaluation (7 principles)
  - Nielsen Heuristics Audit - Comprehensive usability evaluation (10 heuristics)
  - WCAG Accessibility Audit - Legal compliance and accessibility testing (WCAG 2.1/2.2)
- Complete documentation:
  - README with installation instructions and skill descriptions
  - LICENSE (MIT)
  - CONTRIBUTING guide with Conventional Commits standard
  - CHANGELOG following Keep a Changelog format
- GitHub templates:
  - Issue templates (bug report, feature request)
  - Pull request template

---

## Release Types

### Major (X.0.0)
Breaking changes, major new features, significant restructuring

### Minor (0.X.0)
New skills, new features, backwards-compatible improvements

### Patch (0.0.X)
Bug fixes, documentation updates, minor improvements

---

## Commit Convention

This project uses [Conventional Commits](https://www.conventionalcommits.org/):

- `feat:` New features or skills
- `fix:` Bug fixes
- `docs:` Documentation changes
- `style:` Code style/formatting (no functional changes)
- `refactor:` Code refactoring
- `test:` Adding or updating tests
- `chore:` Maintenance tasks, dependencies

Example:
```
feat(wcag-audit): add WCAG 2.2 new success criteria
fix(nielsen): correct severity rating in example
docs(readme): update installation instructions
```

[Unreleased]: https://github.com/mastepanoski/claude-skills/compare/v1.1.0...HEAD
[1.1.0]: https://github.com/mastepanoski/claude-skills/compare/v1.0.0...v1.1.0
[1.0.0]: https://github.com/mastepanoski/claude-skills/releases/tag/v1.0.0
