# Openclaw Config

## Structure

```
openclaw-config/
  SKILL.md       # Main skill file - read this first
  AGENTS.md      # This navigation guide
  CLAUDE.md      # Symlink to AGENTS.md
  references/    # Detailed reference files
```

## Usage

1. Read `SKILL.md` for the main skill instructions
2. Browse `references/` for detailed documentation on specific topics
3. Reference files are loaded on-demand - read only what you need

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
