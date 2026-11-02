# NBA player roles: do the 5 positions really exist?

Unsupervised learning project (K-Means + PCA) that clusters NBA players by how they play, using per-36-minute statistics, and compares the resulting groups with the official positions (PG, SG, SF, PF, C).

**Question:** do the 5 traditional positions describe how players actually play, or do they hide more (or fewer) distinct roles?

**Stack:** Python, pandas, NumPy, scikit-learn, matplotlib, Jupyter.

## Pipeline

| Notebook | Purpose | Status |
|---|---|---|
| `01_data_cleaning.ipynb` | Load the raw table, inspect it, fix its problems, save a clean version | Done |
| `02_feature_engineering.ipynb` | Filter players with too few minutes, choose and scale features | Done |
| `03_clustering.ipynb` | K-Means for several values of k, inertia and silhouette | Planned |
| `04_pca.ipynb` | Reduce to 2 dimensions to visualize and interpret the groups | Planned |
| `05_interpretation.ipynb` | Profile each cluster and compare it with the official positions | Planned |

## Data

Season 2025-26, "Per 36 Minutes" table from [Basketball-Reference](https://www.basketball-reference.com/). The data is not included in this repository.

To reproduce:
1. Open the season's *Per 36 Minutes* page, use *Share & Export* > *Get table as CSV* and save the content as `data/raw/bbref_per36_2025_26.csv`.
2. Run the notebooks in order.

## Setup

The project uses [uv](https://docs.astral.sh/uv/) to manage the environment.

```bash
uv sync
```

Then open the notebooks in VS Code or Jupyter and select the `.venv` environment as the kernel.
