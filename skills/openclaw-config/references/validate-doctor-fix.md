---
title: Run openclaw doctor --fix Before Restarting the Gateway
impact: HIGH
impactDescription: Automatically identifies and resolves common configuration issues before they cause runtime failures
tags: validation, doctor, fix, restart, gateway, pre-flight
---

## Run openclaw doctor --fix Before Restarting the Gateway

Restarting the gateway with an invalid or misconfigured `openclaw.json` causes
downtime. Running `openclaw doctor --fix` first automatically detects and
resolves common issues, so restarts succeed on the first attempt.

**Incorrect (restart immediately after editing config):**

```bash
# Skips validation — any config error causes a failed restart
openclaw restart
```

**Correct (validate and auto-fix, then restart):**

```bash
# Inspect and fix common config issues automatically
openclaw doctor --fix

# Only restart once doctor reports the config is clean
openclaw restart
```

`openclaw doctor --fix` checks for:
- Missing required fields
- Invalid field values or types
- Deprecated keys that need migration
- Structural problems such as duplicate keys or malformed JSON/YAML
- Environment variable references that are undefined at runtime

If `openclaw doctor --fix` cannot resolve an issue automatically, it reports
the remaining problems with actionable guidance before exiting with a non-zero
status. Address those manually before proceeding with the restart.
