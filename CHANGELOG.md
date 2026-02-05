# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added
- **ISO 42001 AI Governance skill** - Responsible AI development and deployment audit
  - Based on ISO/IEC 42001:2023 international standard for AI Management Systems (AIMS)
  - Comprehensive governance framework: 10 key clauses covering full AI lifecycle
  - Risk management: Technical, ethical, legal, operational, and reputational risks
  - Regulatory alignment: EU AI Act, GDPR, NIST AI RMF, sector-specific regulations
  - AI lifecycle management: Design → Development → Validation → Deployment → Monitoring → Maintenance → Decommissioning
  - Ethical AI principles: Fairness, transparency, accountability, privacy, human oversight
  - Documentation requirements: Model cards, risk assessments, audit trails, incident reports
  - Compliance roadmap with phased implementation
  - Suitable for AI integrations, ML systems, and automated decision-making tools

## [1.2.0] - 2026-02-05

### Added
- **UX Audit and Rethink skill** ⭐ Marked as "START HERE" for holistic evaluation
  - Based on IxDF "The Basics of User Experience Design" methodology
  - Triple framework approach:
    * 7 UX Factors (Peter Morville's Honeycomb): Useful, Usable, Findable, Credible, Desirable, Accessible, Valuable
    * 5 Usability Characteristics (ISO 9241-11): Effectiveness, Efficiency, Engagement, Error Tolerance, Ease of Learning
    * 5 Interaction Design Dimensions: Words, Visual Representations, Physical Objects/Space, Time, Behavior
  - Comprehensive 0-100 scoring system with A-F grading
  - Mobile-specific guidelines (IxDF Chapter 8)
  - Design Thinking integration (Empathize, Define, Ideate, Prototype, Test)
  - UX research technique recommendations (user interviews, card sorting, usability testing, etc.)
  - Strategic redesign proposals with ROI estimates
  - Phase-based implementation roadmap
  - Complete executive audit report template
  - Evidence-based prioritization matrix

### Changed
- Reorganized README with "START HERE" indicator for new users
- Updated evaluation methodology workflow recommendations

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

[Unreleased]: https://github.com/mastepanoski/claude-skills/compare/v1.2.0...HEAD
[1.2.0]: https://github.com/mastepanoski/claude-skills/compare/v1.1.0...v1.2.0
[1.1.0]: https://github.com/mastepanoski/claude-skills/compare/v1.0.0...v1.1.0
[1.0.0]: https://github.com/mastepanoski/claude-skills/releases/tag/v1.0.0
