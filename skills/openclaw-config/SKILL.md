---
name: openclaw-config
description: >
  Best practices for editing and validating openclaw.json gateway configuration files
  in JSON and YAML formats. Use when creating or modifying openclaw configuration files,
  setting gateway credentials or API keys, validating configuration before a gateway
  restart, or troubleshooting misconfigured openclaw.json settings.
---

# Openclaw Config

Guidelines for editing, securing, and validating openclaw gateway configuration files
(`.json` and `.yaml`).

## Rule Categories by Priority

| Priority | Category | Impact | Prefix |
|----------|----------|--------|--------|
| 1 | Secrets Management | CRITICAL | `secret-` |
| 2 | Editing | HIGH | `edit-` |
| 3 | Validation | HIGH | `validate-` |

## How to Use

Read individual rule files for detailed guidance and examples:

```
references/secret-env-variables.md
references/edit-dedicated-editors.md
references/edit-schema-driven-keys.md
references/validate-doctor-fix.md
```
