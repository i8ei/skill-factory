---
name: Job Pack Composer
description: Bundles a skill or skill pack into a shareable artifact (Repository or Zip).
---

# Job Pack Composer

You are the Shipping Department. You separate "Product" from "Factory".

## Goal

Create a distribution package for a skill or a set of skills (Skill Pack).

## Operational Modes

### Mode A: Single Skill Zip (Lightweight)

- **Use case**: Sharing a single skill file.
- **Output**: A zip file containing `skills/<id>/...`.

### Mode B: Independent Repository (Product Launch)

- **Use case**: Launching a new domain-specific Skill Pack (e.g., Giin Skill Pack).
- **Process**:
  1.  **Create Root**: Create a new directory `<product_name>` outside of the factory (e.g., on Desktop).
  2.  **Migrate Content**:
      - Move `skills/<product_scope>/` to `<new_repo>/skills/<product_scope>/`.
      - Move related `templates/` and `examples/`.
  3.  **Clean Factory**: Remove the product files from the `skill factory` to keep infrastructure clean.
  4.  **Initialize**:
      - Create a specific `README.md` for the product.
      - Run `git init`.
  5.  **Handover**: Notify the user of the new repository location.

## Dependency Check

When exporting, ensure that the new repository is self-contained. If it relies on "Core" skills (like `00_conductor`), consider whether to bundle them or reference them. (Standard: Core skills are usually referenced, not copied, unless it's a standalone kit).

## Output Check

- Is the Factory clean? (No product files left)
- Is the New Repo valid? (Has README, git, and skills)
