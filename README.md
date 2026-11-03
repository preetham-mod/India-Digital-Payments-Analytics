# India's Digital Payments Transformation: A Data-Driven Analysis (2019–2026)

## Project Overview

This project analyses the growth and evolution of three major digital payment systems in India:

- Unified Payments Interface (UPI)
- Immediate Payment Service (IMPS)
- National Electronic Funds Transfer (NEFT)

Using monthly data from November 2019 to August 2026, the project examines transaction volume, transaction value, growth patterns, payment-system composition and future trends.

The project applies Python-based data analytics, exploratory data analysis, statistical methods and time-series forecasting to understand the changing characteristics of India's digital payment landscape.

## Problem Statement

The rapid expansion of digital payments has transformed India's financial ecosystem. However, different payment systems serve different transaction requirements and exhibit distinct patterns in transaction frequency and monetary value.

This project investigates how UPI, IMPS and NEFT have evolved, how their relative contributions have changed, and what historical trends suggest about future UPI transaction activity.

## Project Objectives

1. Analyse monthly transaction volume and value across UPI, IMPS and NEFT.
2. Measure historical growth using percentage changes and compound annual growth rates.
3. Compare transaction characteristics across the three payment systems.
4. Examine changes in transaction-volume and transaction-value composition.
5. Develop and evaluate time-series forecasting models for UPI volume and value.
6. Present findings through statistical analysis and visualisations.

## Dataset

**Source:** Reserve Bank of India (RBI), Database on Indian Economy (DBIE), Payment System Indicators.

**Study period:** November 2019 – August 2026.

**Frequency:** Monthly.

**Observations:** 82.

### Variables

| Variable | Description |
|---|---|
| Date | Monthly observation date |
| IMPS_Volume_Lakh | IMPS transaction volume |
| IMPS_Value_Crore | IMPS transaction value |
| NEFT_Volume_Lakh | NEFT transaction volume |
| NEFT_Value_Crore | NEFT transaction value |
| UPI_Volume_Lakh | UPI transaction volume |
| UPI_Value_Crore | UPI transaction value |

## Tools and Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Statsmodels
- Jupyter Notebook

## Methodology

The project follows a structured analytical workflow:

1. Data extraction and preparation.
2. Data cleaning and validation.
3. Descriptive statistical analysis.
4. Exploratory data analysis and trend visualisation.
5. Growth-rate and CAGR calculations.
6. Comparative payment-system analysis.
7. Average transaction-size analysis.
8. Payment-volume and payment-value composition analysis.
9. Time-series forecasting and model evaluation.
10. Residual diagnostics and interpretation.

### Forecasting Approach

Seasonal ARIMA (SARIMA) models were evaluated for UPI transaction volume and value.

Model selection used expanding-window rolling-origin validation.

The selected models were:

- **UPI Volume:** SARIMA(0,1,0)(1,0,0,12)
- **UPI Value:** SARIMA(1,1,0)(1,0,0,12)

Performance was evaluated using:

- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- Symmetric Mean Absolute Percentage Error (sMAPE)

## Key Findings

- UPI recorded the strongest historical growth in both transaction volume and value among the three systems.
- UPI accounted for an average 87.34% of their combined monthly transaction volume.
- NEFT accounted for an average 64.58% of their combined monthly transaction value.
- NEFT exhibited the highest volume-weighted average transaction size, followed by IMPS and UPI.
- The composition of transaction activity shifted considerably towards UPI over the study period.

### Forecasting Results

| Indicator | Selected model | MAE | RMSE | sMAPE |
|---|---|---:|---:|---:|
| UPI Volume | SARIMA(0,1,0)(1,0,0,12) | 3,713.66 | 4,588.37 | 2.25% |
| UPI Value | SARIMA(1,1,0)(1,0,0,12) | 64,082.32 | 73,940.07 | 2.76% |

The forecasting exercise projects continued growth in UPI transaction activity over September 2026–August 2027.

**Note:** The selected models retain residual autocorrelation, non-normality and heteroskedasticity. Forecasts should therefore be interpreted cautiously.

## Repository Structure

```text
India-Digital-Payments-Analytics/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   ├── 01_data_understanding.ipynb
│   └── 02_exploratory_data_analysis.ipynb
│
├── visualisations/
│
├── reports/
│   └── India_Digital_Payments_Analytics_Report.docx
│
├── README.md
├── requirements.txt
└── .gitignore
```

## How to Run the Project

### 1. Clone the repository

```bash
git clone <YOUR_GITHUB_REPOSITORY_URL>
```

### 2. Navigate to the project folder

```bash
cd India-Digital-Payments-Analytics
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open the notebooks in the following order:

1. `01_data_understanding.ipynb`
2. `02_exploratory_data_analysis.ipynb`

Ensure the datasets are stored in their corresponding project folders before executing the notebooks.

## Limitations

- The analysis covers only UPI, IMPS and NEFT, not the entire Indian payments ecosystem.
- The dataset contains aggregate monthly observations rather than individual transactions.
- The analysis identifies historical patterns and associations, not causal relationships.
- Forecasting performance may change as new observations become available.
- Residual diagnostic results indicate that the selected forecasting models do not capture all time-series characteristics.

## Author

**Preetham**

Data Analytics | Statistical Analysis | Financial Analytics | Time-Series Forecasting

## Disclaimer

This project is intended for educational, analytical and portfolio demonstration purposes. Findings and forecasts should not be interpreted as official RBI forecasts or financial advice.

The dataset is attributed to the Reserve Bank of India. Refer to the original RBI source for data definitions and applicable reuse conditions.
