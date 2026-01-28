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
- **Import Priority**:
  1.  Found similar? -> Import -> Quarantine (Lint/Test) -> Patch.
  2.  No match? -> Create Fresh.
- **Friction Rule**: Friction 2-3 times -> New Skill.
