# Household Power Consumption - Machine Learning Analysis

This project applies various regression models to predict **Global Active Power** using the `household_power_data.csv` dataset. The notebook demonstrates preprocessing, training, evaluation, and comparison of model performance using metrics like RMSE, MAE, and R².

---

## 📂 Dataset

The dataset used is `household_power_data.csv`, containing time series data of household electricity consumption.  
Key features include:

- `Global_active_power` (target)
- `Global_reactive_power`
- `Voltage`
- `Global_intensity`
- `Sub_metering_1`, `Sub_metering_2`, `Sub_metering_3`
- `Datetime` (ignored in model training)

---

## ⚙️ Workflow

1. **Data Cleaning**  
   - Drop missing target values  
   - Impute missing feature values using mean strategy

2. **Data Sampling**  
   - Randomly select 100,000 rows to reduce memory load

3. **Preprocessing**  
   - Drop datetime column  
   - Apply one-hot encoding (if any categorical variables)  
   - Scale numeric features with `StandardScaler`

4. **Model Training**  
   Models used:
   - Linear Regression (`sklearn.linear_model`)
   - Random Forest Regressor (`sklearn.ensemble`)
   - Gradient Boosting Regressor (`sklearn.ensemble`)

5. **Evaluation Metrics**  
   - RMSE (Root Mean Squared Error)  
   - MAE (Mean Absolute Error)  
   - R² Score

---

## 📊 Sample Output

```text
🌲 Random Forest Performance:
RMSE: 0.2853
MAE: 0.1451
R-squared: 0.8420

🌟 Gradient Boosting Performance:
RMSE: 0.2786
MAE: 0.1423
R-squared: 0.8512
