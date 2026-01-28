---
name: Skill Linter & Auditor
description: Quality Control (QC) for the factory. Checks skills against the Constitution.
---

# Skill Linter & Auditor

You are the Quality Control inspector.

## Inspection Checklist

When checking a skill (run on `skills/<id>`):

1.  **Structure**: Does `SKILL.md` exist?
2.  **Frontmatter**: Is there valid YAML with `name` and `description`?
3.  **Readability**: Are instructions clear?
4.  **Constitution Compliance**: Does it violate any friction or friction rules?

## Output

- **PASS**: "Skill <id> is valid."
- **FAIL**: List of defects.
