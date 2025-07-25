# NBA Player Performance vs Salary Capstone

**Author:** Godwin Omowele  
**Date:** July 2025  

## Project Overview  
This capstone investigates whether NBA teams get good value for the money they spend on players. By comparing on-court performance metrics (points, efficiency ratings, win shares, etc.) against 2024–25 salary data, we identify over-paid and under-paid players. The results can inform contract negotiations, free-agent signings, draft strategy, and salary-cap management.

## Repository Structure  
├── data/
│ ├── nba_player_stats_checked.csv
│ ├── advanced_player_stats_checked.csv
│ ├── nba_salary_checked.csv
│ └── merged_stats.csv ← cleaned & merged master dataset
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
│ └── model_metrics.csv
├── slides/
│ └── Capstone_Presentation.pptx
├── README.md
└── requirements.txt

## Getting Started  

1. **Clone the repo**  
   ```bash
   git clone https://github.com/gomowele/nba-value-capstone.git
   cd nba-value-capstone
2. pip install -r requirements.txt
Run the notebooks
3. Open each notebook in order under notebooks/:

01_Data_Cleaning.ipynb – raw CSV ingestion & cleaning

02_EDA.ipynb – exploratory data analysis & visualizations

03_Preprocessing_and_Training_Data_Development.ipynb – feature engineering, dummy encoding, scaling, train/test split

04_Modeling_and_Metrics.ipynb – model training (LR, RF, XGBoost), metrics generation

4. View results

Model metrics: report/model_metrics.csv

Final write-up: report/Capstone_Report.pdf

Slide deck: slides/Capstone_Presentation.pptx

Key Results
Best model: XGBoost

Test RMSE: 5.11×10⁶

Test MAE: 3.01×10⁶

Test R²: 0.774

Top insight: There remains a $2–5 M “value gap” for individual players; several high-efficiency, lower-salary players are strong targets for contract negotiations.

Next Steps
Expand to multi-season data to detect trends.

Incorporate playoff performance & injury history as additional features.

Explore ensemble stacking or neural-network approaches for improved accuracy.

Thanks for reviewing! Feel free to open an issue if you run into any problems reproducing these results.
