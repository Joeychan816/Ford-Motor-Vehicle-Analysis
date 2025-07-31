# 🚗 Ford Vehicle Fatal Crash Analysis

This project analyzes motor vehicle crash data from 2016 to 2024 to investigate whether driving a Ford vehicle is associated with a higher likelihood of fatal accidents. Using logistic regression models, we explore relationships between vehicle factors and fatality outcomes.

## 📂 Dataset

- **Source:** CSV file `motor.csv` uploaded via Google Colab
- **Size:** 57,207 cleaned crash records
- **Key Variables:** `FORD?`, `FATAL?`, `VEHICLE_OCCUPANTS`, `LICENSED?`, `NUMBER OF PERSONS INJURED`, `VEHICLE_AGE`, `FEMALE?`, `DAYTIME?`

## 🧼 Data Cleaning and Preparation

- Removed unnecessary columns like unique IDs and registration details
- Handled missing data and ensured consistent formatting
- Selected key variables relevant for logistic regression analysis

## 📊 Exploratory Data Analysis (EDA)

- Calculated fatality rates by vehicle type:
  - Ford vehicles: 0.00051%
  - Non-Ford vehicles: 0.0002837%
- Summary statistics and distributions of key variables

## 📈 Statistical Modeling

- **Simple Logistic Regression:** Using `FORD?` as the sole predictor for `FATAL?`
- **Multiple Logistic Regression:** Including additional predictors (`VEHICLE_OCCUPANTS`, `LICENSED?`, etc.)
- Model output includes coefficients, standard errors, p-values, and overall model fit

## ⚠️ Key Findings

- Ford vehicles show higher odds of fatal crashes (odds ratio ~1.8) but this is **not statistically significant** (p = 0.235)
- Only `DAYTIME?` showed a statistically significant relationship with fatal crashes
- Most predictors, including `FORD?`, were not statistically significant
- Important variables like car type, driving speed, and driver impairment were not included
- Reverse causality and omitted variable bias may affect interpretations

## 🚀 How to Use

1. Clone or open the notebook `Ford Logit regression.ipynb` in Google Colab
2. Upload the dataset `motor.csv` when prompted
3. Run cells to perform data loading, cleaning, logistic regression, and view results saved in `Motor_stats.txt`

## 🛠️ Technologies Used

- Python (Pandas, Statsmodels, Matplotlib, Seaborn, SciPy)
- Google Colab environment for execution

---

Feel free to explore, contribute, or raise issues for further improvements!
