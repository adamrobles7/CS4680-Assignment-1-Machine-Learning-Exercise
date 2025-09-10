# CS4680 – Assignment 1: Machine Learning Exercise
**Author:** Adam Robles  

This repo contains:
- `Assignment1.ipynb` — Jupyter notebook with analysis & code  
- `car_sales_data.csv` — dataset  

---

## Overview
The project:
1. Cleans and preprocesses car sales data.  
2. Builds a **naive baseline price estimator** (using medians).  
3. Labels each row as a *Good deal* or *Bad deal* (±$5,000 from baseline).  
4. Trains two models: **Linear Regression** and **Random Forest**.  
5. Compares model performance (MAE, RMSE, R²).  
6. Produces a final table with car details, real vs. estimated price, and deal label.

---

## Data
Columns expected in `car_sales_data.csv`:
- Manufacturer, Model, Fuel type  
- Engine size, Year of manufacture, Mileage, Price

---

## Methods
- **Cleaning:** remove symbols from numeric fields, fill missing with medians, set unknown categories to `"Unknown"`.  
- **Baseline:** median-based price estimate adjusted by engine size, year, mileage.  
- **Good/Bad Deal:** flagged if price differs by more than $5k.  
- **Models:** Linear Regression & Random Forest (`n_estimators=200`).  
- **Metrics:** MAE, RMSE, R².

## Results / Findings
- Random Forest performed the best overall — it gave lower errors (MAE, RMSE) and a higher R² compared to Linear Regression.
- Linear Regression did better than the baseline, but not as well as Random Forest.  

---

## How to Run
```bash
pip install numpy pandas scikit-learn
