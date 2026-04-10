# Skill Writing Guide

Practical guidance for writing effective SKILL.md files and descriptions. Combines specification best practices with lessons learned from iterative skill development.

---

## Writing Effective Descriptions

The `description` field is the primary mechanism that determines whether Claude invokes your skill. Get this right.

### Front-Load Keywords

Put the most important trigger words at the beginning:

```yaml
# GOOD: Keywords first
description: "Generate TypeScript interfaces from JSON schema. Use when converting schemas, creating types, or building API clients."

# BAD: Keywords buried
description: "This skill helps developers who need to work with JSON schemas by providing a way to generate TypeScript interfaces."
```

### Include Trigger Conditions

Always include explicit "when to use" language:

```yaml
# GOOD: Clear "when" clause
description: "Debug React performance issues using Chrome DevTools. Use when components re-render unnecessarily, investigating slow updates, or optimizing bundle size."

# BAD: No trigger conditions
description: "Helps with React performance debugging."
```

### Be Specific

Name technologies, frameworks, and concrete use cases:

```yaml
# GOOD: Specific technologies
description: "Create Express.js REST endpoints with Joi validation, Swagger docs, and Jest tests. Use when building new APIs or adding endpoints."

# BAD: Too generic
description: "Build API endpoints with proper validation and testing."
```

### Make Descriptions "Pushy"

Claude currently tends to "undertrigger" skills — not using them when they'd be useful. Combat this by making descriptions slightly assertive about when to trigger:

```yaml
# GOOD: Pushy — covers adjacent use cases
description: "How to build a simple fast dashboard to display internal data. Make sure to use this skill whenever the user mentions dashboards, data visualization, internal metrics, or wants to display any kind of data, even if they don't explicitly ask for a 'dashboard.'"

# NEUTRAL: Only exact matches will trigger
description: "How to build a simple fast dashboard to display internal data."
```

All "when to use" info goes in the description, not in the SKILL.md body.

---

## Writing SKILL.md Content

### Use Imperative Form

Write instructions as direct commands:

```markdown
# GOOD
Run the setup script before generating components.
Save outputs to the workspace directory.

# LESS EFFECTIVE
The setup script should be run before generating components.
Outputs should be saved to the workspace directory.
```

### Explain the Why

Today's LLMs are smart. They have good theory of mind and when given a good harness can go beyond rote instructions. Rather than heavy-handed MUSTs, explain the reasoning:

```markdown
# GOOD
Grade each assertion against the actual outputs, not the prompt.
The grading must be evidence-based because users rely on these
scores to decide whether to iterate — false positives waste
their time, false negatives hide real improvements.

# LESS EFFECTIVE
You MUST ALWAYS grade assertions against outputs, NEVER against
prompts. ALWAYS provide evidence.
```

If you find yourself writing ALWAYS or NEVER in all caps, that's a yellow flag — reframe and explain the reasoning.

### Keep the Prompt Lean

Remove instructions that aren't pulling their weight. Read the transcripts from test runs — if the skill is making the model waste time on unproductive steps, remove those parts and see what happens.

### Define Output Formats Clearly

```markdown
## Report Structure
ALWAYS use this exact template:
# [Title]
## Executive summary
## Key findings
## Recommendations
```

### Include Examples

Show concrete input/output pairs:

```markdown
## Commit Message Format
**Example 1:**
Input: Added user authentication with JWT tokens
Output: feat(auth): implement JWT-based authentication
```

### Generalize, Don't Overfit

When iterating on a skill with test cases, resist fiddly changes that only fix specific examples. The skill will be used across many different prompts. Rather than oppressively constrictive rules, try different metaphors or recommend different working patterns. It's cheap to experiment.

---

## Progressive Disclosure in Content

### Level 1 — Brief Overview
```markdown
## What This Skill Does
Creates production-ready React components with TypeScript, hooks, and tests in 3 steps.
```

### Level 2 — Common Paths
```markdown
## Quick Start
```bash
# Most common use case (80% of users)
generate-component MyComponent
```
```

### Level 3 — Detailed Steps
```markdown
## Step-by-Step Guide
### Creating a Basic Component
1. Run generator
2. Choose template
3. Customize options
[Detailed explanations]
```

### Level 4 — Edge Cases
```markdown
## Advanced Configuration
For complex scenarios like HOCs, render props, or custom hooks,
see [ADVANCED.md](docs/ADVANCED.md).
```

---

## Domain Organization

When a skill supports multiple domains or frameworks, organize by variant so Claude loads only what's relevant:

```
cloud-deploy/
├── SKILL.md (workflow + selection logic)
└── references/
    ├── aws.md
    ├── gcp.md
    └── azure.md
```

---

## Common Pitfalls

1. **Burying the lede** — Put the most important information first in every section
2. **Kitchen-sink descriptions** — Keep descriptions under 1024 chars; be selective about trigger words
3. **Rigid instruction style** — Explain reasoning instead of using ALL CAPS RULES
4. **Overfitting to test cases** — Generalize from examples; the skill serves millions of prompts
5. **Monolithic SKILL.md** — Keep under 500 lines; extract to reference files
6. **Missing "when" clause** — Always tell Claude when to invoke the skill
7. **Vague examples** — Use concrete file paths, column names, realistic user language
