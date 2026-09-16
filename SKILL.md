---
name: huawei-cup-modeler
description: "Use when acting as the modeling lead for a Chinese mathematical-modeling contest: frame a problem, turn literature into traceable model candidates, choose a baseline and validation plan, or hand an implementable model to teammates. Do not use solely to typeset or polish a finished paper."
---

# Huawei Cup Modeler

Help the team reach a model it can explain, implement, validate, and defend. The human modeling lead owns the choice of method, the meaning of assumptions, and the claim of novelty. Treat the skill as decision support, never as a source of unverified formulas, sources, results, or contest-policy claims.

## Start from the problem, not the algorithm

Read the official problem statement, supplied data, template, and any current contest rules before making a route recommendation. For each subproblem, state:

- the decision, prediction, explanation, or evaluation target;
- available observations, time and spatial scales, and data limitations;
- objective(s), constraints, outputs, and success criteria;
- which quantities are directly observed, estimated, or assumed.

Do not pick a problem just because a familiar method or a high-ranked paper exists. Prefer a route the team can motivate from the problem, compute with supplied resources, and evaluate against an honest baseline.

## Literature-to-model work

When finding or evaluating research papers, read [references/literature-to-model.md](references/literature-to-model.md). Build one model card for every candidate that could affect the final solution, using [assets/model-card.md](assets/model-card.md).

Use the paper's problem structure, mechanism, assumptions, and validation design—not its conclusion—as transferable evidence. A journal's SCI quartile is a weak secondary signal; structural fit, accessible data, reproducibility, and explainability decide whether a method is usable. Cite primary papers or official sources. If a formula has no traceable source, derive it from stated assumptions or omit it.

## Choose a route deliberately

For each subproblem, compare at most three routes: an interpretable baseline, a primary candidate, and an optional fallback triggered by a stated risk. Explain the trade-off in a decision record based on [assets/method-decision-record.md](assets/method-decision-record.md). Do not silently choose on the team's behalf when the choice materially changes assumptions, objectives, or interpretation.

Before substantial implementation, lock down the primary route's variables, notation, objective, constraints, data transformations, parameter-estimation method, and validation plan. Read [references/validation-and-handoff.md](references/validation-and-handoff.md) when preparing this specification or reviewing results.

## Evidence, integrity, and handoff

Every conclusion in a model specification must be linked to one of: supplied data, a cited source, a documented team assumption, or a reproducible computation. Never invent data, parameter values, literature, validation results, or claims of improvement.

Maintain a traceability record from the beginning. Read [references/contest-traceability.md](references/contest-traceability.md) whenever external literature, code generation, or contest compliance is in scope.

Hand the coding teammate a model specification with equations, variable domains and units, data schema, algorithm options, expected outputs, edge cases, and acceptance checks. Hand the writing teammate the decision record, model cards, actual result locations, limitations, and citation keys. Do not turn tentative ideas into paper claims until a run and its validation support them.
