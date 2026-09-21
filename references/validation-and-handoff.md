# Validation and handoff

## Minimum route comparison

Start with the applicable domain-standard model when one exists and its assumptions are defensible. Otherwise use the simplest model that represents the stated mechanism or decision. Add complexity only when it addresses an observed limitation and can be checked. Compare candidates on the same input split, constraints, and metric whenever comparison is meaningful.

Use validation appropriate to the task:

- prediction: a time-aware holdout or cross-validation, error distribution, and failure cases;
- optimization: feasibility, baseline objective value, constraint activity, and perturbation of key inputs;
- evaluation: weight sensitivity, ranking stability, and indicator redundancy;
- mechanism or simulation: units, boundary conditions, limiting cases, calibration, and scenario sensitivity.

Do not force an accuracy contest where it is not meaningful. A parameter conversion, deterministic preprocessing step, or exact derivation may need a correctness and impact check rather than a second model. Do not report a robustness result that has not been computed. If validation is impossible, disclose the reason and narrow the claim.

## Data treatment is part of the model

For every material treatment, record:

- the observed problem: missingness, imbalance, time or spatial misalignment, noise, outliers, inconsistent units, sampling bias, or domain shift;
- how it would bias, destabilize, or invalidate the downstream model;
- the treatment and the basis for its parameters or thresholds;
- leakage controls, especially fitting transformations and resampling only on training data;
- before/after evidence such as distribution, signal-to-noise ratio, class recall, synchronization error, retained sample count, or downstream validation change.

Do not apply a stock preprocessing chain without diagnosis. Do not delete data because it harms a desired conclusion. Preserve the raw data and make every exclusion reproducible.

## Model specification for the coding teammate

Provide one coherent specification, not an algorithm name:

- inputs, units, data transformations, and treatment of missing or invalid values;
- symbols, domains, objective, constraints, and any normalization;
- parameter-estimation, initialization, and stopping rules;
- solver or algorithm alternatives and the condition that selects each one;
- expected result tables and figures, plus invariant or acceptance checks;
- diagnostics and before/after outputs for every material data treatment;
- deterministic run command, inputs, and random-seed policy when randomness exists.

When code reveals an infeasible assumption, a missing quantity, or a mismatch with the equations, return to the model specification. Do not patch the code and leave the model document stale.

## Handoff to the writing teammate

Give the writer the approved equations and derivation notes, solution architecture, model cards and citation keys, actual result-file paths, figure intent, validation results, result ledger, and limitations. Label unverified ideas as drafts. Every reported number must point to a reproducible output, not a conversation or a manually copied value.

For every main subproblem, select one or two decisive numbers for the abstract. Use the evidence appropriate to the task: agreement error for a mechanism model, holdout performance for prediction, objective improvement plus feasibility or runtime for optimization, or rank plus sensitivity stability for evaluation. Include an improvement number only when a matched baseline exists. The abstract should communicate evidence, not dump every metric.
