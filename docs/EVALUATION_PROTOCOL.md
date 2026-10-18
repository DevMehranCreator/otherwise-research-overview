# Proposed evaluation protocol

This is a protocol outline for future work, not a claim that the full study has been completed.

## Before a main evaluation

1. Record the exact source revision, dependency versions, hardware/environment, random seeds, and world-generator version.
2. Freeze the scoring rule, acceptance threshold, baseline systems, compute budget, and success metrics before running the held-out suite.
3. Keep held-out worlds and sealed truth unavailable to anyone tuning the tested agent.
4. Separate failures caused by model misspecification from failures caused by noise, weak instruments, numerical instability, infrastructure interruption, or insufficient experiment budget.
5. Preserve raw observations and append-only decision/claim ledgers. Do not silently edit earlier results after learning the truth.

## Core measures

- Predictive score on observations not used for fitting.
- Calibration and coverage of uncertainty intervals.
- Ability to identify structured residuals and reject an inadequate model family.
- Mechanism/parameter recovery where the evaluation world defines a unique recoverable truth.
- Cost per useful inference, including direct compute, world time, and downstream refits caused by an action.
- Repeatability across world seeds.
- False-discovery and false-retraction rates.
- Generalization to held-out worlds, including mechanisms outside the current hypothesis grammar.

## Language-interface measures (separate study)

- Numeric fidelity to structured engine output.
- Rate of unsupported facts or numbers.
- Preservation of claim status and uncertainty.
- Correct treatment of contradictions and counterfactuals.
- Clarification rate for ambiguous questions.

The language-interface study must not send sealed evaluation truths to the model and must not let model-generated explanations decide which scientific hypothesis is true.

## Reporting

Publish the denominator, failed runs, exclusions with reasons, uncertainty, and deviations from protocol. If a test is interrupted or underpowered, mark it as such rather than counting it as success or failure without qualification. Never change the scoring threshold after seeing results to improve the headline outcome.
