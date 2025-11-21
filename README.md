# doctor_research

A scaffolded repository for organizing doctoral research projects, notebooks, and experiments.

## Project Structure
- `src/`: Python modules for reusable analysis and experiment code.
- `notebooks/`: Jupyter notebooks for exploration and reporting (`.ipynb_checkpoints` are ignored).
- `data/`: Data storage separated into `raw/` (immutable source data) and `processed/` (intermediate artifacts). Keep the `.gitkeep` files so the folders remain in version control.
- `docs/`: Notes, references, and paper drafts.

## Getting Started
1. Create a virtual environment:
   ```bash
   python -m venv .venv
   source .venv/bin/activate
   ```
2. Upgrade packaging tools:
   ```bash
   pip install --upgrade pip
   ```
3. Install dependencies as they are added (e.g., `pip install -r requirements.txt`).

## Data Handling
- Never commit raw datasets; place them under `data/raw/` where they are ignored by `.gitignore`.
- Derived artifacts belong in `data/processed/` or `outputs/` (also ignored by Git).
- Document data provenance and preprocessing steps in `docs/` or notebook headers.

## Development Notes
- Use clear, well-commented notebooks with reproducible cell order.
- Prefer modular code in `src/` for logic that is reused across notebooks.
- Add tests or lightweight checks as the codebase grows to keep analyses reproducible.
