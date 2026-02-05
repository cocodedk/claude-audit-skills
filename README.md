# @mastepanoski/claude-skills

![Version](https://img.shields.io/badge/version-1.2.0-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![Skills](https://img.shields.io/badge/skills-6-orange)
![Agent Skills](https://img.shields.io/badge/agent%20skills-standard-purple)
![Commits](https://img.shields.io/github/commit-activity/m/mastepanoski/claude-skills)
![Last Commit](https://img.shields.io/github/last-commit/mastepanoski/claude-skills)

Custom Agent Skills collection compatible with multiple AI coding assistants.

**🌐 Featured on**: [skills.sh](https://skills.sh) | Open Agent Skills Directory

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
| `ux-audit-rethink` | **⭐ START HERE** - Holistic UX audit using IxDF's 7 factors, 5 usability characteristics, and 5 interaction dimensions. Comprehensive evaluation with strategic redesign proposals and research recommendations |
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

## 🌐 Discover More Skills

This repository is listed on:

### [skills.sh](https://skills.sh) - The Open Agent Skills Directory
**Official directory by Vercel** for discovering and sharing agent skills.

- **Automatic Indexing**: Your skills are automatically indexed once your GitHub repo follows the Agent Skills standard
- **Search & Discovery**: Users can find your skills by searching categories, authors, or keywords
- **Install Tracking**: See how many times your skills have been installed
- **Leaderboard**: Popular skills are featured on the platform

**How to appear on skills.sh:**
1. ✅ Follow Agent Skills standard (SKILL.md format) - Already done!
2. ✅ Publish to public GitHub repository - Already done!
3. ✅ Skills.sh automatically crawls and indexes GitHub repos with Agent Skills
4. 🔍 Search for "mastepanoski/claude-skills" on [skills.sh](https://skills.sh)

**Alternative directories:**
- [SkillsMP](https://skillsmp.com/) - Agent Skills Marketplace
- [Skills Directory](https://www.skillsdirectory.com/) - Open registry for agent skills
- [MCP Market](https://mcpmarket.com/tools/skills) - Agent Skills for Claude, ChatGPT & Codex

## 📖 Resources

- [Agent Skills Specification](https://github.com/anthropics/skills) - Official standard by Anthropic
- [skills.sh](https://skills.sh) - Open directory by Vercel
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
