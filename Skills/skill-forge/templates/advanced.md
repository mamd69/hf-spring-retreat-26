# Advanced Skill Template

Use this template for full-featured skills with comprehensive setup, integrations, scripts, and documentation.

---

```markdown
---
name: "My Advanced Skill"
description: "Comprehensive what with all features and integrations. Use when [trigger 1], [trigger 2], or [trigger 3]. Supports [technology stack]."
---

# My Advanced Skill

## Overview
[Brief 2-3 sentence description]

## Prerequisites
- Technology 1 (version X+)
- Technology 2 (version Y+)
- API keys or credentials

## What This Skill Does
1. **Core Feature**: Description
2. **Integration**: Description
3. **Automation**: Description

---

## Quick Start (60 seconds)

### Installation
```bash
./scripts/install.sh
```

### First Use
```bash
./scripts/quickstart.sh
```

Expected output:
```
Success: Setup complete
Success: Configuration validated
Ready to use
```

---

## Configuration

### Basic Configuration
Edit `config.json`:
```json
{
  "mode": "production",
  "features": ["feature1", "feature2"]
}
```

### Advanced Configuration
See [Configuration Guide](docs/CONFIGURATION.md)

---

## Step-by-Step Guide

### 1. Initial Setup
[Detailed steps]

### 2. Core Workflow
[Main procedures]

### 3. Integration
[Integration steps]

---

## Advanced Features

### Feature 1: Custom Templates
```bash
./scripts/generate.sh --template custom
```

### Feature 2: Batch Processing
```bash
./scripts/batch.sh --input data.json
```

### Feature 3: CI/CD Integration
See [CI/CD Guide](docs/CICD.md)

---

## Scripts Reference

| Script | Purpose | Usage |
|--------|---------|-------|
| `install.sh` | Install dependencies | `./scripts/install.sh` |
| `generate.sh` | Generate code | `./scripts/generate.sh [name]` |
| `validate.sh` | Validate output | `./scripts/validate.sh` |
| `deploy.sh` | Deploy to environment | `./scripts/deploy.sh [env]` |

---

## Resources

### Templates
- `resources/templates/basic.template` - Basic template
- `resources/templates/advanced.template` - Advanced template

### Examples
- `resources/examples/basic/` - Simple example
- `resources/examples/advanced/` - Complex example
- `resources/examples/integration/` - Integration example

### Schemas
- `resources/schemas/config.schema.json` - Configuration schema
- `resources/schemas/output.schema.json` - Output validation

---

## Troubleshooting

### Issue: Installation Failed
**Symptoms**: Error during `install.sh`
**Cause**: Missing dependencies
**Solution**:
```bash
npm install -g required-package
./scripts/install.sh --force
```

### Issue: Validation Errors
**Symptoms**: Validation script fails
**Solution**: See [Troubleshooting Guide](docs/TROUBLESHOOTING.md)

---

## API Reference
Complete API documentation: [API_REFERENCE.md](docs/API_REFERENCE.md)

## Related Skills
- [Related Skill 1](../related-skill-1/)
- [Related Skill 2](../related-skill-2/)

## Resources
- [Official Documentation](https://example.com/docs)
- [GitHub Repository](https://github.com/example/repo)
```
