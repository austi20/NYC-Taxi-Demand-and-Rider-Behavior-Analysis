# Setup and Reproducibility

## Environment

This project was built in Jupyter notebooks using Python 3.10+.

1. Create and activate a virtual environment.
2. Install dependencies with `pip install -r requirements.txt`.
3. Launch JupyterLab or Jupyter Notebook from the repository root.

## Dataset Access

The repository includes two data files at the project root:

- `taxi.csv`: January 2023 NYC yellow taxi trip sample used throughout the notebooks. The file is tracked with Git LFS because of its size.
- `taxi_zones.csv`: NYC Taxi and Limousine Commission zone lookup table used for mapping location IDs to zone names.

If `taxi.csv` does not download automatically after cloning, run `git lfs install` once and then `git lfs pull` from the repository root.

## Notebook Guide

- `ProjectGroup4Final.ipynb`: final integrated notebook and the recommended entry point.

For a clean portfolio review, start with `ProjectGroup4Final.ipynb`.

## Notes on Reproducibility

- The notebooks expect `taxi.csv` and `taxi_zones.csv` to remain in the repository root.
- Several plots are generated inline. If you rerun the notebooks from top to bottom, figures should reproduce without extra path configuration.
- The analysis window is restricted inside the notebook to January 1 through January 14, 2023, so results should be interpreted as a short-horizon case study rather than a full-year NYC taxi analysis.
