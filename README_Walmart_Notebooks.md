# Walmart Income Classification & Customer Segmentation — Notebooks README

This repository includes two Jupyter notebooks that address related but independent tasks using a census‑style dataset.
Both notebooks can be run separately and do **not** depend on each other.

---

## Notebooks

### 1) `Walmart_50000Classifier.ipynb`
- **Goal:** Train a binary classifier to predict whether an individual's annual income exceeds a threshold (e.g., $50,000).
- **What it does:** Loads data, performs cleaning/encoding, splits into train/validation/test, fits a baseline and one or more models, and reports standard evaluation results.
- **You can customize:** data path, target column, feature lists, encoding choices, and model hyperparameters.
- **Output:** Shows results in‑notebook and may optionally save lightweight artifacts (e.g., metrics, plots, or predictions) if paths are enabled.

### 2) `Walmart_Kmeans_F.ipynb`
- **Goal:** Create customer segments via clustering for marketing and analytics use cases.
- **What it does:** Loads data, handles preprocessing, runs clustering over a chosen range of cluster counts, and summarizes segments with simple profiles.
- **You can customize:** data path, selected features, number of clusters, random seeds, and basic profiling settings (e.g., which attributes to display).
- **Output:** Presents segment overviews in‑notebook and may optionally write small helper files (e.g., assignments or summaries) if configured.

> If your dataset includes a sampling **weight** column (e.g., from CPS), it should generally **not** be used as a predictive feature. It can be applied when computing descriptive summaries or segment proportions.

---

## Requirements

- Python 3.9+
- pandas, numpy, scikit‑learn, matplotlib  
- (Optional) seaborn for EDA/plots

Install (one time):
```bash
pip install pandas numpy scikit-learn matplotlib seaborn
```

---

## Data

- Place your data file(s) in the same directory as the notebooks, or update the file paths in the first configuration cell.
- Ensure columns are correctly typed (categorical vs. numeric) so that preprocessing and modeling behave as expected.

---

## How to Run

1. Start Jupyter and open either notebook:
   ```bash
   jupyter lab
   # or
   jupyter notebook
   ```
2. Review the **Parameters/Config** cell at the top; adjust paths and settings as needed.
3. Run cells **top to bottom**.

---

## Suggested Layout (example)

```
project/
├─ Walmart_50000Classifier.ipynb
├─ Walmart_Kmeans_F.ipynb
├─ data/                     # raw or cleaned data (optional)
└─ outputs/                  # artifacts if you enable saving (optional)
```

---

## Notes

- These notebooks are intended as starting points. You can integrate additional models, distance metrics, or profiling logic as your use case evolves.
