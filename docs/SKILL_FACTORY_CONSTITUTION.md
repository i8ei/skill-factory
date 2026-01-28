# Skill Factory Constitution

The Skill Factory is a standardized environment for creating, maintaining, and evolving AI agent "skills". A "skill" is a self-contained package of instructions (SKILL.md) and resources.

## 1. Skill Structure

Every skill must reside in `skills/<skill_id>/` and contain at least:

- `SKILL.md`: The definition file. Must contain YAML frontmatter (name, description) and Markdown instructions.
- `README.md` (Optional): Public-facing documentation for humans.

## 2. The Factory Lifecycle

1.  **Scout**: Before creating a new skill, search for existing ones.
2.  **Import/Create**: Bring in raw materials or draft new logic.
3.  **Lint**: Ensure compliance with this Constitution (Metadata, formatting).
4.  **Test**: Verify functionality with specific prompts/cases.
5.  **Catalog**: Register the skill in the Factory content.
6.  **Patch**: Evolve skills through usage logs (Evolution Logs).

## 3. The "Friction" Rule

- Do not create a new skill for every minor task.
- If a task feels repetitive (friction) 2-3 times, consider making it a skill.

## 4. Procurement Protocol

- **Scout First**: Before creating ANYTHING, run `skill_scout_web`.
- **Self-Improvement**: If the factory itself lacks a capability, ask `factory_kaizen_architect`.
- **Import Priority**:
  1.  Found similar? -> Import -> Quarantine (Lint/Test) -> Patch.
  2.  No match? -> Create Fresh.

- **Friction Rule**: Friction 2-3 times -> New Skill.

## 5. Product Separation Rule (Infrastructure vs. Product)

- **Factory Infrastructure**: Skills in `skill factory/skills/` must be restricted to "Meta-Skills" that operate the factory itself (Core, QA, Procurement, Distribution).
- **Product Incubation (Workbench)**: **New Skill Packs must be developed in `workbench/`.**
  - Do not pollute the main `skills/` directory with work-in-progress.
  - Use `skill_linter_auditor` to check skills in `workbench/`.
- **Product Export**: Completed packs **MUST** be exported to an independent repository.
  - Use `job_pack_composer` to move from `workbench/` to external.

## 6. Product Composition Rule (The "Life" Rule)

- **Mandatory Self-Improvement**: Every Product (Skill Pack) produced by this factory **MUST** include a "Kaizen Skill" (Self-Improvement).
  - A product must be able to analyze its user's pain points and suggest improvements to itself.
  - Example: `99_activity_kaizen`, `99_project_retrospective`.
