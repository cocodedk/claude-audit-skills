# Contributing to @mastepanoski/claude-skills

Thank you for your interest in contributing! This guide will help you get started.

## 📋 Table of Contents

- [Code of Conduct](#code-of-conduct)
- [How Can I Contribute?](#how-can-i-contribute)
- [Commit Convention](#commit-convention)
- [Skill Development Guidelines](#skill-development-guidelines)
- [Pull Request Process](#pull-request-process)
- [Testing Your Skills](#testing-your-skills)

## 🤝 Code of Conduct

### Our Pledge

We are committed to providing a welcoming and inclusive environment for all contributors, regardless of experience level, background, or identity.

### Expected Behavior

- Be respectful and considerate
- Provide constructive feedback
- Focus on what's best for the community
- Show empathy towards others

### Unacceptable Behavior

- Harassment, discrimination, or offensive comments
- Trolling or insulting remarks
- Publishing others' private information
- Any conduct harmful to the community

## 🚀 How Can I Contribute?

### Reporting Bugs

If you find a bug in a skill:

1. **Check existing issues** to avoid duplicates
2. **Open a new issue** with:
   - Clear, descriptive title
   - Steps to reproduce
   - Expected vs. actual behavior
   - Environment details (AI agent, version, platform)
   - Screenshots or examples (if applicable)

**Template:**
```markdown
**Skill**: [skill-name]
**Agent**: Claude Code / Codex / ChatGPT
**Version**: [version]

**Description**:
[Clear description of the issue]

**Steps to Reproduce**:
1. [First step]
2. [Second step]
3. [...]

**Expected Behavior**:
[What should happen]

**Actual Behavior**:
[What actually happens]

**Screenshots/Examples**:
[If applicable]
```

### Suggesting Enhancements

Have an idea for a new skill or improvement?

1. **Open an issue** with:
   - Clear description of the enhancement
   - Use cases and benefits
   - Proposed implementation (if applicable)
2. **Label it** as `enhancement`
3. **Discuss** with maintainers before starting work

### Contributing New Skills

Want to add a new skill? Great! Follow these steps:

1. **Open an issue** first to discuss the skill idea
2. **Fork the repository**
3. **Create a branch**: `git checkout -b feat/new-skill-name`
4. **Develop your skill** (see [Skill Development Guidelines](#skill-development-guidelines))
5. **Test thoroughly** (see [Testing Your Skills](#testing-your-skills))
6. **Submit a Pull Request** (see [Pull Request Process](#pull-request-process))

### Improving Documentation

Documentation improvements are always welcome:

- Fix typos or unclear instructions
- Add examples or use cases
- Translate documentation
- Improve README or skill descriptions

## 📝 Commit Convention

This project follows [Conventional Commits](https://www.conventionalcommits.org/) specification.

### Commit Message Format

```
<type>(<scope>): <subject>

<body>

<footer>
```

### Types

| Type | Description | Example |
|------|-------------|---------|
| `feat` | New feature or skill | `feat(wcag): add color contrast checker` |
| `fix` | Bug fix | `fix(nielsen): correct severity rating logic` |
| `docs` | Documentation only | `docs(readme): update installation steps` |
| `style` | Code style/formatting (no logic changes) | `style(don-norman): fix markdown formatting` |
| `refactor` | Code refactoring (no feature/bug changes) | `refactor(wcag): simplify report structure` |
| `test` | Adding or updating tests | `test(nielsen): add validation tests` |
| `chore` | Maintenance, dependencies, tooling | `chore: update package.json version` |
| `perf` | Performance improvements | `perf(wcag): optimize automated testing` |

### Scope

The scope is optional but recommended. Use the skill name or affected area:

- `feat(wcag-audit): ...`
- `fix(nielsen-heuristics): ...`
- `docs(contributing): ...`
- `chore(deps): ...`

### Subject

- Use imperative, present tense: "add" not "added" nor "adds"
- Don't capitalize first letter
- No period (.) at the end
- Keep it concise (50 characters or less)

### Body (Optional)

- Explain **what** and **why**, not **how**
- Wrap at 72 characters
- Separate from subject with blank line

### Footer (Optional)

- Reference issues: `Closes #123`, `Fixes #456`
- Breaking changes: `BREAKING CHANGE: description`

### Examples

#### Good Commits

```bash
feat(cognitive-walkthrough): add new skill for task-specific evaluation

Add comprehensive cognitive walkthrough skill that guides users through
step-by-step task analysis, identifying potential usability issues.

Closes #15
```

```bash
fix(wcag-audit): correct contrast ratio calculation

The previous implementation didn't account for alpha transparency.
Updated to use WCAG 2.1 relative luminance formula.
```

```bash
docs(readme): add usage examples for UX suite

Added practical examples showing how to combine Don Norman,
Nielsen, and WCAG audits for comprehensive evaluation.
```

```bash
chore: update dependencies to latest versions
```

#### Bad Commits

```bash
# ❌ Too vague
fix: bug fixes

# ❌ Not imperative
feat: added new skill

# ❌ Too long subject
feat(wcag): add comprehensive WCAG 2.2 accessibility audit with all success criteria and automated testing

# ❌ No scope when relevant
feat: accessibility audit

# ✅ Better
feat(wcag-audit): add WCAG 2.2 accessibility audit
```

### Commit Tools

To help enforce commit conventions, you can use:

```bash
# Install commitizen globally
npm install -g commitizen cz-conventional-changelog

# Use interactive commit
git cz
```

Or add to your `.git/hooks/commit-msg`:

```bash
#!/bin/bash
# Simple commit message validation
commit_msg=$(cat "$1")
pattern="^(feat|fix|docs|style|refactor|test|chore|perf)(\([a-z-]+\))?: .{1,50}"

if ! echo "$commit_msg" | grep -qE "$pattern"; then
  echo "❌ Invalid commit message format!"
  echo "Use: <type>(<scope>): <subject>"
  echo "Example: feat(wcag-audit): add contrast checker"
  exit 1
fi
```

## 🏗️ Skill Development Guidelines

### Skill Structure

Every skill must follow the Agent Skills standard:

```
skills/
└── your-skill-name/
    ├── SKILL.md          # REQUIRED: Core skill definition
    ├── README.md         # OPTIONAL: Additional documentation
    ├── scripts/          # OPTIONAL: Helper scripts
    │   ├── helper.sh
    │   └── validator.py
    ├── references/       # OPTIONAL: Reference documentation
    │   └── guide.md
    └── assets/           # OPTIONAL: Templates, examples
        └── template.json
```

### SKILL.md Format

**REQUIRED structure:**

```markdown
---
name: your-skill-name
description: Brief description (max 200 chars) - AI uses this to determine when to invoke
---

# Your Skill Title

Clear explanation of what this skill does and when to use it.

## When to Use This Skill

Bullet points of scenarios when this skill should be invoked.

## Inputs Required

List of inputs the AI agent needs to execute this skill:
- **input_name**: Description [REQUIRED/OPTIONAL]

## Procedure

Step-by-step instructions the AI agent will follow:

### Step 1: [Title]
1. [Action]
2. [Action]

### Step 2: [Title]
[Continue...]

## Output Format

Description or example of expected output.

## Best Practices

Tips for effective use of this skill.

## Version

1.0 - Initial release
```

### Skill Naming Conventions

- Use **kebab-case**: `nielsen-heuristics-audit`
- Be **descriptive**: Clear purpose from name
- Keep it **concise**: 2-4 words typically
- Avoid **redundancy**: Don't repeat "skill" in name

**Good:**
- ✅ `wcag-accessibility-audit`
- ✅ `cognitive-walkthrough`
- ✅ `design-system-review`

**Bad:**
- ❌ `audit` (too vague)
- ❌ `wcag_accessibility` (use kebab-case)
- ❌ `TheWCAGAccessibilityAuditSkill` (PascalCase, redundant)

### Skill Quality Checklist

Before submitting, ensure your skill:

- [ ] Has clear, actionable YAML frontmatter (name + description)
- [ ] Description is under 200 characters
- [ ] Instructions are step-by-step and unambiguous
- [ ] Includes "When to Use This Skill" section
- [ ] Specifies required/optional inputs
- [ ] Defines expected output format
- [ ] Uses proper Markdown formatting
- [ ] Has no spelling or grammar errors
- [ ] Works with multiple AI agents (Claude, Codex, ChatGPT)
- [ ] Is tested locally before submission
- [ ] Includes examples or use cases
- [ ] Credits sources/standards if applicable

### Writing Style

- **Be concise**: Clear, actionable instructions
- **Use active voice**: "Analyze the interface" not "The interface should be analyzed"
- **Use imperative mood**: Commands, not descriptions
- **Be specific**: "Check color contrast is 4.5:1" not "Ensure good contrast"
- **Include examples**: Show, don't just tell
- **Use formatting**: Bold, lists, code blocks for clarity

## 🔄 Pull Request Process

### Before Submitting

1. **Test locally**:
   ```bash
   npx skills add . --skill your-skill-name
   ```

2. **Validate SKILL.md**:
   - YAML frontmatter parses correctly
   - Description under 200 characters
   - No broken markdown

3. **Update documentation**:
   - Add skill to README.md skills table
   - Update CHANGELOG.md with your changes
   - Add any new dependencies to package.json

4. **Commit with convention**:
   ```bash
   git add .
   git commit -m "feat(your-skill): add comprehensive description"
   ```

### Submitting Pull Request

1. **Push to your fork**:
   ```bash
   git push origin feat/your-skill-name
   ```

2. **Create Pull Request** with:
   - **Clear title** following commit convention:
     - `feat(skill-name): add new skill for X`
     - `fix(skill-name): correct Y issue`
     - `docs: update contributing guide`

   - **Description** including:
     ```markdown
     ## Changes
     - [List of changes]

     ## Motivation
     [Why this change is needed]

     ## Testing
     [How you tested this]

     ## Screenshots/Examples
     [If applicable]

     Closes #[issue-number]
     ```

3. **Link related issues**: Use `Closes #123` or `Fixes #456`

4. **Request review**: Assign maintainers for review

### PR Review Process

Maintainers will:

1. **Review code/documentation** for quality and standards
2. **Test the skill** with multiple AI agents if applicable
3. **Request changes** if needed
4. **Approve and merge** when ready

### After Merge

- Your contribution will be added to CHANGELOG
- You'll be credited in release notes
- Skill becomes available via `npx skills add`

## 🧪 Testing Your Skills

### Local Testing

```bash
# From repository root
npx skills add . --skill your-skill-name

# Test with Claude Code CLI
claude "Use [your-skill-name] to evaluate [something]"
```

### Manual Testing Checklist

Test your skill with:

- [ ] **Claude Code** - Primary target
- [ ] **OpenAI Codex** - If accessible
- [ ] **ChatGPT** - For broader compatibility
- [ ] **Different inputs** - Edge cases, minimal/maximal inputs
- [ ] **Different scenarios** - Various use cases from "When to Use"

### Common Issues

| Issue | Solution |
|-------|----------|
| Skill not invoked | Description too vague or over 200 chars |
| Unclear instructions | Add more specific step-by-step guidance |
| Inconsistent output | Define clearer output format/structure |
| Agent confused | Simplify language, add examples |

## 📚 Additional Resources

### Agent Skills Standard
- [Anthropic Skills Repository](https://github.com/anthropics/skills)
- [Claude Code Skills Docs](https://code.claude.com/docs/en/skills)
- [Agent Skills Specification](https://github.com/anthropics/skills/blob/main/SPECIFICATION.md)

### Standards Referenced in Skills
- [WCAG 2.2 Guidelines](https://www.w3.org/WAI/WCAG22/quickref/)
- [Nielsen's 10 Usability Heuristics](https://www.nngroup.com/articles/ten-usability-heuristics/)
- [Don Norman - The Design of Everyday Things](https://www.nngroup.com/books/design-everyday-things-revised/)

### Commit Conventions
- [Conventional Commits](https://www.conventionalcommits.org/)
- [Keep a Changelog](https://keepachangelog.com/)
- [Semantic Versioning](https://semver.org/)

## ❓ Questions?

- **Issues**: Open an issue for bugs or questions
- **Discussions**: Use GitHub Discussions for general questions
- **Email**: [Your contact if you want to provide one]

## 🎉 Recognition

Contributors will be recognized in:
- README Contributors section
- Release notes
- CHANGELOG entries

Thank you for contributing to @mastepanoski/claude-skills! 🙌

---

**Last Updated**: 2026-02-05
**Maintainer**: [@mastepanoski](https://github.com/mastepanoski)
