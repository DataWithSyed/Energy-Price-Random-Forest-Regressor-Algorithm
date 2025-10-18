# Energy Price Forecasting - Random Forest Regressor Algorithm

This repository contains a **conceptual example** of forecasting **energy market prices** using **machine learning** techniques. The project demonstrates data preprocessing, feature engineering, and price prediction using a **Random Forest Regressor**, along with result visualization for comparison between actual and predicted prices.

> **Note:** The dataset used in this project (`market_data.csv`) contains confidential energy market information and **cannot be shared publicly**. Therefore, this repository includes **only the source code**, not the dataset.

---

## 📘 Project Overview

Energy price forecasting is crucial for energy traders, utilities, and policymakers to make informed operational and strategic decisions.
This project showcases how time series data (such as demand, renewable generation, and historical prices) can be used to build a predictive model for short-term energy price forecasting.

---

## 🧠 Workflow Summary

### 1. **Data Loading**

The project expects a CSV file named `market_data.csv` containing historical data with columns such as:

* `Date` – Timestamp of the observation
* `Price` – Historical market price of energy
* `Demand` – Energy consumption or demand data
* `Renewable_Generation` – Contribution from renewable sources

> ⚠️ Since the data is private, the code includes a safety check to prevent execution if the file is not found.

### 2. **Feature Engineering**

* Converts `Date` column to datetime format and sets it as the index.
* Creates **lagged features** (e.g., previous day’s price) to capture time dependencies.
* Removes missing values to ensure model stability.

### 3. **Model Definition**

* Uses a **Random Forest Regressor** from `scikit-learn` as a baseline predictive model.
* Features: `Price_lag1`, `Demand`, `Renewable_Generation`
* Target: `Price`

### 4. **Training and Testing**

* Splits the dataset into **80% training** and **20% testing** sets (time-based, no shuffling).
* Fits the model on training data and evaluates it on test data.

### 5. **Prediction and Visualization**

* Predicts energy prices for the test set.
* Visualizes **actual vs predicted prices** using `matplotlib` to assess performance visually.

---

## 📊 Example Visualization

The script produces a plot comparing actual and predicted prices over time:

```
Energy Price Forecasting
│
├── Actual Prices (Solid Line)
└── Predicted Prices (Dashed Line)
```

This helps assess how well the model captures short-term market movements.

---

## 🛠️ Technologies Used

* **Python 3.x**
* **Pandas** – Data manipulation and preprocessing
* **Scikit-learn** – Machine learning and model training
* **Matplotlib** – Data visualization

---

## ⚙️ How to Use

1. **Clone this repository:**

   ```bash
   git clone https://github.com/yourusername/Energy-Price-Forecasting.git
   cd Energy-Price-Forecasting
   ```

2. **Install dependencies:**

   ```bash
   pip install pandas scikit-learn matplotlib
   ```

3. **Provide your own dataset:**
   Save your CSV file as `market_data.csv` in the project directory with the following columns:

   ```
   Date, Price, Demand, Renewable_Generation
   ```

4. **Run the script:**

   ```bash
   python forecast_energy_price.py
   ```

---

## 🚫 Data Availability

> **Important:**
> The dataset used in this analysis is confidential and **cannot be shared**.
> This repository is intended for educational and demonstration purposes, showcasing the methodology and workflow rather than the actual data.

---

## 📈 Future Enhancements

* Integrate **LSTM** or **XGBoost** for improved time-series forecasting accuracy.
* Include **error metrics** (MAE, RMSE, MAPE) for quantitative evaluation.
* Add **hyperparameter tuning** for optimal model performance.
* Deploy as a **web dashboard** using Streamlit or Dash for real-time prediction visualization.

---

## 🧩 Author

**Syed Muhammad Taha Nasir**
Data Analyst | Energy Analyst | Machine Learning & Computer Vision Enthusiast
🔗 [GitHub: DataWithSyed](https://github.com/DataWithSyed)

---

