# doctor_research

A scaffolded repository for organizing doctoral research projects, notebooks, and experiments with a focus on meta-learning workflows.

## Project Structure
- `src/`: Python modules for reusable analysis and experiment code.
- `notebooks/`: Jupyter notebooks for exploration and reporting (`.ipynb_checkpoints` are ignored).
- `data/`: Data storage separated into `raw/` (immutable source data) and `processed/` (intermediate artifacts). Keep the `.gitkeep` files so the folders remain in version control.
- `docs/`: Notes, references, and paper drafts.

## Getting Started
1. Create a virtual environment using Conda (works on Windows and Linux):
   ```bash
   conda env create -f environment.yml
   conda activate doctor-research
   ```
2. Upgrade packaging tools (optional but recommended):
   ```bash
   python -m pip install --upgrade pip
   ```
3. Install additional dependencies as needed (e.g., `pip install -r requirements.txt`).

## Data Handling
- Never commit raw datasets; place them under `data/raw/` where they are ignored by `.gitignore`.
- Derived artifacts belong in `data/processed/` or `outputs/` (also ignored by Git).
- Document data provenance and preprocessing steps in `docs/` or notebook headers.

## Meta-Learning Workflow
- Use the Conda environment for consistent packages on Windows and Linux.
- Keep reusable training, evaluation, and data utilities in `src/` for sharing across notebooks.
- Store experiment runs (configs, metrics, plots) under `docs/` or `data/processed/` as appropriate.

## Development Notes
- Use clear, well-commented notebooks with reproducible cell order.
- Prefer modular code in `src/` for logic that is reused across notebooks.
- Add tests or lightweight checks as the codebase grows to keep analyses reproducible.
