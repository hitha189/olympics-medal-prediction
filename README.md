# Olympic Medal Prediction

UE24CS352A Machine Learning Mini-Project

Predicts how many medals each country wins at the Summer Olympics from
economic and demographic features, using a two-step model.

**Team:** Hithashree S (PES1UG24CS189), Jayanth Kumar P (PES1UG24CS199)

## Approach

1. A Random Forest classifier decides whether a country wins at least one medal.
2. A Ridge regressor predicts the medal count for the countries that pass.
3. Both steps are compared against a baseline Linear Regression.

The approach is based on: Dobkowski, B., "2020 Summer Olympics Predictions Using Machine Learning", Stanford.

## Data (in `data/`)

- `athlete_events.csv`, `noc_regions.csv`: Kaggle, "120 years of Olympic history: athletes and results"
- `worldbank.csv`: World Bank World Development Indicators (GDP, population, land area)

## Project structure

- `notebooks/olympics.ipynb`: all code (cleaning, merging, models, evaluation)
- `results/`: final chart and 2016 predictions
- `requirements.txt`: Python libraries needed

## How to run

1. Install Python 3 and the libraries:

```
pip install -r requirements.txt
```

2. Start Jupyter:

```
jupyter notebook
```

3. Open `notebooks/olympics.ipynb` and choose **Kernel > Restart Kernel and Run All Cells**.

## Results (2016 test set)

| Model | RMSE | MAE |
|---|---|---|
| Baseline Linear Regression | 7.55 | 4.07 |
| Two-step Random Forest + Ridge | 3.73 | 1.59 |

The model was trained on 1992-2012 and tested on 2016.
The chart and predictions are saved in `results/`.
