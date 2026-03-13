---
title: Use Environment Variables for Credentials and API Keys
impact: CRITICAL
impactDescription: Eliminates credential exposure and makes configuration portable across deployment environments
tags: secrets, credentials, api-keys, environment-variables, security
---

## Use Environment Variables for Credentials and API Keys

Hardcoding credentials, API keys, or other sensitive values directly into
`openclaw.json` or `.yaml` configuration files exposes them to version control
leaks and limits portability across environments.

**Incorrect (hardcoded secret in config):**

```json
{
  "gateway": {
    "admin_token": "s3cr3t-admin-key-abc123",
    "database": {
      "password": "mypassword"
    }
  }
}
```

**Correct (reference environment variables):**

```json
{
  "gateway": {
    "admin_token": "$OPENCLAW_ADMIN_TOKEN",
    "database": {
      "password": "$OPENCLAW_DB_PASSWORD"
    }
  }
}
```

Set the values in the environment before starting the gateway:

```bash
export OPENCLAW_ADMIN_TOKEN="s3cr3t-admin-key-abc123"
export OPENCLAW_DB_PASSWORD="mypassword"
openclaw start
```

This pattern keeps secrets out of configuration files entirely, prevents
accidental commits of sensitive data, and makes configuration reusable across
development, staging, and production environments.
