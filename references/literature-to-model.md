# Literature to model

## What to search for

Search from the problem's mechanism and mathematical structure, not from a contest-title phrase. Combine the object or mechanism with the target and the decisive constraint. Examples include `uncertain demand + multi-objective routing + robust optimization` or `diffusion process + inverse parameter estimation + sparse observations`.

Collect only the sources needed to make a decision. For a serious candidate, an efficient set is usually one source establishing the method, one recent application with a similar structure, and one source that supports validation or a required domain assumption. A large bibliography is not evidence by itself.

## Evaluate a candidate before adopting it

For each candidate, record its source, mapping, requirements, and limits in a model card. Assess these in order:

1. **Structural fit** — Do the paper's target, variables, constraints, and time or spatial scales map to the task?
2. **Assumption fit** — Are its independence, stationarity, linearity, equilibrium, or observability assumptions defensible here?
3. **Data and computation fit** — Can the team obtain every needed input and run the method within the time budget?
4. **Evidence fit** — Can the proposed output be checked with a holdout, benchmark, physical constraint, counterfactual, sensitivity test, or comparison?
5. **Communication fit** — Can the team derive the essential equations and explain what each result means?

SCI Q1/Q2 status may help identify established research venues, but it cannot compensate for poor structural fit or an inaccessible method. Do not treat it as a quality certificate for a particular use.

## Adapt honestly

Separate the source method from the team's adaptation. State which mechanism, equation, loss term, constraint, or validation idea comes from the source; then state what is changed to meet the problem. Novelty can arise from a justified new constraint, coupling, objective, calibration strategy, or validation design. It is not created by renaming a known algorithm or stacking unrelated methods.

When a source is unavailable, rely on its DOI, publisher page, preprint, or another primary version. Do not cite snippets, an AI summary, or a reference that has not been read sufficiently to support the claimed use.
