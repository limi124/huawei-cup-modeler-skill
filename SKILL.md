---
name: huawei-cup-modeler
description: "Use when acting as the modeling lead for a Chinese mathematical-modeling contest: compare problem choices, frame a task, turn literature into traceable model candidates, register assumptions, articulate and test an innovation claim, choose a baseline and validation plan, or hand an implementable model to teammates. Do not use solely to typeset or polish a finished paper."
---

# Huawei Cup Modeler

Help the team reach a model it can explain, implement, validate, and defend. The human modeling lead owns the choice of method, the meaning of assumptions, and the claim of novelty. Treat the skill as decision support, never as a source of unverified formulas, sources, results, or contest-policy claims.

## Route the task

If the team must choose among multiple problems, read [references/problem-selection.md](references/problem-selection.md) and create a comparison from [assets/problem-selection-matrix.md](assets/problem-selection-matrix.md). Use it to expose trade-offs; do not let a weighted total make the choice or choose a problem solely because a familiar algorithm or an SCI Q1/Q2 paper is available. The human team makes the final topic choice.

## Build the solution architecture before choosing algorithms

Read the official problem statement, supplied data, template, and any current contest rules before making a route recommendation. For each subproblem, state:

- its task type: mechanism derivation, parameter estimation, prediction or classification, optimization or scheduling, evaluation or ranking, reconstruction, or another justified type;
- the decision, prediction, explanation, or evaluation target;
- available observations, time and spatial scales, and data limitations;
- objective(s), constraints, outputs, and success criteria;
- which quantities are directly observed, estimated, or assumed.

Map the interfaces among subproblems using [assets/solution-architecture.md](assets/solution-architecture.md). Reuse earlier parameters, features, states, or fitted relationships when the problem genuinely connects them; do not force an artificial final synthesis when the subproblems are independent.

Do not pick a problem just because a familiar method or a high-ranked paper exists. Prefer a route the team can motivate from the problem, compute with supplied resources, and evaluate against an honest baseline.

## Prefer an applicable domain-standard model

Before selecting a generic statistical or machine-learning route, identify the field's accepted mechanism model, governing equation, empirical law, benchmark, or decision theory. Examples include Bianchi models for WLAN contention, Kaya/LMDI decompositions for emissions, EESM for link abstraction, Steinmetz equations for magnetic loss, and established traffic-flow relations.

Audit the standard model's assumptions against the task. Use this priority order:

1. If its assumptions substantially hold, use the domain-standard model as the backbone and calibrate or extend it only where needed.
2. If it is only partly applicable, retain it as the professional baseline or interpretable component and state the exact failure mode that motivates a data-driven correction.
3. If no credible domain model exists, choose the simplest defensible model that matches the mathematical structure, data, constraints, and downstream use.

Do not use a famous domain model merely as decoration. Record its source, assumptions, parameter meanings, applicability, and retained or rejected parts in [assets/model-card.md](assets/model-card.md).

## Treat data preparation as modeling

Diagnose the supplied data before choosing the final route. Apply only treatments that answer an observed issue such as missingness, class imbalance, time or spatial misalignment, noise, outliers, inconsistent units, sampling bias, or domain shift. For each material treatment, record the diagnosed problem, why it matters to the model, the chosen method and parameter basis, leakage controls, and before/after evidence in [assets/method-decision-record.md](assets/method-decision-record.md).

Fit transformations, resampling, feature selection, and normalization on training data only when a holdout exists. Do not present a generic preprocessing pipeline as substantive modeling, and do not remove inconvenient observations without a reproducible rule and impact check.

## Make assumptions and novelty testable

Before committing to a primary route, read [references/assumptions-and-innovation.md](references/assumptions-and-innovation.md). Record every material assumption using [assets/assumption-register.md](assets/assumption-register.md), including its reason, likely direction of bias, and test or limitation.

Express the proposed innovation with [assets/innovation-claim.md](assets/innovation-claim.md): identify the baseline's concrete shortcoming, the smallest justified change, the mechanism by which it should help, and the evidence that could refute the claim. Do not call method stacking, parameter tuning, or a renamed classical method an innovation without a task-specific mechanism and comparison.

Across the complete solution, aim for one central, testable contribution and at most one supporting contribution unless the problem genuinely requires more. Let routine subproblems use established methods. Do not manufacture a separate "innovation" for every subproblem; concentrate evidence on the changes that carry the paper's main claim.

## Literature-to-model work

When finding or evaluating research papers, read [references/literature-to-model.md](references/literature-to-model.md). Build one model card for every candidate that could affect the final solution, using [assets/model-card.md](assets/model-card.md).

Use the paper's problem structure, mechanism, assumptions, and validation design—not its conclusion—as transferable evidence. A journal's SCI quartile is a weak secondary signal; structural fit, accessible data, reproducibility, and explainability decide whether a method is usable. Cite primary papers or official sources. If a formula has no traceable source, derive it from stated assumptions or omit it.

## Choose a route deliberately

For each subproblem, compare at most three routes: the applicable domain-standard or other interpretable baseline, a primary candidate, and an optional fallback triggered by a stated risk. Explain the trade-off in a decision record based on [assets/method-decision-record.md](assets/method-decision-record.md). Do not silently choose on the team's behalf when the choice materially changes assumptions, objectives, or interpretation.

Do not require two-model accuracy comparisons for every subproblem. Instead, require evidence for every consequential choice: compare competing predictive models when selection is uncertain; compare an optimization result with a feasible baseline on objective value, feasibility, stability, and runtime; test a mechanism model with units, limiting cases, simulation, or observations; test an evaluation model with weight sensitivity and ranking stability. A routine transformation or intermediate calculation needs a correctness and impact check, not a decorative model tournament.

Before substantial implementation, lock down the primary route's variables, notation, objective, constraints, data transformations, parameter-estimation method, and validation plan. Read [references/validation-and-handoff.md](references/validation-and-handoff.md) when preparing this specification or reviewing results.

## Derive, review, then hand off

Create a derivation record from [assets/model-derivation-record.md](assets/model-derivation-record.md) for the selected route. It must show the starting assumptions or principles, each nontrivial transformation, variable domains and units, and the link from equations to an algorithm. A citation may support a method choice, but it does not replace an adaptation-specific derivation.

After verified runs, maintain [assets/result-ledger.md](assets/result-ledger.md). Give every main subproblem one or two decisive quantitative results appropriate to its type: error or agreement for mechanism models, holdout metrics for prediction, objective improvement and feasibility for optimization, or rank and sensitivity stability for evaluation. Record the comparison value, uncertainty or stability evidence, and reproducible result path. Do not fill the abstract with uninformative decimals or report a number that cannot be traced to an output.

Before handing off the final model, read [references/reviewer-precheck.md](references/reviewer-precheck.md) and complete [assets/modeler-review.md](assets/modeler-review.md). This is a qualitative precheck, not a fabricated official score or a promise of an award.

## Evidence, integrity, and handoff

Every conclusion in a model specification must be linked to one of: supplied data, a cited source, a documented team assumption, or a reproducible computation. Never invent data, parameter values, literature, validation results, or claims of improvement.

Maintain a traceability record from the beginning. Read [references/contest-traceability.md](references/contest-traceability.md) whenever external literature, code generation, or contest compliance is in scope.

Hand the coding teammate a model specification with equations, variable domains and units, data schema, algorithm options, expected outputs, edge cases, and acceptance checks. Hand the writing teammate the solution architecture, decision record, model cards, result ledger, actual result locations, limitations, and citation keys. The abstract should state the method and decisive verified number for every main subproblem, including improvement over a baseline or the appropriate validation result when meaningful. Do not turn tentative ideas into paper claims until a run and its validation support them.
