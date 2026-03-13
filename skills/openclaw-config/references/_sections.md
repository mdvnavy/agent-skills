# Section Definitions

Rule categories for openclaw configuration best practices. Rules are automatically assigned to sections based on their filename prefix.

---

## 1. Secrets Management (secret)
**Impact:** CRITICAL
**Description:** Handling credentials, API keys, and other sensitive values. Keep secrets out of configuration files by using environment variables.

## 2. Editing (edit)
**Impact:** HIGH
**Description:** Using purpose-built JSON/YAML editors and schema-verified keys when modifying openclaw configuration files.

## 3. Validation (validate)
**Impact:** HIGH
**Description:** Validating configuration with `openclaw doctor --fix` before initiating a gateway restart.
