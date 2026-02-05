---
name: example-skill
description: Template skill demonstrating the Agent Skills standard structure with YAML frontmatter and markdown instructions
---

# Example Skill

This is a template skill that demonstrates the standard Agent Skills format. Use this as a starting point for creating your own skills.

## When This Skill is Invoked

This skill will be invoked when the AI agent determines (based on the description in the YAML frontmatter) that the user's request matches this skill's purpose.

## What This Skill Does

When invoked, the AI agent will follow these instructions:

1. **Greet the user** - Acknowledge that the example skill has been activated
2. **Explain the structure** - Describe the SKILL.md format:
   - YAML frontmatter with `name` and `description` (required)
   - Markdown content with clear instructions
3. **Show optional additions** - Explain that skills can include:
   - `/scripts/` - Executable Python or Bash scripts
   - `/references/` - Documentation loaded into context
   - `/assets/` - Templates and binary files
4. **Provide next steps** - Guide the user on how to create their own skill

## Example Instructions Format

Write clear, actionable instructions using:
- **Numbered steps** for sequential tasks
- **Bullet points** for options or lists
- **Code blocks** for examples
- **Bold text** for emphasis
- **Headers** for organization

## Code Example

If your skill needs to show code, use fenced code blocks:

```javascript
// Example: A simple function
function greet(name) {
  return `Hello, ${name}!`;
}
```

## Best Practices

1. Keep the description under 200 characters
2. Write clear, specific instructions
3. Use active voice and imperative mood
4. Include examples where helpful
5. Test your skill with different AI agents

## Success Criteria

The skill execution is successful when:
- ✅ The user understands the skill format
- ✅ The user knows how to create their own skills
- ✅ The user has a working template to start from

---

**Note:** This is an example skill. Replace this content with your actual skill instructions.
