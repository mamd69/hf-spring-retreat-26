# Example: React Component Generator Skill

A code generation skill showing prerequisites, templates, and multi-step workflow.

---

```markdown
---
name: "React Component Generator"
description: "Generate React functional components with TypeScript, hooks, tests, and Storybook stories. Use when creating new components, scaffolding UI, or following component architecture patterns."
---

# React Component Generator

## Prerequisites
- Node.js 18+
- React 18+
- TypeScript 5+

## Quick Start
```bash
./scripts/generate-component.sh MyComponent

# Creates:
# - src/components/MyComponent/MyComponent.tsx
# - src/components/MyComponent/MyComponent.test.tsx
# - src/components/MyComponent/MyComponent.stories.tsx
# - src/components/MyComponent/index.ts
```

## Step-by-Step Guide

### 1. Run Generator
```bash
./scripts/generate-component.sh ComponentName
```

### 2. Choose Template
- Basic: Simple functional component
- With State: useState hooks
- With Context: useContext integration
- With API: Data fetching component

### 3. Customize
Edit generated files in `src/components/ComponentName/`

## Templates
See `resources/templates/` for available component templates.
```
