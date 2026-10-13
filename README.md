# F1 Podium Prediction

This is our Milestone 1 project. We predict whether a driver will finish in the top 3 of a race, using only what we know after qualifying (so nothing from the race itself).

We're using the Formula 1 World Championship dataset from Kaggle (version 24, 1950–2024):
https://www.kaggle.com/datasets/rohanrao/formula-1-world-championship-1950-2020

## Team

- Mahmoud Ahmed Mabrouk Ghobashy - 58-2432
- Zain Abdullah - 58-0726
- Marawan Lasheen - 58-6465
- Omar Salah - 58-6370

## What's in here

- `notebooks/f1_podium_prediction.ipynb` - the main notebook, everything is in there
- `report/F1_Podium_Prediction_Report.pdf` - the analytical report
- `report/report.md` - the report source
- `report/figures/` - every figure, saved by the notebook when it runs
- `data/` - the dataset goes here (it's not on GitHub, the notebook downloads it). The notebook also saves the final modeling table here as `modeling_table.csv`

## Results in one paragraph

After cleaning (sentinels, typing, key checks, shared-drive duplicates, non-starters, Indianapolis 500) we built one row per driver per race with 20 leakage-safe features (grid, qualifying, driver form, constructor form, standings before the race, field size). We trained on 1981–2019, validated on 2020–2021 and tested once on 2022–2024. The final model (tuned logistic regression) gets **PR-AUC 0.722, F1 0.669, ROC-AUC 0.937** on the test seasons, against PR-AUC 0.647 for the rule "the top 3 on the grid finish on the podium". Random forest, gradient boosting and a shallow neural network were statistically indistinguishable from it.

## How to run it

Install the requirements:

```
pip install -r requirements.txt
```

Then open the notebook and click Run All. The first time you run it, it downloads the dataset (around 6 MB). A full run takes about a minute on a laptop.

On Kaggle: add the dataset as an input and Run All. The notebook finds it under `/kaggle/input` by itself.
