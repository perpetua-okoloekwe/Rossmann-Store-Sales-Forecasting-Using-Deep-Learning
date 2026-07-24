# Rossmann Store Sales Forecasting

## Overview

This project explores time-series forecasting using the Rossmann Store Sales dataset. The objective is to predict future sales using historical store data and compare different deep learning forecasting architectures.

Models implemented:

- Baseline Forecast
- Recurrent Neural Network (RNN)
- Long Short-Term Memory (LSTM)
- Attention-Based Model
- Transformer Model

---

## Business Problem

Accurate sales forecasts can help retail businesses:

- Anticipate future demand
- Support inventory planning
- Improve resource allocation
- Assist revenue forecasting
- Support data-driven decision-making

---

## Exploratory Data Analysis (EDA)

The following analyses were conducted to understand sales patterns and business drivers:

- Average Sales by Store Type
- Average Sales by Month
- Average Sales by Day of Week
- Sales Distribution by Promotion Status
- Customer Traffic vs Sales
- Monthly Sales Trends
- Daily Sales Over Time

### Key Insights

- Sales patterns varied across store types.
- Promotions were associated with higher sales activity.
- Customer traffic showed a strong relationship with sales performance.
- Monthly and daily trends revealed seasonality and recurring demand patterns.

---

## Forecasting Approach

### Sequence Creation

- Lookback Window: 30 Days
- Forecast Horizon: 1 Day

Example:

```text
Days 1–30 → Predict Day 31
Days 2–31 → Predict Day 32
```

### Data Preparation

- Missing value treatment
- Feature engineering
- Categorical encoding
- Feature scaling
- Chronological train-test split
- Sequence generation

---

## Model Results

| Model | MAE | RMSE |
|---------|---------|---------|
| Baseline | 0.3785 | 0.4617 |
| LSTM | 0.0902 | 0.1079 |
| Transformer | 0.0767 | 0.1016 |
| Attention | 0.0801 | 0.0997 |
| RNN | **0.0602** | **0.0783** |

🏆 **Best Performing Model: RNN**

---

## Discussion

All deep learning models significantly outperformed the baseline forecast.

Under the experimental setup used in this project, the RNN achieved the best performance. However, results should be interpreted within the context of the experiment because models were trained using:

- 10,000 training sequences
- 5 training epochs
- Limited computational resources
- Minimal hyperparameter tuning

Therefore, the results represent performance under the chosen conditions rather than a definitive ranking of forecasting architectures.

---

## Project Limitations

- Reduced training dataset due to computational constraints
- Limited training epochs
- Minimal hyperparameter tuning
- Google Colab memory limitations

---

## Future Improvements

- Train using the complete dataset
- Increase training epochs
- Perform hyperparameter optimization
- Engineer additional forecasting features
- Deploy the best model using Streamlit
- Compare against traditional forecasting methods (ARIMA, Prophet, XGBoost)

---

## Key Learnings

This project provided hands-on experience with:

- Time-Series Forecasting
- Sequence Creation
- Chronological Validation
- Data Leakage Prevention
- RNNs
- LSTMs
- Attention Mechanisms
- Transformers
- Experimental Design and Model Evaluation

One of the most important lessons from this project was learning that model performance should always be interpreted within the context of the experiment.

> The question is not only: "Which model performed best?"
>
> The better question is: "Under what conditions did it perform best?"

---
## Project Structure

```text
rossmann-store-sales-forecasting/
│
├── notebooks/
│   └── Rossmann_Forecasting.ipynb
│
├── images/
│   ├── Average_Sales_By_StoreType.png
│   ├── Average_Sales_By_Month.png
│   ├── Average_Sales_By_DayOfWeek.png
│   ├── Sales_Distribution_By_Promotion_Status.png
│   ├── Customer_Traffic_Vs_Sales.png
│   ├── Monthly_Sales_Trend.png│ 
│   └── Daily_Sales_Over_Time.png
│
├── README.md
│
└── requirements.txt



---

## Reproducibility Note

During experimentation, preprocessing artifacts and trained model weights were generated in Google Colab.

These files were not preserved after the original training session ended and are therefore not included in this repository.

The complete notebook, visualizations, workflow, model architectures, evaluation results, and documentation remain available to reproduce the study.

---

## Author

**Perpetua Okoloekwe**

Data Scientist | Aspiring AI Engineer

Building in public, one project at a time. 🌱
```

## Author

**Perpetua Okoloekwe**

Data Scientist | Aspiring AI Engineer

Building in public, one project at a time. 🌱
