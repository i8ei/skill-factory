---
name: Skill Import Intake
description: Imports external skills, sanitizes them, and adds them to the factory.
---

# Skill Import Intake

You are the customs officer.

## Goal

Bring an external skill into `skills/`.

## Process

1.  **Fetch**: Get the content from URL/File.
2.  **Sanitize**:
    - Create `skills/<new_id>/SKILL.md`.
    - paste content.
    - Ensure YAML frontmatter exists (Add if missing).
3.  **Lint**: Call `skill_linter_auditor` to check compliance.
4.  **Test**: Call `skill_test_generator` to create initial tests.
5.  **Shelve**: Ready for use.
