# Example: README Generator Skill

A simple documentation skill showing minimal but effective structure.

---

```markdown
---
name: "README Generator"
description: "Generate comprehensive README.md files for GitHub repositories. Use when starting new projects, documenting code, or improving existing READMEs."
---

# README Generator

## What This Skill Does
Creates well-structured README.md files with badges, installation, usage, and contribution sections.

## Quick Start
```bash
# Answer a few questions
./scripts/generate-readme.sh

# README.md created with:
# - Project title and description
# - Installation instructions
# - Usage examples
# - Contribution guidelines
```

## Customization
Edit sections in `resources/templates/sections/` before generating.
```
