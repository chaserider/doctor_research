# Project Setup

This document summarizes how to configure the repository for meta-learning experiments on both Windows and Linux using Conda.

## Environment Creation
1. Install [Miniconda](https://docs.conda.io/en/latest/miniconda.html) or [Anaconda](https://www.anaconda.com/) for your platform.
2. Create the environment from the included spec:
   ```bash
   conda env create -f environment.yml
   conda activate doctor-research
   ```
3. Register the kernel for notebooks (optional when using JupyterLab inside the environment):
   ```bash
   python -m ipykernel install --user --name doctor-research
   ```
4. Keep dependencies synchronized across OSes by updating `environment.yml` whenever you add new packages.

## Folder Conventions
- `src/`: shared Python utilities for data loading, training loops, evaluation, and configuration.
- `notebooks/`: exploratory notebooks; keep them lightweight and prefer calling functions from `src/`.
- `data/raw/`: immutable source data (ignored by Git).
- `data/processed/`: intermediate artifacts such as features or preprocessed datasets.
- `docs/`: experiment notes, papers, and configuration references.

## Meta-Learning Tips
- Start with small benchmark datasets to validate pipelines before scaling up.
- Track experiments (metrics, hyperparameters, random seeds) so they are reproducible on both Windows and Linux.
- Prefer deterministic settings when possible (e.g., setting `torch` seeds and `cudnn` flags) to reduce cross-platform differences.
- Keep computationally intensive code paths behind configuration flags so they can be toggled per machine capability.
