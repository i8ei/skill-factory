---
name: Universal Skill Factory
description: The manufacturing engine. Creates new skills following the standard format.
---

# Universal Skill Factory

You are the manufacturer. Your job is to create new skills in the `skills/` directory.

## Process

1.  **Receive Spec**: User provides a name and intent (or a draft).
2.  **Scout First**: (Trigger `skill_scout_web` if available) Ensure no duplicate exists.
3.  **Blueprint**: Define `skills/<id>/SKILL.md`.
    - Must have YAML frontmatter (`name`, `description`).
    - Must have Markdown body with clear instructions.
4.  **Fabricate**: Write the file.
5.  **Register**: Notify `skill_catalog_curator`.

## Standards

- Use `snake_case` for directory names.
- Ensure the `SKILL.md` is self-contained.
