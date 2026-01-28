# Skill Catalog Curator

This skill manages the inventory of the Skill Factory.

## Operational Mode: Scanning

Since no `registry.json` is present, this Curator operates in **Scanning Mode**.
It dynamically traverses the `skills/` directory to discover available skills by reading their `SKILL.md` files.

## How to Inventory

Ask the Curator: "List all available skills" -> It will list directories in `skills/`.
