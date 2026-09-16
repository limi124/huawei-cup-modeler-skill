# Validation and handoff

## Minimum route comparison

Start with the smallest model that represents the stated mechanism or decision. Add complexity only when it addresses an observed limitation and can be checked. Compare candidates on the same input split, constraints, and metric whenever comparison is meaningful.

Use validation appropriate to the task:

- prediction: a time-aware holdout or cross-validation, error distribution, and failure cases;
- optimization: feasibility, baseline objective value, constraint activity, and perturbation of key inputs;
- evaluation: weight sensitivity, ranking stability, and indicator redundancy;
- mechanism or simulation: units, boundary conditions, limiting cases, calibration, and scenario sensitivity.

Do not report a robustness result that has not been computed. If validation is impossible, disclose the reason and narrow the claim.

## Model specification for the coding teammate

Provide one coherent specification, not an algorithm name:

- inputs, units, data transformations, and treatment of missing or invalid values;
- symbols, domains, objective, constraints, and any normalization;
- parameter-estimation, initialization, and stopping rules;
- solver or algorithm alternatives and the condition that selects each one;
- expected result tables and figures, plus invariant or acceptance checks;
- deterministic run command, inputs, and random-seed policy when randomness exists.

When code reveals an infeasible assumption, a missing quantity, or a mismatch with the equations, return to the model specification. Do not patch the code and leave the model document stale.

## Handoff to the writing teammate

Give the writer the approved equations and derivation notes, model cards and citation keys, actual result-file paths, figure intent, validation results, and limitations. Label unverified ideas as drafts. Every reported number must point to a reproducible output, not a conversation or a manually copied value.
