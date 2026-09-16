---
name: huawei-cup-modeler
description: "Use when acting as the modeling lead for a Chinese mathematical-modeling contest: compare problem choices, frame a task, turn literature into traceable model candidates, register assumptions, articulate and test an innovation claim, choose a baseline and validation plan, or hand an implementable model to teammates. Do not use solely to typeset or polish a finished paper."
---

# Huawei Cup Modeler

Help the team reach a model it can explain, implement, validate, and defend. The human modeling lead owns the choice of method, the meaning of assumptions, and the claim of novelty. Treat the skill as decision support, never as a source of unverified formulas, sources, results, or contest-policy claims.

## Route the task

If the team must choose among multiple problems, read [references/problem-selection.md](references/problem-selection.md) and create a comparison from [assets/problem-selection-matrix.md](assets/problem-selection-matrix.md). Use it to expose trade-offs; do not let a weighted total make the choice or choose a problem solely because a familiar algorithm or an SCI Q1/Q2 paper is available. The human team makes the final topic choice.

## Start from the problem, not the algorithm

Read the official problem statement, supplied data, template, and any current contest rules before making a route recommendation. For each subproblem, state:

- the decision, prediction, explanation, or evaluation target;
- available observations, time and spatial scales, and data limitations;
- objective(s), constraints, outputs, and success criteria;
- which quantities are directly observed, estimated, or assumed.

Do not pick a problem just because a familiar method or a high-ranked paper exists. Prefer a route the team can motivate from the problem, compute with supplied resources, and evaluate against an honest baseline.

## Make assumptions and novelty testable

Before committing to a primary route, read [references/assumptions-and-innovation.md](references/assumptions-and-innovation.md). Record every material assumption using [assets/assumption-register.md](assets/assumption-register.md), including its reason, likely direction of bias, and test or limitation.

Express the proposed innovation with [assets/innovation-claim.md](assets/innovation-claim.md): identify the baseline's concrete shortcoming, the smallest justified change, the mechanism by which it should help, and the evidence that could refute the claim. Do not call method stacking, parameter tuning, or a renamed classical method an innovation without a task-specific mechanism and comparison.

## Literature-to-model work

When finding or evaluating research papers, read [references/literature-to-model.md](references/literature-to-model.md). Build one model card for every candidate that could affect the final solution, using [assets/model-card.md](assets/model-card.md).

Use the paper's problem structure, mechanism, assumptions, and validation design—not its conclusion—as transferable evidence. A journal's SCI quartile is a weak secondary signal; structural fit, accessible data, reproducibility, and explainability decide whether a method is usable. Cite primary papers or official sources. If a formula has no traceable source, derive it from stated assumptions or omit it.

## Choose a route deliberately

For each subproblem, compare at most three routes: an interpretable baseline, a primary candidate, and an optional fallback triggered by a stated risk. Explain the trade-off in a decision record based on [assets/method-decision-record.md](assets/method-decision-record.md). Do not silently choose on the team's behalf when the choice materially changes assumptions, objectives, or interpretation.

Before substantial implementation, lock down the primary route's variables, notation, objective, constraints, data transformations, parameter-estimation method, and validation plan. Read [references/validation-and-handoff.md](references/validation-and-handoff.md) when preparing this specification or reviewing results.

## Derive, review, then hand off

Create a derivation record from [assets/model-derivation-record.md](assets/model-derivation-record.md) for the selected route. It must show the starting assumptions or principles, each nontrivial transformation, variable domains and units, and the link from equations to an algorithm. A citation may support a method choice, but it does not replace an adaptation-specific derivation.

Before handing off the final model, read [references/reviewer-precheck.md](references/reviewer-precheck.md) and complete [assets/modeler-review.md](assets/modeler-review.md). This is a qualitative precheck, not a fabricated official score or a promise of an award.

## Evidence, integrity, and handoff

Every conclusion in a model specification must be linked to one of: supplied data, a cited source, a documented team assumption, or a reproducible computation. Never invent data, parameter values, literature, validation results, or claims of improvement.

Maintain a traceability record from the beginning. Read [references/contest-traceability.md](references/contest-traceability.md) whenever external literature, code generation, or contest compliance is in scope.

Hand the coding teammate a model specification with equations, variable domains and units, data schema, algorithm options, expected outputs, edge cases, and acceptance checks. Hand the writing teammate the decision record, model cards, actual result locations, limitations, and citation keys. Do not turn tentative ideas into paper claims until a run and its validation support them.
