# PJME_Forecasting
Time Series Forecasting and Model Comparison using PJME Energy Data
# Short-Term Electricity Demand Forecasting (PJM East)

A next-day electricity demand forecasting project built on hourly PJM East data. It covers data cleaning, leakage-safe feature engineering, walk-forward model validation and a Power BI dashboard for monitoring forecast accuracy.

## Business Problem
Utilities need reliable next-day demand forecasts for planning. The goal is to forecast daily demand and check whether a model genuinely beats simple baselines such as "tomorrow equals today".

## Key Results
| Metric | Result |
|---|---|
| Daily records used | 6,023 |
| Forecast error | **4.94% MAPE** |
| Improvement over baseline | **22% lower MAE** than the previous-day baseline |
| Validation | Walk-forward (time-ordered, no future data leakage) |

## Tech Stack
Python (Pandas, NumPy, scikit-learn, XGBoost, Matplotlib) | Power BI

## Approach
1. **Data cleaning**: cleaned hourly demand data and aggregated complete observations into 6,023 daily records.
2. **Feature engineering**: created calendar features, lagged-demand features and rolling statistics, built so that only past information is used for next-day forecasting (no data leakage).
3. **Models compared**: XGBoost and Linear Regression, against naive baselines (e.g. previous-day demand).
4. **Validation**: walk-forward validation, which respects time order and mimics real forecasting.
5. **Dashboard**: Power BI report comparing forecasts with actuals, monitoring accuracy, and analysing error patterns by weekday and month.

## Dashboard
[Add 1-2 screenshots of your Power BI dashboard here, e.g. `![Dashboard](images/dashboard.png)`, and upload the .pbix file or a PDF export.]

## Project Structure
```
[Replace with your actual files/folders, for example:]
├── data/            # dataset (or link to source)
├── notebooks/       # cleaning, features, modelling
├── dashboard/       # Power BI file / screenshots
└── README.md
```

## How to Run
```bash
git clone https://github.com/sanghamitrajana/Electricity-Demand-Forecasting-PJM-East.git
cd Electricity-Demand-Forecasting-PJM-East
pip install -r requirements.txt
# open the notebook and run all cells
```

## Data
[Add dataset name and source link here.]

## Author
**Sanghamitra Jana**, M.Sc. Statistics, Banaras Hindu University
[LinkedIn](https://www.linkedin.com/in/sanghamitrajana) | sanghamitra.bhu.stat27@gmail.com

