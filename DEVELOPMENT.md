# Development Guide

This guide is for developers who want to contribute new skills or modify existing ones.

## 📋 Table of Contents

- [Architecture Overview](#architecture-overview)
- [Setting Up Development Environment](#setting-up-development-environment)
- [Creating a New Skill](#creating-a-new-skill)
- [Testing Skills Locally](#testing-skills-locally)
- [Skill Structure Reference](#skill-structure-reference)
- [SKILL.md Anatomy](#skillmd-anatomy)
- [Commit Convention](#commit-convention)
- [Quality Standards Checklist](#quality-standards-checklist)
- [Publishing Workflow](#publishing-workflow)

## 🏗️ Architecture Overview

This repository follows the **Agent Skills open standard** (December 2025) adopted by Anthropic, OpenAI, and others. The standard ensures skills are portable across different AI coding assistants.

### Repository Structure

```
skills/                    # All skills live here
├── skill-name/           # Each skill is a directory (kebab-case)
│   ├── SKILL.md          # REQUIRED: YAML frontmatter + markdown instructions
│   ├── scripts/          # OPTIONAL: Executable helpers (.sh, .py, .js)
│   ├── references/       # OPTIONAL: Reference documentation
│   └── assets/           # OPTIONAL: Templates, examples, data files
```

### How Skills Work

1. **Installation**: User runs `npx skills add mastepanoski/claude-skills --skill skill-name`
2. **Registration**: The AI assistant indexes the skill's YAML frontmatter
3. **Detection**: When user requests match the skill's `description`, AI invokes it
4. **Execution**: AI reads `SKILL.md` and follows the instructions
5. **Output**: AI delivers structured results based on the skill's procedure

## 🛠️ Setting Up Development Environment

### Prerequisites

- Node.js 18+ (for testing with `npx`)
- Git
- Text editor with YAML/Markdown support

### Clone and Setup

```bash
# Clone repository
git clone https://github.com/mastepanoski/claude-skills.git
cd claude-skills

# Install dependencies (if any)
npm install

# Verify structure
tree skills/
```

### Configure Git Hooks (Optional)

```bash
# Enable commit-msg validation for Conventional Commits
# (Add if we implement pre-commit hooks in future)
```

## 🆕 Creating a New Skill

### Step 1: Create Directory Structure

```bash
# Use kebab-case for skill names
mkdir -p skills/your-skill-name
cd skills/your-skill-name
```

### Step 2: Create SKILL.md

Use this template:

```markdown
---
name: your-skill-name
description: Brief description of what this skill does (MAX 200 characters)
---

# Your Skill Title

## When to Use This Skill

Describe scenarios where this skill should be invoked:
- Scenario 1
- Scenario 2
- Scenario 3

## Inputs Required

**Required:**
- `input_name`: Description of required input

**Optional:**
- `optional_input`: Description of optional input (default: value)

## Procedure

Step-by-step instructions the AI agent will execute:

### Step 1: Preparation
1. Action 1
2. Action 2

### Step 2: Analysis
1. Action 1
2. Action 2

### Step 3: Reporting
1. Action 1
2. Action 2

## Output Format

Describe the expected output structure:

\```markdown
# Report Title

## Section 1
Content format...

## Section 2
Content format...
\```

## References

- [Resource 1](https://example.com)
- [Resource 2](https://example.com)

## Examples

### Example 1: Basic Usage
\```
Input: ...
Output: ...
\```

### Example 2: Advanced Usage
\```
Input: ...
Output: ...
\```
```

### Step 3: Add Optional Resources

```bash
# Add executable scripts (if needed)
mkdir scripts
touch scripts/helper.sh
chmod +x scripts/helper.sh

# Add reference documentation
mkdir references
touch references/methodology.md

# Add templates or data
mkdir assets
touch assets/template.json
```

### Step 4: Update README.md

Add your skill to the appropriate section:

```markdown
| `your-skill-name` | Brief description of the skill |
```

### Step 5: Update CHANGELOG.md

Add entry under `[Unreleased]`:

```markdown
## [Unreleased]

### Added
- **your-skill-name**: New skill for X evaluation following Y methodology
```

## 🧪 Testing Skills Locally

### Test Single Skill

```bash
# From repository root
npx skills add . --skill your-skill-name

# Verify installation
npx skills list | grep your-skill-name
```

### Test with AI Assistant

1. Install the skill locally
2. Open your AI assistant (Claude Code, etc.)
3. Request an evaluation that should trigger your skill
4. Verify the AI invokes your skill correctly
5. Check output matches expected format

### Validation Checklist

- [ ] YAML frontmatter parses correctly (no syntax errors)
- [ ] `description` field is ≤200 characters
- [ ] Skill name matches directory name (kebab-case)
- [ ] Instructions are clear and actionable
- [ ] Output format is well-defined
- [ ] No spelling/grammar errors
- [ ] Scripts are executable (if any)
- [ ] References are accurate and accessible

### Testing with Different AI Assistants

```bash
# Test with Claude Code
claude "Audit my login page using your-skill-name"

# Test with OpenAI Codex CLI (if available)
codex "Evaluate this interface with your-skill-name"
```

## 📖 Skill Structure Reference

### Required Files

**`SKILL.md`** - Core skill definition
- YAML frontmatter with `name` and `description`
- Markdown instructions for the AI agent
- Clear sections: When to Use, Inputs, Procedure, Output

### Optional Directories

**`scripts/`** - Executable helpers
- Shell scripts (`.sh`)
- Python scripts (`.py`)
- Node.js scripts (`.js`)
- Must be executable: `chmod +x script.sh`

**`references/`** - Supporting documentation
- Research papers
- Methodology explanations
- Industry standards
- Best practices guides

**`assets/`** - Data and templates
- JSON templates
- CSV data files
- Example inputs/outputs
- Configuration files

## 📝 SKILL.md Anatomy

### YAML Frontmatter (Required)

```yaml
---
name: skill-name              # kebab-case, matches directory name
description: Brief description of what this skill does (MAX 200 characters)
---
```

**Critical Constraints:**
- `name`: Must match directory name exactly
- `description`: MAX 200 characters (AI uses this for skill matching)
- YAML must be valid (test with YAML validator)

### Markdown Body (Required)

**Section 1: When to Use This Skill**
- Clear scenarios for invocation
- Helps AI decide when to use your skill
- Be specific about use cases

**Section 2: Inputs Required**
- List all required inputs
- Document optional inputs with defaults
- Specify input formats (URL, file path, code, screenshot)

**Section 3: Procedure**
- Step-by-step instructions
- Use numbered lists for clarity
- Be prescriptive: "Do X", not "You might do X"
- Include all necessary context

**Section 4: Output Format**
- Define expected structure
- Use markdown code blocks for examples
- Specify sections, headings, formatting

**Optional Sections:**
- References: Links to methodologies, standards
- Examples: Sample inputs and outputs
- Troubleshooting: Common issues and solutions

## 📜 Commit Convention

This repository uses **Conventional Commits** specification for automated changelog generation and semantic versioning.

### Format

```
<type>(<scope>): <subject>

<body>

<footer>
```

### Types

- `feat`: New skill or feature
- `fix`: Bug fix in existing skill
- `docs`: Documentation changes
- `style`: Formatting, whitespace (no logic change)
- `refactor`: Code restructuring (no behavior change)
- `test`: Adding or modifying tests
- `chore`: Maintenance tasks (dependencies, build)

### Scope

Use the skill name or affected area:
- Skill name: `wcag-audit`, `nielsen-heuristics`, etc.
- Area: `readme`, `contributing`, `package`, etc.

### Subject Rules

- Use imperative mood: "add" not "added" or "adds"
- No capitalization on first letter
- No period at end
- Maximum 50 characters
- Be specific and descriptive

### Examples

**Good Commits:**
```bash
feat(cognitive-walkthrough): add task analysis skill
fix(wcag-audit): correct WCAG 2.2 criteria references
docs(readme): add installation examples for npm
style(nielsen): format markdown tables
refactor(ux-audit): simplify evaluation structure
chore(deps): update agent skills specification
```

**Bad Commits:**
```bash
feat: new skill                          # Too vague, no scope
fix: fixed bugs                          # Not imperative, vague
feat(wcag): Added comprehensive audit    # Capitalized, not imperative
Update README.md                         # Not conventional format
Fixed typo                               # No type or scope
```

### Commit Body and Footer

**Body** (optional but recommended):
- Explain **why** the change was made
- Describe **what** was changed (if not obvious)
- Wrap at 72 characters

**Footer** (optional):
- Reference issues: `Closes #123`
- Note breaking changes: `BREAKING CHANGE: description`

**Full Example:**
```bash
git commit -m "feat(iso-42001): add AI governance audit skill

Implements comprehensive AI governance evaluation using ISO 42001:2023
standard. Covers risk management, ethics, security, transparency, and
regulatory compliance with EU AI Act and GDPR.

Closes #42"
```

## ✅ Quality Standards Checklist

Before committing a new skill or major change:

### Code Quality
- [ ] YAML frontmatter is valid (no syntax errors)
- [ ] `description` is ≤200 characters
- [ ] Skill name uses kebab-case
- [ ] Skill name matches directory name
- [ ] No spelling or grammar errors
- [ ] Instructions are clear and actionable
- [ ] Output format is well-defined

### Testing
- [ ] Tested locally with `npx skills add .`
- [ ] Verified AI invokes skill correctly
- [ ] Output matches expected format
- [ ] Scripts are executable (if any)
- [ ] No errors or warnings during execution

### Documentation
- [ ] Added to README.md skills table
- [ ] Added to CHANGELOG.md under `[Unreleased]`
- [ ] Included "When to Use" section
- [ ] Defined required and optional inputs
- [ ] Documented output format
- [ ] Added references (if applicable)

### Repository Hygiene
- [ ] Used Conventional Commits format
- [ ] Meaningful commit message
- [ ] No unrelated changes included
- [ ] Branched from latest `main`
- [ ] Ready for pull request

## 🚀 Publishing Workflow

### For Contributors (Pull Requests)

1. **Fork and Branch**
```bash
git checkout -b feat/your-skill-name
```

2. **Develop and Test**
```bash
# Create skill
# Test locally
npx skills add . --skill your-skill-name
```

3. **Commit**
```bash
git add .
git commit -m "feat(your-skill-name): add X evaluation skill"
```

4. **Push and PR**
```bash
git push origin feat/your-skill-name
# Open pull request on GitHub
```

### For Maintainers (Releases)

1. **Review PRs**
- Verify quality standards
- Test skill locally
- Check commit message format

2. **Merge to Main**
```bash
git merge feat/your-skill-name
```

3. **Update Version**
```bash
# Update version in package.json
npm version patch|minor|major

# Update CHANGELOG.md
# Move [Unreleased] entries to [X.Y.Z] section
```

4. **Create Release**
```bash
git tag v1.3.0
git push origin main --tags
```

5. **Publish to npm** (if configured)
```bash
npm publish
```

## 🔍 Multi-Agent Compatibility

Skills in this repository follow the **Agent Skills open standard** (December 2025). Write skills to be agent-agnostic.

### DO ✅
- Use neutral language: "the AI", "the assistant"
- Write portable instructions
- Use standard markdown and YAML
- Test with multiple AI assistants if possible

### DON'T ❌
- Reference specific AI agents: "Claude should...", "ChatGPT will..."
- Use proprietary extensions or formats
- Assume specific tool availability
- Hard-code agent-specific behaviors

## 📚 Resources for Developers

### Agent Skills Standard
- [Official Specification](https://github.com/anthropics/skills)
- [Anthropic Skills Docs](https://docs.anthropic.com/skills)

### Development Tools
- [YAML Validator](https://www.yamllint.com/)
- [Markdown Linter](https://github.com/markdownlint/markdownlint)
- [Conventional Commits CLI](https://github.com/conventional-changelog/commitlint)

### Testing Resources
- [Claude Code CLI](https://claude.ai/code)
- [OpenAI Codex CLI](https://platform.openai.com/docs/guides/code)

### Community
- [GitHub Discussions](https://github.com/mastepanoski/claude-skills/discussions)
- [Issues](https://github.com/mastepanoski/claude-skills/issues)
- [Pull Requests](https://github.com/mastepanoski/claude-skills/pulls)

## 🤔 Need Help?

- **General questions**: Open a [GitHub Discussion](https://github.com/mastepanoski/claude-skills/discussions)
- **Bug reports**: Create an [Issue](https://github.com/mastepanoski/claude-skills/issues)
- **Feature requests**: Create an [Issue](https://github.com/mastepanoski/claude-skills/issues) with `enhancement` label
- **Security issues**: Email maintainer privately

---

**Happy skill development!** 🎉

Your contributions help improve UX/UI evaluation for the entire AI community.
