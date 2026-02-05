# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added
- Initial repository setup
- Example skill template showing Agent Skills standard structure
- UX/UI Evaluation Suite with five professional skills:
  - Don Norman Principles Audit - Human-centered design evaluation
  - Nielsen Heuristics Audit - Comprehensive usability evaluation
  - WCAG Accessibility Audit - Legal compliance and accessibility testing
  - Cognitive Walkthrough - Task-specific deep-dive analysis for learnability
  - UI Design Review - Visual design and aesthetics evaluation

### Documentation
- README with installation instructions and skill descriptions
- LICENSE (MIT)
- CONTRIBUTING guide with Conventional Commits standard
- CHANGELOG following Keep a Changelog format
- CLAUDE.md with repository architecture guidance

## [1.0.0] - 2026-02-05

### Added
- Initial release of @mastepanoski/claude-skills
- Agent Skills standard-compliant repository structure
- Three production-ready UX evaluation skills
- Complete documentation and contribution guidelines

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

[Unreleased]: https://github.com/mastepanoski/claude-skills/compare/v1.0.0...HEAD
[1.0.0]: https://github.com/mastepanoski/claude-skills/releases/tag/v1.0.0
