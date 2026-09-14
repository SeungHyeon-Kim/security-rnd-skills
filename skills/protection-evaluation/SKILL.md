---
name: protection-evaluation
description: Design or audit protection-technology measurements and comparisons, validate a defined effectiveness claim, or judge adoption of an experimental technique. Use during exploration when the measurement setup itself needs scrutiny; routine unit tests and candidate generation alone do not need this skill.
---

# Evaluate protection evidence

Assess a specific protection claim or adoption decision using the relevant implementation, threat model, constraints, baselines, and evidence. Reuse existing project context and stay within authorized targets, data, and budgets. Apply the checks relevant to the claim; early measurement checks do not require a complete adoption study.

## Establish what would support the decision

- Separate functional correctness, attack resistance, performance, and mathematical guarantees. Define the claim, asset, attacker's knowledge and observation/modification/query capabilities, attack success event, evaluation targets, and resource limits. For adoption, identify the required benefit and acceptable functional, integration, and operating costs.
- Fix evaluation conditions and decision criteria before validation. Use an unprotected implementation where meaningful and the closest relevant existing methods as baselines. Match inputs, attacker capabilities, compute and time budgets, and tuning opportunities; disclose unavoidable differences. Evaluate an attacker who knows the protection rather than only replaying an uninformed attack.

## Establish that measurements are trustworthy

- Before interpreting measurements, check relevant known outcomes and controls. For attack evaluations, verify success on a known vulnerable sample and test negative controls for spurious signals. If suitable controls are unavailable, seek another verification path or explicitly limit the conclusions.
- Keep tool crashes, timeouts, unsupported features, missing traces, and instrumentation effects distinct from defensive success. Investigate setup failures before drawing effectiveness conclusions. Connect each central defense claim to an evaluation that attempts to break it; size, entropy, or decompilation failure alone cannot establish security.

## Compare, explain, and check generalization

- Use single-factor comparisons or component ablations by default; use factorial experiments when interactions are the question. A bundle of changes does not identify an individual cause. Keep design limitations, implementation defects, measurement failures, and insufficient budgets separate, leaving unresolved causes explicit.
- Validate preserved behavior, including relevant exceptions, side effects, and platform contracts. Check generalization on inputs, keys, samples, or environments not used during exploration, to the extent needed by the claim.
- Distinguish implementation changes from changes to the harness, baselines, or expected answers. If evaluation is wrong, retain a minimal counterexample and correction rationale, version the revised evaluation, and rerun every comparison target under the corrected conditions. Preserve earlier results.
- For variable outcomes, report the replication unit, sample size, successes and failures, effect size, and relevant uncertainty. Repeated measurements of one sample are not independent samples. Retain unfavorable runs and explain exclusions; do not decide practical value from a p-value alone.

## Preserve a reproducible basis

- Link important conclusions to the commit and any uncommitted patch, commands, environment and tool versions, configuration and input identifiers, test seeds, raw results, and aggregation method. Provide a rerun entry point for a supported environment; disclose specialized equipment, manual steps, and nondeterminism. Use disclosable test keys and data; never use fixed seeds for real production keys.
- Retain reduced failures as regression tests when practical. Cross-check important conclusions through different implementations, observation paths, or verification methods. Agreement between models or repeated runs of the same harness alone is not independent validation; disclose when an independent check was not performed.

## Make the bounded decision

- State unsuccessful attacks as “No success was observed for attack A under conditions B within budget C.” This is neither a guarantee against other attacks nor a mathematical security lower bound. For a proof, state its model, assumptions, and scope separately.
- Adopt, reject, or defer using demonstrated benefit, functional preservation, performance, integration and maintenance costs, and project dependency policy. A provisional result may justify another experiment without supporting adoption. If a material criterion is untested, state it and defer the unsupported claim or decision.
- Briefly record the conclusion and evidence level, scope and budget, reproduction links and baseline results, failures, competing explanations, missing checks, and what would overturn the conclusion. Finish with the decision and the most valuable next check. At the resource limit, preserve results and remaining uncertainty; do not relabel incomplete validation as success. Use the existing research record without requiring another skill or a separate report template.
