---
name: protection-evaluation
description: Design or audit protection measurements and comparisons, validate an effectiveness claim, or judge adoption. Also use during exploration when the measurement setup needs scrutiny. Routine unit tests and candidate generation alone do not need this skill.
---

# Evaluate protection evidence

Evaluate a specific claim or adoption decision using project context, implementation, threat model, baselines, and evidence. Stay within authorized targets, data, and budgets; early measurement checks do not require a full adoption study.

## Establish what would support the decision

- Separate functional correctness, attack resistance, performance, and mathematical guarantees. Define the claim, asset, attacker knowledge and observation/modification/query capabilities, attack success criteria, evaluation targets, and resource limits. For adoption, identify required benefits and acceptable functional, integration, and operating costs.
- Budget setup, runs, review, and recording together. Without a given limit, state a small initial time or attempt bound and reassess before expanding. Report unavailable usage as unknown; effort bounds do not enforce usage or spending caps. Extra paid capacity or a higher spending limit requires authorization.
- Fix validation conditions and decision criteria. Use the closest relevant methods as baselines, including an unprotected implementation when meaningful. Match inputs, attacker capabilities, compute/time budgets, and tuning opportunities; disclose unavoidable differences. Evaluate an attacker who knows the protection.
- Preserve trusted reference definitions and expected answers separately from candidate changes. Check that final verification addresses the intended claim and assumptions.

## Establish that measurements are trustworthy

- Check known outcomes and controls before interpreting measurements. For attacks, verify success on a known vulnerable sample and test negative controls for spurious signals. If controls are unavailable, find another check or explicitly limit conclusions.
- Separate crashes, timeouts, unsupported features, missing traces, and instrumentation effects from defensive success. Investigate setup failures first. Test each central defense claim with an attempt to break it; size, entropy, or decompilation failure alone cannot establish security.

## Compare, explain, and check generalization

- When attributing effects to individual factors, use single-factor comparisons or ablations; use factorial designs for interactions. A bundle comparison alone does not identify individual contributions. Distinguish design limits, defects, measurement failures, and insufficient budgets; leave unresolved causes explicit.
- Validate preserved behavior, including relevant exceptions, side effects, and platform contracts. Check generalization on inputs, keys, samples, or environments not used during exploration, to the extent needed by the claim.
- Distinguish candidate changes from changes to the harness, baselines, or expected answers. For evaluation errors, preserve a minimal counterexample, correction rationale, and earlier results. Version the evaluation and rerun all members of each affected comparison under corrected conditions.
- For variable outcomes, report the replication unit, sample size, successes and failures, effect size, and relevant uncertainty. Repeated measurements of one sample are not independent samples. Retain unfavorable runs and explain exclusions; do not decide practical value from a p-value alone.

## Preserve a reproducible basis

- Link conclusions to commit and uncommitted patch, commands, environment/tool versions, configuration/input identifiers, test seeds, raw results, and aggregation. Provide a rerun entry point; disclose special equipment, manual steps, and nondeterminism. Use disclosable test keys and data; never fix seeds for production keys.
- Keep practical reduced failures as regression tests. Cross-check important conclusions through different implementations, observation paths, or verification methods when feasible. Prefer an existing executable check that resolves the claim at lower cost; add model review only for remaining uncertainty. Model agreement or repeated use of the same harness is not independent validation; disclose missing checks.

## Make the bounded decision

- Report unsuccessful attacks as “No success observed for attack A under conditions B within budget C.” This gives no guarantee against other attacks or mathematical security lower bound. State proof models, assumptions, and scope separately.
- Adopt, reject, or defer based on demonstrated benefit, preserved functionality, performance, integration and maintenance costs, and dependency policy. Narrow or defer claims with unmet criteria or required checks that do not fit the budget; provisional findings can justify further research.
- In the existing research record, keep the conclusion and evidence level, scope/budget, reproduction and baseline links, failures, competing explanations, missing checks, what would overturn the result, and next useful check. Preserve unresolved questions at resource limits. Use this decision to advance remaining authorized work; no other skill or separate report template is required.
