# Formula 1 Podium Prediction (Milestone 1)

Predicts whether a driver finishes on the podium (`positionOrder <= 3`) using only information
available after qualifying and before the race starts.

Dataset: [Formula 1 World Championship (1950–2024)](https://www.kaggle.com/datasets/rohanrao/formula-1-world-championship-1950-2020)

## Team

| Name | ID |
|------|----|
| Mahmoud Ahmed Mabrouk Ghobashy | 58-2432 |
| Zain Abdullah | 58-0726 |
| Marawan Lasheen | 58-6465 |

## Structure

| Path | Contents |
|------|----------|
| `notebooks/f1_podium_prediction.ipynb` | The single run-all notebook (EDA, cleaning, questions, features, models, ablation, XAI, inference) |
| `report/` | Final PDF report |
| `data/` | Raw CSVs (downloaded automatically, not committed) |

## Running locally

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
jupyter notebook notebooks/f1_podium_prediction.ipynb
```

Then **Run All**. The first run downloads the dataset (~6 MB).

## Deadline

18 October 2026, 11:59 PM
