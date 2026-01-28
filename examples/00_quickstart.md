# Quickstart

The fastest way to use the factory.

## 1. Scout

```bash
# Check if it exists
@skill_scout_web "Find a skill that does X"
```

## 2. Create

```bash
# If not found, create it
@universal_skill_factory "Create a skill named 'foo_bar' that does X"
```

## 3. Validate

```bash
# Lint
@skill_linter_auditor "Check skills/foo_bar"

# Test
@skill_test_generator "Generate tests for skills/foo_bar"
```

## 4. Evolve

```bash
# If it fails
@evolution_log_capturer "Record failure in foo_bar: X happened instead of Y"
@skill_patch_proposer "Fix foo_bar based on logs"
```
