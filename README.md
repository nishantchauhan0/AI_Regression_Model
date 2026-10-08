# Yes Bank Stock Closing Price Prediction (Regression Model)

An end-to-end Machine Learning regression project to predict the monthly closing stock price of **Yes Bank** using historical financial data (July 2005 – November 2020).

---

## 📌 Project Overview

Yes Bank has been one of the most prominent private sector banks in India. Due to major events and transitions around 2018–2020, the stock experienced extreme volatility, rising from ~₹12 in 2005 to a peak close of ~₹368 in July 2018, followed by a drastic fall. 

This project explores historical monthly stock prices, performs exploratory data analysis (EDA), treats skewness and multicollinearity, and evaluates multiple regression models to predict closing prices.

---

## 📊 Dataset Description

The dataset contains monthly stock prices of Yes Bank from **July 2005 to November 2020** (185 records):
- **Date**: Month and year of the observation.
- **Open**: Opening stock price for the month.
- **High**: Highest price recorded during the month.
- **Low**: Lowest price recorded during the month.
- **Close**: Final closing price of the stock for the month (Target variable).

---

## 🛠️ Key Steps & Methodology

1. **Exploratory Data Analysis (EDA):**
   - Trend and distribution analysis across the timeline.
   - Identified significant positive skewness and handled it via log transformation.
   - Evaluated multicollinearity using Correlation Heatmaps and Variance Inflation Factor (VIF).

2. **Feature Engineering & Preprocessing:**
   - Log transformation on features and target variable.
   - Train-test split (and time-series chronological validation).
   - Standard scaling for feature normalization.

3. **Model Training & Evaluation:**
   - **Linear Regression**
   - **Ridge Regression** (with hyperparameter tuning via GridSearchCV)
   - **Random Forest Regressor** (tuned)
   - **Gradient Boosting Regressor** (tuned)

---

## 📈 Model Performance & Results

Evaluation on the test dataset (original price scale):

| Model | Test $R^2$ | MAE (₹) | RMSE (₹) | MAPE (%) |
| :--- | :---: | :---: | :---: | :---: |
| **Linear Regression** | **0.9912** | **5.52** | **8.93** | **6.5%** |
| **Ridge Regression (Tuned)** | **0.9912** | **5.52** | **8.93** | **6.5%** |
| **Random Forest Regressor** | 0.9823 | 8.00 | 12.66 | 10.2% |
| **Gradient Boosting Regressor** | 0.9798 | 8.67 | 13.50 | 10.9% |

> **Final Selected Model:** **Ridge / Linear Regression** achieved the highest $R^2$ score (0.9912) and lowest RMSE/MAE, demonstrating minimal overfitting and robust generalizability.

---

## 📁 Repository Structure

```text
├── data_YesBank_StockPrices.csv         # Historical stock price dataset
├── Yes_Bank_Stock_Price_Regression.ipynb # Full Jupyter notebook with EDA & models
├── Yes_Bank_Code_Explanation.docx       # Detailed technical documentation & report
├── .gitignore                           # Git ignore rules
└── README.md                            # Project documentation
```

---

## 🚀 How to Run

1. Clone this repository:
   ```bash
   git clone <REPO_URL>
   cd AI_Regression_Model
   ```

2. Install dependencies:
   ```bash
   pip install numpy pandas matplotlib seaborn scikit-learn
   ```

3. Open and run the Jupyter Notebook:
   ```bash
   jupyter notebook Yes_Bank_Stock_Price_Regression.ipynb
   ```
