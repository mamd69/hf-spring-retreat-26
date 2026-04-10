# Claude Code Skill Specification

Complete reference for skill structure, YAML frontmatter, progressive disclosure, and validation.

---

## YAML Frontmatter (Required)

Every SKILL.md **must** start with YAML frontmatter containing exactly two required fields:

```yaml
---
name: "Skill Name"                    # REQUIRED: Max 64 chars
description: "What this skill does    # REQUIRED: Max 1024 chars
and when Claude should use it."       # Include BOTH what & when
---
```

### `name` Field

- **Type**: String
- **Max Length**: 64 characters
- **Format**: Human-friendly display name
- **Usage**: Shown in skill lists, UI, and loaded into Claude's system prompt
- **Best Practice**: Use Title Case, be concise and descriptive
- **Examples**:
  - "API Documentation Generator"
  - "React Component Builder"
  - "Database Schema Designer"
  - Bad: "skill-1" (not descriptive)

### `description` Field

- **Type**: String
- **Max Length**: 1024 characters
- **Format**: Plain text or minimal markdown
- **Content**: MUST include:
  1. **What** the skill does (functionality)
  2. **When** Claude should invoke it (trigger conditions)
- **Usage**: Loaded into Claude's system prompt for autonomous matching
- **Best Practice**: Front-load key trigger words, be specific about use cases
- **Examples**:
  - "Generate OpenAPI 3.0 documentation from Express.js routes. Use when creating API docs, documenting endpoints, or building API specifications."
  - "Create React functional components with TypeScript, hooks, and tests. Use when scaffolding new components or converting class components."
  - Bad: "A comprehensive guide to API documentation" (no "when" clause)
  - Bad: "Documentation tool" (too vague)

### YAML Formatting Rules

```yaml
---
# CORRECT: Simple string
name: "API Builder"
description: "Creates REST APIs with Express and TypeScript."

# CORRECT: Multi-line description
name: "Full-Stack Generator"
description: "Generates full-stack applications with React frontend and Node.js backend. Use when starting new projects or scaffolding applications."

# CORRECT: Special characters quoted
name: "JSON:API Builder"
description: "Creates JSON:API compliant endpoints: pagination, filtering, relationships."

# WRONG: Missing quotes with special chars
name: API:Builder  # YAML parse error!

# WRONG: Extra fields (ignored but discouraged)
name: "My Skill"
description: "My description"
version: "1.0.0"       # NOT part of spec
author: "Me"           # NOT part of spec
tags: ["dev", "api"]   # NOT part of spec
---
```

**Critical**: Only `name` and `description` are used by Claude. Additional fields are ignored.

---

## Directory Structure

### Minimal Skill (Required)

```
~/.claude/skills/                    # Personal skills location
└── my-skill/                        # Skill directory (MUST be at top level!)
    └── SKILL.md                     # REQUIRED: Main skill file
```

**IMPORTANT**: Skills MUST be directly under `~/.claude/skills/[skill-name]/`.
Claude Code does NOT support nested subdirectories or namespaces!

### Full-Featured Skill (Recommended)

```
~/.claude/skills/
└── my-skill/
    ├── SKILL.md                     # REQUIRED: Main skill file
    ├── scripts/                     # Executable scripts
    │   ├── setup.sh
    │   ├── validate.js
    │   └── deploy.py
    ├── resources/                   # Supporting files
    │   ├── templates/
    │   ├── examples/
    │   └── schemas/
    ├── references/                  # Docs loaded into context as needed
    ├── agents/                      # Subagent definitions
    ├── evals/                       # Test cases (evals.json)
    │   └── evals.json
    ├── eval-viewer/                 # Result viewer tools
    ├── assets/                      # Files used in output
    └── docs/                        # Additional documentation
```

### Skills Locations

**Personal Skills** (available across all projects):
- **Path**: `~/.claude/skills/`
- **Scope**: Available in all projects for this user
- **Version Control**: NOT committed to git (outside repo)
- **Use Case**: Personal productivity tools, custom workflows

**Project Skills** (team-shared, version controlled):
- **Path**: `.claude/skills/` in project root
- **Scope**: Available only in this project
- **Version Control**: SHOULD be committed to git
- **Use Case**: Team workflows, project-specific tools, shared knowledge

---

## Progressive Disclosure Architecture

Claude Code uses a **3-level progressive disclosure system** to scale to 100+ skills without context penalty:

### Level 1: Metadata (Name + Description)
- **Loaded**: At Claude Code startup, always
- **Size**: ~200 chars per skill
- **Purpose**: Enable autonomous skill matching
- **Context**: Loaded into system prompt for ALL skills
- 100 skills = ~6KB context (minimal!)

### Level 2: SKILL.md Body
- **Loaded**: When skill is triggered/matched
- **Size**: ~1-10KB typically
- **Purpose**: Main instructions and procedures
- **Context**: Only loaded for ACTIVE skills
- Keep under 500 lines; use reference files for overflow

### Level 3+: Referenced Files
- **Loaded**: On-demand as Claude navigates
- **Size**: Variable (KB to MB)
- **Purpose**: Deep reference, examples, schemas
- **Context**: Loaded only when Claude accesses specific files
- Scripts can execute without loading into context

**Benefit**: Install 100+ skills with ~6KB context. Only active skill content enters context.

---

## SKILL.md Content Structure

### Recommended 4-Level Structure

```markdown
# Your Skill Name

## Level 1: Overview (Always Read First)
Brief 2-3 sentence description of the skill.

## Prerequisites
- Requirement 1
- Requirement 2

---

## Level 2: Quick Start (For Fast Onboarding)

### Basic Usage
[Simplest use case]

### Common Scenarios
1. Scenario 1
2. Scenario 2

---

## Level 3: Detailed Instructions (For Deep Work)

### Step-by-Step Guide
[Detailed steps with code blocks and expected output]

### Advanced Options
[Configuration, integration, etc.]

---

## Level 4: Reference (Rarely Needed)

### Troubleshooting
[Common issues and solutions]

### Complete API Reference
See [API_REFERENCE.md](docs/API_REFERENCE.md)

### Examples
See [examples/](resources/examples/)
```

---

## Scripts and Resources

### Scripts Directory
- **Purpose**: Executable scripts that Claude can run
- **Location**: `scripts/` in skill directory
- **Best Practice**: Reference from SKILL.md with clear usage instructions

### Resources Directory
- **Purpose**: Templates, examples, schemas, static files
- **Location**: `resources/` in skill directory
- **Best Practice**: Reference or copy by scripts

### File References and Navigation

Claude can navigate to referenced files automatically. Use these patterns:

```markdown
# Markdown links
See [Advanced Configuration](docs/ADVANCED.md) for complex scenarios.

# Relative file paths
Use the template located at `resources/templates/api-template.js`

# Inline file content
See `resources/examples/config.json`:
```

**Best Practice**: Keep SKILL.md lean (~2-5KB). Move lengthy content to separate files and reference them.

---

## Validation Checklist

Before publishing a skill, verify:

**YAML Frontmatter**:
- [ ] Starts with `---`
- [ ] Contains `name` field (max 64 chars)
- [ ] Contains `description` field (max 1024 chars)
- [ ] Description includes "what" and "when"
- [ ] Ends with `---`
- [ ] No YAML syntax errors

**File Structure**:
- [ ] SKILL.md exists in skill directory
- [ ] Directory is DIRECTLY in `~/.claude/skills/[skill-name]/` or `.claude/skills/[skill-name]/`
- [ ] Uses clear, descriptive directory name
- [ ] NO nested subdirectories (Claude Code requires top-level structure)

**Content Quality**:
- [ ] Level 1 (Overview) is brief and clear
- [ ] Level 2 (Quick Start) shows common use case
- [ ] Level 3 (Details) provides step-by-step guide
- [ ] Level 4 (Reference) links to advanced content
- [ ] Examples are concrete and runnable
- [ ] Troubleshooting section addresses common issues

**Progressive Disclosure**:
- [ ] Core instructions in SKILL.md (~2-5KB)
- [ ] Advanced content in separate docs/
- [ ] Large resources in resources/ directory
- [ ] Clear navigation between levels

**Testing**:
- [ ] Skill appears in Claude's skill list
- [ ] Description triggers on relevant queries
- [ ] Instructions are clear and actionable
- [ ] Scripts execute successfully (if included)
- [ ] Examples work as documented

**Automated Validation**:
```bash
python -m scripts.quick_validate <path-to-skill-folder>
```
