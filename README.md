# Security R&D — Agent Guidance

## What this is

Guidance files that make an AI coding agent (e.g., Claude Code) treat security work
as **research**, not routine implementation — aiming for a *verified conclusion*
(threat model, reproducible evidence, independent verification) rather than just
*working code*, always within strict scope and a non-negotiable safety floor.

Two forms, each in a Korean and an English variant:

- **`CLAUDE.md`** — always-on project guidance; lives at a repo root and applies to
  every task in that repo.
- **`security-rnd-guidelines` skill (`SKILL.md`)** — on-demand; invoke it for a specific,
  repo-independent spec or task.

## Why use it

General-purpose agents handle ordinary development well but tend to play it safe and
shallow on open-ended, adversarial, or sensitive security tasks. These files push
the agent to start from a hypothesis, decompose to first principles, think
adversarially ("how does this break?"), and hold its conclusions to a real bar —
while refusing out-of-scope or malicious work.
