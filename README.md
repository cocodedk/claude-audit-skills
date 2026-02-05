# @mastepanoski/claude-skills

![Version](https://img.shields.io/badge/version-1.3.1-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![Skills](https://img.shields.io/badge/skills-7-orange)
![Agent Skills](https://img.shields.io/badge/agent%20skills-standard-purple)
![Commits](https://img.shields.io/github/commit-activity/m/mastepanoski/claude-skills)
![Last Commit](https://img.shields.io/github/last-commit/mastepanoski/claude-skills)

Professional UX/UI evaluation and AI governance skills for AI coding assistants. Audit your interfaces using industry-standard methodologies like Nielsen's heuristics, WCAG compliance, and Don Norman's principles.

## 🌐 Browse on skills.sh

**[📦 View all skills →](https://skills.sh/mastepanoski/claude-skills)** | Official directory by Vercel

Our skills are indexed on **[skills.sh](https://skills.sh/?q=mastepanoski)** — the open directory for discovering agent skills across the ecosystem. Each skill below has a direct link to its skills.sh page where you can see install commands, usage examples, and community stats.

## 🤖 Compatible AI Assistants

These skills work with any AI assistant supporting the **Agent Skills standard**:

- ✅ **Claude Code** (Anthropic)
- ✅ **OpenAI Codex CLI**
- ✅ **ChatGPT**
- ✅ Any other agent supporting the specification

## 🚀 Quick Start

```bash
# List all available skills
npx skills add mastepanoski/claude-skills --list

# Install a specific skill
npx skills add mastepanoski/claude-skills --skill wcag-accessibility-audit

# Install all skills
npx skills add mastepanoski/claude-skills
```

After installation, simply ask your AI assistant to use the skill:
- "Audit my login page using WCAG standards"
- "Evaluate this component with Nielsen's heuristics"
- "Review the visual design of this interface"

The AI will automatically detect when to use the installed skills based on your request.

## 📚 Available Skills

### 🎨 UX/UI Evaluation Suite

#### **⭐ ux-audit-rethink** - Complete UX Evaluation
**[→ View on skills.sh](https://skills.sh/mastepanoski/claude-skills/ux-audit-rethink)**

```bash
npx skills add mastepanoski/claude-skills --skill ux-audit-rethink
```

Holistic UX audit using the **Interaction Design Foundation's frameworks**:
- **7 UX factors**: Useful, Usable, Findable, Credible, Desirable, Accessible, Valuable
- **5 Usability characteristics**: Learnability, Efficiency, Memorability, Errors, Satisfaction
- **5 Interaction dimensions**: Words, Visual, Space, Time, Behavior

**Best for**: Comprehensive interface evaluation with strategic redesign proposals

**Example usage:**
```
"Perform a complete UX audit on my e-commerce checkout flow"
"Evaluate the overall UX of this dashboard and propose improvements"
```

---

#### **nielsen-heuristics-audit** - Usability Inspection
**[→ View on skills.sh](https://skills.sh/mastepanoski/claude-skills/nielsen-heuristics-audit)**

```bash
npx skills add mastepanoski/claude-skills --skill nielsen-heuristics-audit
```

Systematic evaluation using **Jakob Nielsen's 10 usability heuristics**:
- Visibility of system status
- Match between system and real world
- User control and freedom
- Consistency and standards
- Error prevention
- And 5 more...

**Includes**: Severity ratings (0-4 scale), actionable recommendations

**Best for**: Quick usability inspection, identifying major usability problems

**Example usage:**
```
"Check my app against Nielsen's heuristics"
"Find usability issues in this navigation menu"
```

---

#### **wcag-accessibility-audit** - Legal Compliance Checker
**[→ View on skills.sh](https://skills.sh/mastepanoski/claude-skills/wcag-accessibility-audit)**

```bash
npx skills add mastepanoski/claude-skills --skill wcag-accessibility-audit
```

Complete **WCAG 2.1/2.2** accessibility audit:
- **4 POUR principles**: Perceivable, Operable, Understandable, Robust
- **Conformance levels**: A, AA, AAA
- **Automated + manual testing** procedures

**Best for**: Legal compliance (ADA, Section 508), inclusive design, accessibility certification

**Example usage:**
```
"Audit my website for WCAG AA compliance"
"Check if this form meets accessibility standards"
```

---

#### **don-norman-principles-audit** - Fundamental Design Check
**[→ View on skills.sh](https://skills.sh/mastepanoski/claude-skills/don-norman-principles-audit)**

```bash
npx skills add mastepanoski/claude-skills --skill don-norman-principles-audit
```

Evaluate interfaces using **Don Norman's 7 principles** from *The Design of Everyday Things*:
- Discoverability, Affordances, Signifiers
- Feedback, Mapping, Constraints
- Conceptual models

**Best for**: Evaluating intuitiveness and learnability of new interfaces

**Example usage:**
```
"Check if users can discover key features in my app"
"Evaluate the affordances in this mobile interface"
```

---

#### **cognitive-walkthrough** - Task-Specific Deep Dive
**[→ View on skills.sh](https://skills.sh/mastepanoski/claude-skills/cognitive-walkthrough)**

```bash
npx skills add mastepanoski/claude-skills --skill cognitive-walkthrough
```

Step-by-step simulation of **novice user cognition** for specific tasks:
- Will users know what to do?
- Will they see how to do it?
- Will they understand feedback?
- Will they know if they succeeded?

**Best for**: Testing onboarding flows, critical user tasks, first-time user experience

**Example usage:**
```
"Walk through the signup process as a new user"
"Analyze the 'create new project' task for a first-time user"
```

---

#### **ui-design-review** - Visual Design Polish
**[→ View on skills.sh](https://skills.sh/mastepanoski/claude-skills/ui-design-review)**

```bash
npx skills add mastepanoski/claude-skills --skill ui-design-review
```

Comprehensive **visual design evaluation** across 10 dimensions:
- Typography & hierarchy
- Color system & contrast
- Spacing & layout grid
- Component consistency
- Branding & modern trends

**Best for**: Visual refinement, design system audits, brand consistency

**Example usage:**
```
"Review the visual design of my landing page"
"Check if my component library is consistent"
```

---

### 🛡️ AI Governance & Security

#### **iso-42001-ai-governance** - Responsible AI Audit
**[→ View on skills.sh](https://skills.sh/mastepanoski/claude-skills/iso-42001-ai-governance)**

```bash
npx skills add mastepanoski/claude-skills --skill iso-42001-ai-governance
```

AI system governance using **ISO 42001:2023** standard:
- Risk management & impact assessment
- Ethics & fairness evaluation
- Security & privacy controls
- Transparency & explainability
- Regulatory compliance (EU AI Act, GDPR)

**Best for**: AI product development, ML system audits, regulatory preparation

**Example usage:**
```
"Audit my recommendation algorithm for ISO 42001 compliance"
"Review AI governance practices for our chatbot"
```

---

## 💡 How to Use

### 1. Install the skill you need
```bash
npx skills add mastepanoski/claude-skills --skill nielsen-heuristics-audit
```

### 2. Provide context to your AI assistant
Share the URL, screenshot, or code of your interface:
```
"Here's my login page: https://example.com/login"
"I've attached a screenshot of my dashboard"
"Here's the React component code for my form"
```

### 3. Request the evaluation
```
"Audit this using WCAG standards"
"Check this against Nielsen's heuristics"
"Perform a complete UX evaluation"
```

### 4. Receive structured report
The AI will provide:
- ✅ What works well
- ❌ Issues found (with severity)
- 💡 Specific recommendations
- 🎯 Priority actions

## 🎯 Skill Selection Guide

**Choose based on your goal:**

| Your Goal | Recommended Skill |
|-----------|------------------|
| Complete UX overhaul | `ux-audit-rethink` |
| Quick usability check | `nielsen-heuristics-audit` |
| Legal accessibility compliance | `wcag-accessibility-audit` |
| Test if interface is intuitive | `don-norman-principles-audit` |
| Analyze specific user task | `cognitive-walkthrough` |
| Polish visual design | `ui-design-review` |
| AI system governance | `iso-42001-ai-governance` |

**Pro tip**: Start with `ux-audit-rethink` for comprehensive evaluation, then use specialized skills to deep-dive into specific areas.

## 🌐 Discover More Skills

### Featured on skills.sh

**[Browse our collection →](https://skills.sh/mastepanoski/claude-skills)** | **[Search all skills →](https://skills.sh/?q=mastepanoski)**

**[skills.sh](https://skills.sh)** is the official open directory by Vercel for discovering agent skills. Our skills are automatically indexed with:
- 📊 Real-time install statistics
- 🔍 Full-text search across all skills
- 📦 One-click install commands
- 🏆 Community leaderboard

**Other skill directories:**
- [SkillsMP](https://skillsmp.com/) - Agent Skills Marketplace
- [Skills Directory](https://www.skillsdirectory.com/) - Open registry
- [MCP Market](https://mcpmarket.com/tools/skills) - Multi-platform skills catalog

## 📖 Learn More

- **[Agent Skills Specification](https://github.com/anthropics/skills)** - Technical standard
- **[Claude Code Skills Docs](https://code.claude.com/docs/en/skills)** - Official documentation
- **[How to Create Skills](https://support.claude.com/en/articles/12512198-how-to-create-custom-skills)** - Tutorial

## 🤝 Contributing

Want to improve these skills or create new ones? Check out:
- **[DEVELOPMENT.md](DEVELOPMENT.md)** - Technical guide for developers
- **[CONTRIBUTING.md](CONTRIBUTING.md)** - Contribution guidelines and standards
- **[CHANGELOG.md](CHANGELOG.md)** - Version history

We welcome pull requests for:
- New evaluation frameworks
- Improved audit procedures
- Bug fixes and refinements
- Better examples and documentation

## 📝 License

MIT License - See [LICENSE](LICENSE) file for details

---

**Questions?** Open an issue on [GitHub](https://github.com/mastepanoski/claude-skills/issues)

Built with ❤️ by [@mastepanoski](https://github.com/mastepanoski)
