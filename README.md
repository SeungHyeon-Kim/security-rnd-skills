# Security R&D Guidelines for AI Agents

A compact core guide and optional skills for agents researching protection technology. The scope includes cryptographic, software, and system protections; white-box cryptography, obfuscation, and mobile protection are examples, not limits.

**[Read in English](PROJECT-GUIDE.md) · [한국어](kr/PROJECT-GUIDE.md)**

## Why this exists

These instructions help agents connect protection research to a useful decision, develop grounded alternatives, and investigate within authorization. Working implementations and reliable evidence should support that decision.

The core combines engineering fundamentals with a short research loop:

**Understand the purpose → frame the question → develop grounded alternatives → run an informative experiment → validate the evidence → decide what to do next.**

Load detailed procedures only when relevant. Routine development stays lightweight; exploration permits prototypes; effectiveness and adoption claims require validation. The instructions' effect on research outcomes still needs comparative evaluation.

For workflow evaluation, compare with single-agent exploration on representative tasks under the same model, tools, and total budget. Count failed runs, coordination, and validation. Compare supported decisions, errors, human intervention, elapsed time, and actual usage; limit cost claims when usage is unavailable. Budget this trial separately; individual delegated tasks do not require it.

## Contents

| Component | Purpose | English | 한국어 |
| --- | --- | --- | --- |
| Core guide | Purpose, autonomy, development, evidence, and reporting principles | [Guide](PROJECT-GUIDE.md) | [지침](kr/PROJECT-GUIDE.md) |
| `protection-research` | Broad goals, mechanisms, alternative designs, and new techniques | [Skill](skills/protection-research/SKILL.md) | [스킬](kr/skills/protection-research/SKILL.md) |
| `protection-evaluation` | Measurement, comparison, effectiveness claims, and adoption | [Skill](skills/protection-evaluation/SKILL.md) | [스킬](kr/skills/protection-evaluation/SKILL.md) |

The guide and each skill work independently. Keep project facts and results in existing documents and research records. Findings can lead from exploration to evaluation, or back to investigation, without requiring both skills.

## Use the core guide

### As AGENTS.md

Copy your preferred language version to your repository root as `AGENTS.md`. Agents that support this convention can load it as project instructions; see the [Codex documentation](https://learn.chatgpt.com/docs/agent-configuration/agents-md).

If you already have an `AGENTS.md`, merge the guide into it while preserving project-specific rules and resolving conflicts. Start a new session and confirm that the agent has loaded the instructions.

### As a separate file

Copy your preferred language version into your repository as `PROJECT-GUIDE.md`. Add the following to your agent's project instructions, or paste it at the start of a task:

```text
Read PROJECT-GUIDE.md before starting and apply it to this task.
```

Provide the protection objective, required behavior, practical constraints, authorized targets/data, build/test commands, and resource limits. Link existing context. A broad goal is sufficient: the agent derives questions and candidates, states consequential assumptions, and asks about material ambiguities.

State limits in observable units (time, attempts, tokens, credits, or spend) and keep those units distinct. Context capacity is not remaining allowance. Use runtime spending and concurrency controls where supported; instructions cannot enforce billing caps or prevent interruption. Without a stated budget, begin with a small bounded probe and reassess; unknown balances remain unknown.

## Add optional procedures

### With skill support

Choose the English folders under `skills/` or the Korean folders under `kr/skills/`. These are distribution locations, not automatic Codex discovery locations. Copy each desired skill folder to a location supported by your agent. For a Codex project, use:

```text
<target-repository>/
  .agents/skills/
    protection-research/SKILL.md
    protection-evaluation/SKILL.md
```

Install one language version per skill, preserving folder and skill names. Both languages use the same names. Confirm the skills appear in the agent's available skills before relying on automatic selection.

Codex initially receives skill names and descriptions and reads a skill's body when selected. Descriptions specify when each procedure applies; in Codex CLI or the IDE extension, you can also explicitly invoke `$protection-research` or `$protection-evaluation`. See the [official skill documentation](https://learn.chatgpt.com/docs/build-skills) for discovery and invocation details.

### Without skill support

Copy the desired skill folders from one language into `skills/` at the target repository root. Add the actual paths and conditions to the existing project instructions, for example:

```text
When framing a broad protection-research goal, investigating a mechanism,
or exploring alternative designs or new techniques, read
skills/protection-research/SKILL.md and apply the relevant procedure.

When designing research measurements or comparisons, assessing protection
effectiveness, or deciding adoption, read
skills/protection-evaluation/SKILL.md and apply the relevant procedure.

Read only the procedures relevant to the current decision. Neither is
required for routine development with a settled approach. If a procedure
is unavailable, apply PROJECT-GUIDE.md (or the merged AGENTS.md) and state
any actual evidence or capability limits.
```

Keep paths consistent with your layout. Load procedures only when useful; their absence does not prevent using the core guide. No plugin, connector, or particular model is required.
