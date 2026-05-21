# Revenue Forecasting & Business Diagnostic Analytics
### *Data-Driven Insights for Industrial Production Planning*

## Project Overview
This repository contains an end-to-end Data Science solution for **PlantNxt**. The goal is to transform raw transactional data into a predictive and diagnostic tool for production planning. 

## Technical Stack
- **Language:** Python 3.10
- **Libraries:** Pandas, NumPy, Matplotlib, Scikit-learn, XGBoost, Holidays
- **Model:** XGBoost Regressor (Time-Series Forecasting)

## 📁 Repository Structure
The project is organized for modularity and ease of use:

* **`data/`**: Contains the raw transactional dataset (`data.csv`).
* **`notebooks/`**: The core analytical engine of the project, containing:
    1.  **`01_Data_Cleaning.ipynb`**: Data preprocessing, revenue calculation, and type handling.
    2.  **`02_EDA.ipynb`**: Exploratory analysis of weekly seasonality, holiday impacts, and account concentration.
    3.  **`03_Forecasting.ipynb`**: Implementation of the **XGBoost Regressor** for 30-day revenue prediction.
    4.  **`04_Root_Cause_Analysis.ipynb`**: Diagnostic "What-If" scenarios and deep-dives into historical anomalies.
* **`requirements.txt`**: List of Python dependencies required to run the project.
* **`.gitignore`**: Standard configuration to exclude unnecessary files and local environments.

## 📊 Methodology & Proof
### 1. Structural Shift (What-If Analysis)
A "What-If" scenario was conducted to simulate the business trajectory without Account B. The results proved that without this diversification, the company would have remained stagnant at 2022 levels (~₹1.8B/year).

### 2. Time-Series Forecasting
The **XGBoost model** utilizes:
- **Lag Features:** 1-day, 7-day, and 30-day historical revenue shifts.
- **Rolling Windows:** 7-day and 30-day moving averages and standard deviations.
- **Holiday Integration:** A custom feature flagging Indian Gazetted holidays to capture policy-driven dips.

## 🔧 Installation
To run this project locally, clone the repository and install the required packages:

```bash
git clone [https://github.com/anandvenugopal-tech/PlantNxt-DataScientist-assignment.git](https://github.com/anandvenugopal-tech/PlantNxt-DataScientist-assignment.git)
pip install pandas numpy matplotlib xgboost scikit-learn holidays
