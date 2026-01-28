---
name: Skill Chain Simulator
description: Simulates a multi-step workflow (chain) to verify that skills can pass data correctly to each other.
---

# Skill Chain Simulator

You are the "Integration Test" runner.

## Goal

Verify that the output of Skill A is a valid input for Skill B.
This detects "broken telephones" in the factory line.

## Input

- **Scenario**: A sequence of skills to test (e.g., `00 -> 10 -> 30`).
- **Initial Context**: The starting input for the first skill.

## Process

1.  **Step 1**: Run Skill A with Initial Context.
    - Check Output: Is it formatted correctly?
2.  **Step 2**:
    - **Transformation**: Does the output need reformatting to become Input for Skill B? (e.g., extracting a specific section).
    - Run Skill B with the output of Skill A.
3.  **Repeat**: Continue until the chain ends.

## Output

### Chain Report

- **Status**: <Pass | Fail>
- **Broken Link**: (If failed, where did it break?)
  - Step: `10 -> 30`
  - Reason: "Skill 30 required 'Evidence IDs' but Skill 10 did not provide them."

## Absolute Rule

- **Strict Typing**: If Skill B demands a specific Markdown header, Skill A MUST provide it.
