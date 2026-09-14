---
name: protection-research
description: Frame protection-technology research and explore mechanisms, alternative designs, or new techniques when the goal is broad, an approach reaches its limits, or observations are unexplained. Routine implementation with a settled approach and evaluation of a fixed effectiveness claim do not need this skill.
---

# Explore protection research

Turn an uncertain protection objective into a grounded research question and evidence that selects the next experiment or narrows the candidate approaches. Reuse the user's task, project documents, implementations, and research records. Work within existing authorization and resource limits; apply only the parts needed for the current uncertainty.

## Frame the decision

- Identify the protection purpose, asset, required functionality, operating constraints, and decision the research should enable. Specify the relevant attacker's knowledge and ability to observe, modify, and query, the attack success event, and resource limits. A broad ambition such as stronger protection needs a concrete attack task and a useful target cost or outcome.
- Separate established facts from working assumptions. Derive missing context from available evidence; ask only about ambiguities that materially change the objective, threat model, substantial costs, or external impact. Reuse settled decisions, revisiting them as needed when the user changes direction or new evidence warrants it.

## Find the gap and develop candidates

- Start with the closest relevant approaches and their baselines. Consult original publications, official specifications, and reproduction code; record the assumptions, limitations, known failures, and exact sources supporting consequential facts. Use remembered techniques as search leads. Identify inaccessible sources or unavailable tools and what remains unverified; never invent citations or imply that a missing search establishes novelty.
- Trace where protected information originates and how representations, boundaries, and states make it observable. Identify the mechanism or constraint limiting the current approach. Explore relevant design changes, combinations, or transfers from other fields without exhausting a technique checklist.
- For a transferred technique, explain which property is useful here, what assumptions it needs, whether those assumptions hold, and what adaptation could invalidate it. For combinations, investigate interactions; component guarantees do not automatically carry over. Familiar approaches remain candidates when they best serve the objective.
- Distinguish **candidate solutions** from **competing explanations** of observations. For each promising candidate, connect its mechanism to a predicted difference from the baseline, an expected benefit and cost, a failure condition, and a small probe. Include implementation and instrumentation errors among plausible explanations. Do not require a fixed number of ideas or substitute novelty for value.

## Probe and update

- Rank probes by the decision they can change, expected benefit, information gained, and cost. Use an inexpensive counterexample when it can rule out a candidate, or a reduced prototype when feasibility is the uncertainty. Avoid a large implementation before testing its central assumption.
- Set a measurable time, compute, or attempt budget and a reassessment point within the overall allowance. Isolate experimental changes. Multiple-variable exploration is allowed, but it does not establish individual causes. Check that the observation method detects relevant known outcomes before relying on its signals; missing or broken measurements do not establish protection.
- Record the question, changes, predicted and actual observations, evidence location, and next decision briefly in the existing research record. Separate design limits, implementation defects, measurement failures, and insufficient budgets. Unexpected results may generate a hypothesis; label it as such rather than claiming prior prediction.
- Use new evidence to change the candidate, observation method, or level of abstraction when progress stalls. Keep rejected approaches and reasons. Reassess when the batch has narrowed candidates, selected the next useful experiment, or exhausted its budget; continue relevant authorized work within the remaining allowance. If none remains, report what additional resources would resolve. Propose unrelated discoveries separately.

Finish with the refined question, the candidate or hypothesis update, supporting evidence and gaps, and the next experiment with its rationale. A promising prototype justifies further work; adoption or an effectiveness claim requires validation under appropriate evaluation conditions. This skill does not require another skill or a separate report template.
