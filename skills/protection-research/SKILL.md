---
name: protection-research
description: Frame protection research and explore mechanisms, alternative designs, or new techniques when the goal is broad, an approach stalls, or observations are unexplained. Not needed for routine implementation or validation of a fixed effectiveness claim.
---

# Explore protection research

Turn an uncertain protection objective into a grounded question and evidence for the next research decision. Reuse project context and research records; stay within authorized targets, data, and resources.

## Frame the decision and budget

- Define the protection purpose, asset, required functionality, constraints, and intended decision. Specify relevant attacker knowledge, observation/modification/query capabilities, attack success criteria, and resources. Translate broad ambitions into a concrete attack task and useful target cost or outcome.
- Separate facts from assumptions. Reuse settled context, revisiting it when evidence or the user changes direction. Ask only about ambiguities materially affecting objectives, threat model, substantial costs, or external impact.
- Reuse agreed limits; set a measurable probe budget and reassessment point. Without a given limit, start with a small stated time or attempt bound. Distinguish measured usage, estimates, and unknown balances. Context capacity is not an allowance balance; effort bounds do not enforce usage or spending caps. Extra paid capacity or exceeding spending limits requires authorization.
- Include context preparation, tools, all agents, retries, integration, and verification in the total. Reserve enough for a credible check and a resumable record; narrow or stop a probe if it is unlikely to fit with those steps.

## Find the gap and develop candidates

- Start from the closest approaches and baselines. Use original publications, official specifications, and reproduction code; record sources, assumptions, limits, and known failures supporting consequential facts. Remembered techniques are search leads. Disclose inaccessible sources and tools; never invent citations or treat a failed search as evidence of novelty.
- Trace protected information through representations, boundaries, and states to identify what exposes it or limits protection. Explore relevant design changes, combinations, and transfers from other fields; do not exhaust a checklist.
- For transferred techniques, explain the useful property, required assumptions, their applicability, and adaptations that could invalidate them. Check interactions in combinations; component guarantees do not automatically carry over. Keep familiar approaches when they best serve the objective.
- Distinguish **candidate solutions** from **competing explanations**, including implementation and measurement errors. Connect each promising candidate's mechanism to a predicted difference from baseline, benefit, cost, failure condition, and small probe. Do not require a fixed number of ideas or novelty for its own sake.

## Probe and update

- Rank probes by decision value, expected benefit, information gain, and cost. Prefer a cheap counterexample for elimination or a reduced prototype for feasibility. Record removed conditions and what needs rechecking on the real target. Test the central assumption before a large implementation.
- Isolate changes. Multiple-variable exploration is allowed, but does not establish individual causes. Check that observations detect relevant known outcomes; missing or broken measurements do not establish protection.
- Record the question, change, prediction, actual result, evidence location, and next decision. Distinguish design limits, defects, measurement failures, and insufficient budgets. Label hypotheses arising from unexpected results as new hypotheses.
- At each checkpoint, continue, redirect, or stop using observed progress and the next probe's value. Change candidate, measurement method, or abstraction when warranted. Unchanged retries need a reason, such as a transient fault or planned replication. Stop uninformative repetition; keep rejected approaches and reasons. End exploration when the current research decision has enough evidence, even with budget left. At the limit, preserve evidence and unresolved questions.

## Coordinate independent work when useful

- Use one research agent by default. When tools and authorization permit, delegate separable work only if expected information or time benefits justify total usage and coordination. Specify distinct questions or approaches, relevant context, deliverables, worker budgets, and checkpoints. All further delegation shares the allowance; reassess before increasing concurrency.
- Share brief findings, assumptions, evidence/reproduction links, failures, and unresolved claims. Avoid full histories or repeated broadcasts. Check supporting evidence and applicability before reusing another branch's findings; resolve disagreements through a discriminating check. Agreement alone is not validation.

Use the findings for the next decision; an effectiveness or adoption claim requires validation. Continue remaining authorized work within the overall budget. Preserve results in the existing research record; no other skill or report template is required. Propose unrelated discoveries separately.
