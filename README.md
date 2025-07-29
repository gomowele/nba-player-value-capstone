# NBA Player Performance vs Salary — Capstone Two  
**Author:** Godwin Omowele | **Date:** July 2025  

---

## Project Overview  

Do NBA teams really get value for the money they spend on players?  
I predict a player’s *fair* 2024-25 salary directly from 2023-24 performance metrics (PTS, VORP, Win Shares, etc.).  
Contracts that diverge sharply from the model’s estimate are flagged as **over-paid** or **under-paid** — insights GMs can use in negotiations, free-agency, and cap management.

---

## Repository Structure  

.
├── data/
│ ├── nba_player_stats_checked.csv
│ ├── advanced_player_stats_checked.csv
│ ├── nba_salary_checked.csv
│ └── merged_stats.csv # cleaned & merged master set
├── figures/
│ ├── salary_raw_vs_log.png
│ ├── xgb_feature_importance.png
│ └── xgb_actual_vs_pred.png
├── notebooks/
│ ├── 01_Data_Cleaning.ipynb
│ ├── 02_EDA.ipynb
│ ├── 03_Preprocessing_and_Training_Data_Development.ipynb
│ └── 04_Modeling_and_Metrics.ipynb
├── processed/
│ ├── X_train.csv
│ ├── X_test.csv
│ ├── y_train.csv
│ └── y_test.csv
├── report/
│ ├── Capstone_Report.md
│ ├── Capstone_Report.pdf
│ ├── model_metrics_raw.csv
│ └── model_metrics_log.csv
├── slides/
│ └── Capstone_Final_Presentation_v4.pptx
├── README.md ← you are here
└── requirements.txt

---

## Getting Started  

```bash
# 1) Clone the repo
git clone https://github.com/gomowele/nba-value-capstone.git
cd nba-value-capstone

# 2) Install deps
pip install -r requirements.txt
Run the notebooks
Order matters – execute each notebook top-to-bottom.

01_Data_Cleaning.ipynb — raw CSV ingestion & cleaning

02_EDA.ipynb — histograms, correlations, salary skew

03_Preprocessing_and_Training_Data_Development.ipynb — dummy encoding, scaling, train/test split

04_Modeling_and_Metrics.ipynb — SelectKBest(40), Linear Reg, RF, XGBoost, log-salary variant

View Results
Model metrics — report/model_metrics_log.csv (log-target) & report/model_metrics_raw.csv

Final write-up — report/Capstone_Report.pdf

Slide deck — slides/Capstone_Final_Presentation_v4.pptx

Key Results (log-target XGBoost)
Metric	Test Value
RMSE	$ 0.42 M
MAE	$ 0.19 M
R²	0.999

Typical error ≈ 3 % of an average NBA salary (~$13 M).

Insight
There is a $2–5 M value gap on several rotation-level players.
Teams can renegotiate or acquire these players below market to gain cap flexibility.

Next Steps
Add multi-season and playoff metrics to capture consistency and clutch value.

Incorporate injury history to penalise risky long-term deals.

Deploy a SHAP-powered dashboard so front-office analysts can explain each prediction.

Thanks for checking out the project!



