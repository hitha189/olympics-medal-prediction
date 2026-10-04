\# Olympic Medal Prediction (UE24CS352A ML Mini-Project)



Predicts how many medals each country wins at the Summer Olympics from

economic and demographic features, using a two-step model.



\*\*Team:\*\* <Hithashree S (PES1UG24CS189)>, <Jayanth Kumar P (PES1UG24CS199)>



\## Approach

1\. Classifier (Random Forest): does a country win at least one medal?

2\. Regressor (Ridge): for countries that pass, predict the medal count.

3\. Compared against a baseline Linear Regression.



\## Data (in `data/`)

\- `athlete\_events.csv`, `noc\_regions.csv`: Kaggle, "120 years of Olympic history"

\- `worldbank.csv`: World Bank World Development Indicators (GDP, population, land area)



\## How to run

1\. Install Python 3 and the libraries:

&#x20;  pip install -r requirements.txt

2\. Start Jupyter:

&#x20;  jupyter notebook

3\. Open `notebooks/olympics.ipynb` and choose Kernel > Restart and Run All.



\## Results (2016 test set)

| Model | RMSE | MAE |

|---|---|---|

| Baseline Linear Regression | 7.55 | 4.07 |

| Two-step RandomForest + Ridge | 3.73 | 1.59 |



Chart and predictions are saved in `results/`.



\## Reference

Dobkowski, B. "2020 Summer Olympics Predictions Using Machine Learning", Stanford.

