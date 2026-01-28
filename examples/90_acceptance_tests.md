# Factory Acceptance Tests

Run these to verify the Factory is operational.

## Test Suite 1: New Skill Creation

- **Action**: Run `universal_skill_factory` to create 'temp_skill'.
- **Check 1**: Directory `skills/temp_skill` exists.
- **Check 2**: `skills/temp_skill/SKILL.md` exists with frontmatter.
- **Check 3**: `skill_linter_auditor` passes on 'temp_skill'.

## Test Suite 2: Import & Quarantine

- **Action**: Run `skill_import_intake` with a dummy text.
- **Check**: Skill is created, Lint reports "Pass" or structured errors.

## Test Suite 3: Catalog & Deprecation

- **Action**: Ask Curator to "List all skills".
- **Expectation**: 'temp_skill' appears in the list.
- **Action**: Mark 'temp_skill' as deprecated in its SKILL.md.
- **Action**: Ask Curator.
- **Expectation**: Curator flags it as [DEPRECATED].
