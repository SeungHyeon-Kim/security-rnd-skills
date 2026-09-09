# Security R&D Guidelines for AI Agents

A standalone guide for AI agents working on white-box cryptography, DEX and binary obfuscation, mobile security, and other security research.

**[Read in English](PROJECT-GUIDE.md) · [한국어](kr/PROJECT-GUIDE.md)**

## Why this exists

Working code is only part of security R&D. You also need to understand why an approach works, how it fails, and what the evidence actually supports.

This guide combines everyday engineering practices with a research loop:

**Ask a precise question → form competing hypotheses → run a small experiment → validate the evidence → decide what to do next.**

Routine development stays lightweight. Uncertain security claims get deeper investigation.

## How to use it

### Option 1: Use it as AGENTS.md

Copy your preferred language version to your repository root as `AGENTS.md`. Agents that support this convention can load it as project instructions; see the [Codex documentation](https://learn.chatgpt.com/docs/agent-configuration/agents-md).

If you already have an `AGENTS.md`, merge the guide into it while preserving project-specific rules and resolving conflicts. Start a new session and confirm that the agent has loaded the instructions.

### Option 2: Keep it as a separate guide

Copy your preferred language version into your repository as `PROJECT-GUIDE.md`. Add the following to your agent's project instructions, or paste it at the start of a task:

```text
Read PROJECT-GUIDE.md before starting and apply it to this task.
```

With either option, provide the task, authorized scope, build/test commands, and any resource limits. Link existing project documentation where available.

The guide works on its own. No playbook, plugin, or particular model is required.
