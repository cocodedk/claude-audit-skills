# @mastepanoski/claude-skills

Custom Agent Skills collection compatible with multiple AI coding assistants.

## 🤖 Compatible Agents

This repository uses the **Agent Skills open standard**, making these skills compatible with:

- ✅ **Claude Code** (Anthropic)
- ✅ **OpenAI Codex CLI**
- ✅ **ChatGPT**
- ✅ Any other agent supporting the Agent Skills specification

## 📦 Installation

### Install from GitHub

```bash
# List available skills
npx skills add mastepanoski/claude-skills --list

# Install a specific skill
npx skills add mastepanoski/claude-skills --skill example-skill

# Install all skills
npx skills add mastepanoski/claude-skills
```

### Install from npm (once published)

```bash
npx skills add @mastepanoski/claude-skills --skill example-skill
```

## 📚 Available Skills

### 🎨 UX/UI Evaluation Suite

| Skill | Description |
|-------|-------------|
| `example-skill` | A template skill showing the standard structure |
| `don-norman-principles-audit` | Evaluate UX/UI using Don Norman's 7 fundamental design principles: discoverability, affordances, signifiers, feedback, mapping, constraints, and conceptual models |
| `nielsen-heuristics-audit` | Comprehensive usability evaluation using Jakob Nielsen's 10 industry-standard heuristics. Systematic audit with severity ratings and actionable recommendations |
| `wcag-accessibility-audit` | Complete WCAG 2.1/2.2 accessibility audit across 4 POUR principles. Legal compliance checker with A/AA/AAA conformance levels, automated + manual testing procedures |
| `cognitive-walkthrough` | Deep-dive task-specific usability analysis. Simulates novice user cognition step-by-step through the 4 cognitive questions to identify learnability issues and failure points |
| `ui-design-review` | Comprehensive visual design and aesthetics evaluation across 10 dimensions: hierarchy, typography, color, spacing, consistency, imagery, layout, components, branding, and modern standards |

## 🏗️ Skill Structure

Each skill follows the Agent Skills standard format:

```
skill-name/
├── SKILL.md          # Core prompt and instructions (REQUIRED)
├── scripts/          # Executable helpers (optional)
├── references/       # Documentation and context (optional)
└── assets/           # Templates and files (optional)
```

### SKILL.md Format

```markdown
---
name: skill-name
description: Brief description (max 200 chars) - used by AI to determine when to invoke
---

# Skill Instructions

Clear, step-by-step instructions the AI agent will follow...
```

## 🚀 Creating Your Own Skills

1. Create a new folder in `skills/`
2. Add a `SKILL.md` file with frontmatter and instructions
3. (Optional) Add helper scripts, references, or assets
4. Test locally: `npx skills add . --skill your-skill-name`
5. Commit and push to GitHub

## 📖 Resources

- [Agent Skills Specification](https://github.com/anthropics/skills)
- [Claude Code Skills Docs](https://code.claude.com/docs/en/skills)
- [How to Create Custom Skills](https://support.claude.com/en/articles/12512198-how-to-create-custom-skills)

## 🤝 Contributing

We welcome contributions! Please read our [Contributing Guide](CONTRIBUTING.md) for:
- How to submit new skills
- Commit message conventions (Conventional Commits)
- Pull request process
- Testing guidelines

See [CHANGELOG.md](CHANGELOG.md) for version history.

## 📝 License

MIT License - See [LICENSE](LICENSE) file for details

---

Built with ❤️ by [@mastepanoski](https://github.com/mastepanoski)
