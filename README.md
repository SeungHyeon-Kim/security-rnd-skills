# Security R&D Guidelines for AI Agents

A compact core guide and optional skills for agents researching protection technology. The scope includes cryptographic, software, and system protections; white-box cryptography, obfuscation, and mobile protection are examples, not limits.

**[Read in English](PROJECT-GUIDE.md) · [한국어](kr/PROJECT-GUIDE.md)**

## Why this exists

The aim is to help an agent understand the research purpose, develop alternatives, apply techniques from other fields, and investigate them autonomously within the authorized scope. Working implementations and reliable evidence should advance a useful decision.

The core combines engineering fundamentals with a short research loop:

**Understand the purpose → frame the question → develop grounded alternatives → run an informative experiment → validate the evidence → decide what to do next.**

Detailed procedures are optional and loaded when relevant. Routine development stays lightweight; exploration permits small prototypes; effectiveness and adoption claims require stronger evidence. The effect of these instructions on agent behavior and research outcomes still needs comparative evaluation.

## Contents

| Component | Purpose | English | 한국어 |
| --- | --- | --- | --- |
| Core guide | Purpose, autonomy, development, evidence, and reporting principles | [Guide](PROJECT-GUIDE.md) | [지침](kr/PROJECT-GUIDE.md) |
| `protection-research` | Broad goals, mechanisms, alternative designs, and new techniques | [Skill](skills/protection-research/SKILL.md) | [스킬](kr/skills/protection-research/SKILL.md) |
| `protection-evaluation` | Measurement, comparison, effectiveness claims, and adoption | [Skill](skills/protection-evaluation/SKILL.md) | [스킬](kr/skills/protection-evaluation/SKILL.md) |

The guide works on its own. Each skill is a self-contained procedure and does not require the other. Project facts and experiment results belong in the project's existing documents and research record.

## Use the core guide

### As AGENTS.md

Copy your preferred language version to your repository root as `AGENTS.md`. Agents that support this convention can load it as project instructions; see the [Codex documentation](https://learn.chatgpt.com/docs/agent-configuration/agents-md).

If you already have an `AGENTS.md`, merge the guide into it while preserving project-specific rules and resolving conflicts. Start a new session and confirm that the agent has loaded the instructions.

### As a separate file

Copy your preferred language version into your repository as `PROJECT-GUIDE.md`. Add the following to your agent's project instructions, or paste it at the start of a task:

```text
Read PROJECT-GUIDE.md before starting and apply it to this task.
```

Provide the higher-level protection objective, required behavior and practical constraints, authorized targets and data, available build/test commands, and resource limits. Link existing documentation instead of restating it. A broad goal is sufficient to start: the agent should derive research questions and candidate approaches, making consequential assumptions explicit and asking about material ambiguities.

## Add optional procedures

### With skill support

Choose the English folders under `skills/` or the Korean folders under `kr/skills/`. These are distribution locations, not automatic Codex discovery locations. Copy each desired skill folder to a location supported by your agent. For a Codex project, use:

```text
<target-repository>/
  .agents/skills/
    protection-research/SKILL.md
    protection-evaluation/SKILL.md
```

Install only one language version of each skill, preserving its folder and skill name. The two languages use the same names. Check that the desired skills appear in the agent's available skills before relying on automatic selection.

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

Read only the procedure relevant to the current decision. Neither is
required for routine development with a settled approach. If a procedure
is unavailable, apply PROJECT-GUIDE.md (or the merged AGENTS.md) and state
any actual evidence or capability limits.
```

Keep these paths consistent with your chosen layout. Optional procedures do not need to be read together or on every task, and their absence does not prevent use of the core guide. No plugin, connector, or particular model is required.
