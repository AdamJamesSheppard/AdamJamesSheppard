# Portfolio quality review — 2026-10-11

Purpose: select a rounded portfolio without confusing presentation quality with
scientific validity. Review by the implementing assistant, not an independent
assessor. This is a code/document inspection and bounded software testing exercise;
it confers no research gate promotion. No repository was deleted, renamed, archived,
or made private. Original experiment files remain unchanged in the repair PRs.

## Selection criteria

Assess mathematical/numerical correctness, task and metric alignment, leakage,
reproducibility, documented assumptions, testable evidence, scientific limitations
and usefulness to the overall portfolio. Breadth is secondary to defensible claims.
No stars, attractive plots or repository descriptions serve as validation.

## Current FPE/operator-learning research

Inspected remote main `23e260960c4a750ec1fc0aa1ef6280e561db0fb9`, its programme
documents, and current local scientific state. This is the strongest *documented
research programme* in this selection: versioned assumptions, failure history,
tests and explicit qualification gates. That assessment is relative to the other
inspected repositories, not a certification of every solver path. G04 reference
applicability remains OPEN, and the neural pilot is unqualified. Local newer G04
work is separate from remote main and was not modified in this portfolio task.
Governance independence remains incomplete while owner credentials are shared.

Keep this as the principal research entry, with direct links to current scope and
evidence. Do not advertise a production neural solver or completed assimilation.

## C++ Lorenz utility

Base `11020bc96423a5c9b2c3e67bc60975fa6f3df89f`; inspected both source files.
`RungeKutta.cpp` has invalid OpenMP private declarations and attempts parallel
timesteps with shared dependent state. Initial-time/randomisation/output accounting
also require repair. The historical source is unsuitable as a qualified generator.

[Repair PR](https://github.com/AdamJamesSheppard/Lorenz-Atrractor-Revisited-C-/pull/1),
commit `e5dec3bcae4e3c1c4b7667955efc63d5b2ad6ef0`, adds a separate sequential
streaming integrator and8 passing tests, including analytic decay and an independent
short-horizon DOP853 comparison. Long-time chaotic accuracy remains unqualified.
Feature as a numerical-engineering project under review, not a validated dataset.

## Madrid time-series work

Base `bf14dcc48e5d46516bd6a1e3e0b993a74e05e6bb`; inspected notebook code and
interpretations. Full-series imputation/feature inspection leaks evaluation
information. The custom percentage score is mislabelled accuracy; the unit-conversion
narrative and several statistical interpretations are unsound. Original data are
absent, so reported historical accuracy has not been independently reproduced.

[Repair PR](https://github.com/AdamJamesSheppard/Multivariate-Time-Series-Analysis/pull/1),
commit `0ef90e954d4d7fa102158bb653e7741ee9815f48`, adds a separate rolling one-step
Ridge/persistence baseline with train-only preprocessing, standard metrics,
provenance and8 passing tests. Synthetic fixtures are software evidence only.
Feature for applied breadth with explicit re-evaluation status. Source data,
units, licensing and a fresh evaluation protocol remain required.

## Gaussian fusion notes

Base `e34ce846349bed1d338933ffea1f9fbb4d6a3f4c`; inspected notebook and Kalman
script. Notebook cell9 doubles one sensor's precision without explaining a second
independent observation; cell8 confuses precision and covariance. The Kalman script
uses identity transition dynamics on Lorenz-96 and reports fused-measurement errors
rather than filter-estimate errors. It cannot validate Lorenz filtering.

[Repair PR](https://github.com/AdamJamesSheppard/Data-Fusion/pull/1),
commit `561a6af29ea88986e9ab12eeaaf864070bc3e4f4`, adds an explicitly scoped
Gaussian utility, a derivation, limitations and8 passing analytic/property checks.
Leave accessible as historical teaching work, rather than a principal research pin.
No Gaussian method here substitutes for the current full-density DA objective.

## Reservoir/NVAR notebook

Base `1acb265323268f3b68012bef3df839f181b5e906`; inspected its code and README.
Predictor/corrector cell9 returns inside its first loop iteration, mixes derivative
components and uses a different timestep from its RK initialisation. Reported ESN
metrics span training and testing predictions and compare next-step predictions
to unshifted states. NVAR rollout comparisons also need explicit timestamp alignment.
The README already calls results preliminary; no valid comparative ranking follows
from this audit. Full rerunning/realignment of the experiment exceeds a small repair.
Remove from principal pins pending a properly specified re-evaluation, while
retaining the historical link in the portfolio. No model-training run was launched.

## Validation and unresolved scope

Three additive repair suites:24/24 local tests passed. Each PR records its actual
runtime environment, source base, limitations, original defects and self-review.
One initial time-series test attempt lacked scikit-learn; the failure and isolated
dependency remedy are retained in its validation record. GitHub CI uses separately
declared dependencies; consult actual workflow results before accepting compatibility.
PRs remain proposals until reviewed/merged. New code does not repair old evidence
retroactively. Untouched evaluation cannot be recovered by relabelling inspected data.

Method/source references are in each PR's README. Cross-cutting rationale:
[scikit-learn leakage guidance](https://scikit-learn.org/stable/common_pitfalls.html),
[time-series evaluation](https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.TimeSeriesSplit.html),
[standard regression metrics](https://scikit-learn.org/stable/api/sklearn.metrics.html),
[SciPy integration methods](https://docs.scipy.org/doc/scipy/reference/generated/scipy.integrate.solve_ivp.html),
Kevin P. Murphy, *Probabilistic Machine Learning: An Introduction*, MIT Press2022,
[linear-Gaussian/sensor-fusion context](https://probml.github.io/book1).
