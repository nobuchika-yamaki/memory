README
Overview

This repository contains the complete simulation and analysis code used in the manuscript
“Dissipative dynamics stabilize recurrent neural computation under noise” (submitted to PLOS Computational Biology).

The code reproduces all results reported in the paper, including task performance, uncertainty estimates, statistical tests, baseline comparisons, and internal dynamical analyses.

Implemented models

Continuous-time recurrent neural network with position–momentum states (q, p)

Reversible dynamics (γq = γp = 0)

Dissipative dynamics (γq = γp > 0)

Baseline models

Echo State Network (ESN)

Leaky integrator RNN

All models are evaluated using identical inputs, noise levels, and linear readout training.

Tasks

Attractor-memory retrieval
Pattern recall under initial-state noise.

Sequence tracking
Externally driven transitions between stored patterns under ongoing noise.

Nonlinear input–output mapping
Reservoir computation task with target
f(x) = sin(πx₁) cos(πx₂), evaluated under ongoing noise.

Internal dynamics analysis

Trial-to-trial variance of internal activity

Autocorrelation decay time (1/e criterion)

Statistical analysis

n = 50 independent trials per condition

95% confidence intervals via nonparametric bootstrap

Welch’s t-test, Fisher’s exact test

Effect size: Cohen’s d

Multiple-comparison correction: Holm–Bonferroni

Figures and tables

Figure 1: Input–output mapping performance (MSE) across models

Figure 2: Trial-to-trial internal variability

Figure 3: Autocorrelation decay of internal activity

Table 1: Summary of all task-level and internal-dynamics results

Requirements

Python ≥ 3.9

NumPy

SciPy

Matplotlib# memory

Notes

All parameters (network size, timestep, noise levels, dissipation constants) exactly match those reported in the manuscript.

No hyperparameter tuning is performed across conditions.

Random seeds are fixed for full reproducibility.
