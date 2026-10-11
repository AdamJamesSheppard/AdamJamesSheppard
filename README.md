<p align="center">
  <img src="https://raw.githubusercontent.com/AdamJamesSheppard/AdamJamesSheppard/main/assets/research-banner.svg" alt="Adam James Sheppard — scientific computing, probability and machine learning. Abstract geometric artwork." width="100%" />
</p>

# Adam James Sheppard

I work on scientific computing and machine learning for dynamical systems, with a focus on probability densities, numerical methods and data assimilation.

My current research asks how a learned forecast operator can propagate a complete probability density for the Lorenz system, and what evidence is needed before that surrogate can be trusted in Bayesian data assimilation.

### Current research

**[Lorenz Fokker–Planck & operator learning](https://github.com/AdamJamesSheppard/lorenz-training-set)**

A research programme connecting finite-element probability-density evolution with operator-learning qualification. The numerical work includes discontinuous Galerkin methods, positivity constraints, full diffusion tensors and locally refined hexahedral meshes.

The operator-learning stage is in progress. An end-to-end neural pilot has demonstrated data-generation and GPU-training feasibility; statistical fidelity, reference applicability and surrogate qualification remain open. The eventual assimilation method is a full-density Bayesian update, without imposing a Gaussian or Gaussian-mixture state approximation.

[Programme and evidence](https://github.com/AdamJamesSheppard/lorenz-training-set/tree/main/docs/operator_learning) · [Research integrity](https://github.com/AdamJamesSheppard/lorenz-training-set/blob/main/SCIENTIFIC_INTEGRITY.md)

### Research portfolio

These projects show the range of my work, with their evidence status made explicit.
The older studies are exploratory; a [code and research-quality review](QUALITY_REVIEW.md)
records limitations and proposed repairs. Listing a project here does not imply
that its scientific conclusions have been independently validated.

- **[Lorenz datasets in C++](https://github.com/AdamJamesSheppard/Lorenz-Atrractor-Revisited-C-)** — trajectory-generation work, with a [tested deterministic integrator proposed for review](https://github.com/AdamJamesSheppard/Lorenz-Atrractor-Revisited-C-/pull/1). The historical generator has correctness defects.
- **[Multivariate time-series analysis](https://github.com/AdamJamesSheppard/Multivariate-Time-Series-Analysis)** — Madrid air-quality exploration, with a [train-only chronological baseline proposed for review](https://github.com/AdamJamesSheppard/Multivariate-Time-Series-Analysis/pull/1). Historical scores need re-evaluation.
- **[Learning chaotic dynamics](https://github.com/AdamJamesSheppard/Echo-State-Networks-Nonlinear-Vector-Autoregression-and-Data-Assimilation-for-Chaotic-Systems)** — historical reservoir-computing and nonlinear autoregressive experiments. Forecast alignment and out-of-sample evaluation require repair before strong comparisons.
- **[Bayesian data-fusion notes](https://github.com/AdamJamesSheppard/Data-Fusion)** — Gaussian teaching examples, with a [sensor-accounting correction proposed for review](https://github.com/AdamJamesSheppard/Data-Fusion/pull/1). Separate from the full-density formulation of the current research.

### How I approach the work

Define the scientific question. Preserve competing explanations. Test against strong baselines. Record assumptions, failed experiments and the limits of each claim.

I distinguish mathematical proof, numerical verification and empirical evidence. A successful software run is one part of the argument; application qualification requires more.

**Tools across these projects:** Python · C++ · Jupyter · finite elements · numerical optimisation · neural operators

---

Earlier repositories remain available as a research history. Their methods and conclusions should be read in the context of each experiment; they do not automatically describe the current programme.
