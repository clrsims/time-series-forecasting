## Grocery‑Sales Forecasting | Corporación Favorita Kaggle (Python, CatBoost)
Built an end‑to‑end time‑series pipeline on ≈ 125 M daily transactions (54 stores × 33 product families)—from EDA and feature engineering to automated CSV submission.
- Engineered 40 + temporal & exogenous features (lags/rolls, promo windows, oil‑price shifts, cyclic encodings, pay‑day flags, cold‑start indicators) that cut validation RMSLE from 1.24 → 0.62 vs. linear baseline.
- Trained a CatBoost regressor with native categorical handling (store‑type, product family) and log‑transformed target; ranked top 10 % of 800 teams on the public leaderboard.
- Implemented leakage‑safe splits, deterministic seeds, and null‑imputation rules, enabling fully reproducible results across GPU/CPU hardware.
- Visualized model behavior—feature‑importance bars and RMSE‑by‑iteration plots—highlighting weekend demand spikes, holiday lift, and oil‑price sensitivity for business stakeholders.

## Dataset

The data used is from the **[Corporación Favorita Grocery Sales Forecasting](https://www.kaggle.com/competitions/favorita-grocery-sales-forecasting)** competition on Kaggle. It includes:

- `train.csv` — historical sales records  
- `test.csv` — data for forecasting  
- `stores.csv` — metadata on stores  
- `oil.csv` — daily oil prices  
- `holidays_events.csv` — national/regional holidays

## Installation

1. **Clone the repo**

   ```bash
   git clone https://github.com/clrsims/grocery-sales-forecasting.git
   cd grocery-sales-forecasting
   
2. **Install dependencies**
   
    ```bash
   pip install -r requirements.txt

3. **Download and prepare the dataset**

   a.	Folder structure should look like:

   ```bash
      grocery-sales-forecasting/
   ├── data/
   │   ├── train.csv
   │   ├── test.csv
   │   ├── stores.csv
   │   ├── holidays_events.csv
   │   └── oil.csv
   ├── forecasting_pipeline.py
   ├── requirements.txt
   └── README.md

4. **Run the notebook**
   ```bash
   jupyter notebooks
