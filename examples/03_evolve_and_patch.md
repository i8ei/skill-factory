# Evolve and Patch

Don't delete; Evolve.

## 1. Capture Friction

When a skill fails or is annoying:

```bash
@evolution_log_capturer "The 'foo' skill failed to parse JSON correctly."
```

_This writes to `skills/foo/EVOLUTION_LOG.md`._

## 2. Propose Patch

```bash
@skill_patch_proposer "Read the log for 'foo' and fix the SKILL.md"
```

_The agent will rewrite the skill instruction._
