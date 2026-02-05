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

| Skill | Description |
|-------|-------------|
| `example-skill` | A template skill showing the standard structure |

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

## 📝 License

MIT License - See LICENSE file for details

## 🤝 Contributing

Contributions welcome! Please open an issue or PR.

---

Built with ❤️ by [@mastepanoski](https://github.com/mastepanoski)
