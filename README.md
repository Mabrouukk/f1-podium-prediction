# F1 Podium Prediction

This is our Milestone 1 project. We're trying to predict if a driver will finish in the top 3 of a race, using only what we know after qualifying (so nothing from the race itself).

We're using the Formula 1 World Championship dataset from Kaggle:
https://www.kaggle.com/datasets/rohanrao/formula-1-world-championship-1950-2020

## Team

- Mahmoud Ahmed Mabrouk Ghobashy - 58-2432
- Zain Abdullah - 58-0726
- Marawan Lasheen - 58-6465

## What's in here

- `notebooks/f1_podium_prediction.ipynb` - the main notebook, everything is in there
- `report/` - the PDF report
- `data/` - the dataset goes here (it's not on GitHub, the notebook downloads it)

## How to run it

Install the requirements:

```
pip install -r requirements.txt
```

Then open the notebook and click Run All. The first time you run it, it downloads the dataset (around 6 MB).
