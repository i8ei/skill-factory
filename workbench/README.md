# Workbench (Incubation Area)

This is the "Development Floor" of the Skill Factory.

## Purpose

- Use this directory to create, test, and iterate on **New Skill Packs**.
- Do NOT mix work-in-progress files with the Factory's infrastructure (`skills/`).

## Workflow

1.  **Create**: Make a folder here (e.g., `workbench/marketing_pack/`).
2.  **Develop**: Create `SKILL.md` files, templates, and examples.
3.  **Verify**: Run `skill_linter_auditor` and `skill_test_generator` against your work.
4.  **Export**: When ready, use `job_pack_composer` to move the folder out to an external repository.
    - `job_pack_composer "Export workbench/marketing_pack to Desktop"`

## Rules

- This directory is for **TEMPORARY** storage during development.
- Completed products must be **EXPORTED** and removed from here.
