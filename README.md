# Bitcoin-Market-Sentiment-vs-Trader-Behavior-Analysis
This project analyzes how Bitcoin market sentiment (Fear vs Greed) influences trader behavior and performance using historical trading data. 

By combining market sentiment indicators with historical trader data, the analysis explores whether traders change their behavior and profitability depending on the overall market mood.

The project focuses on:

Trader profitability during Fear vs Greed periods

Behavioral changes such as trade frequency, position size, and long/short bias

Identifying different types of traders using behavioral segmentation

Proposing simple strategy rules based on the findings

# Problem Statement

Financial markets are heavily influenced by investor emotions. Fear and Greed often drive market movements, but their impact on individual trader behavior is less understood.

This project aims to answer the following questions:

1. Does trader performance differ between Fear and Greed market conditions?
2. Do traders change their behavior based on market sentiment?
3. Can trader profitability be predicted using behavioral and sentiment-based features?

---

# Dataset Description

The analysis combines:

### Trading Data

* Trade timestamps
* Trade direction (Long/Short)
* Trade size
* Profit and Loss (PnL)
* Trader activity records

### Market Sentiment Data

Daily sentiment labels:

* Fear
* Greed

The sentiment dataset was merged with trading records to evaluate trader behavior under different market conditions.

---

# Methodology

## 1. Data Cleaning

The following preprocessing steps were performed:

* Removed duplicate records
* Checked and handled missing values
* Converted timestamps into datetime format
* Aggregated records at daily granularity

---

## 2. Data Integration

Trading activity was merged with daily sentiment classifications to create a unified dataset for behavioral analysis.

This enabled direct comparison of trader performance during Fear and Greed periods.

---

## 3. Feature Engineering

Several behavioral metrics were generated:

* Daily Profit and Loss (PnL)
* Win Rate
* Average Trade Size
* Trade Frequency
* Long vs Short Ratio
* Trader Profitability Metrics
* Sentiment-Based Trading Features

These features were used for both analysis and machine learning.

---

## 4. Behavioral Analysis

The project evaluates how trader behavior changes across sentiment regimes.

Key areas examined:

* Profitability during Fear vs Greed
* Trading activity levels
* Position sizing decisions
* Directional bias (Long vs Short)
* Risk-taking behavior

---

## 5. Trader Segmentation

Traders were grouped using behavioral characteristics such as:

* Average trade size
* Profitability
* Win rate
* Trading frequency

Clustering techniques were applied to identify distinct trader archetypes and behavioral patterns.

---

# Machine Learning Model

A classification model was developed to predict trade profitability.

### Model Used

* Random Forest Classifier

### Implementation

```python
from sklearn.ensemble import RandomForestClassifier
from sklearn.metrics import accuracy_score

model = RandomForestClassifier()

model.fit(X_train, y_train)

predictions = model.predict(X_test)

print("Accuracy:", accuracy_score(y_test, predictions))
```

### Performance

| Metric   | Score  |
| -------- | ------ |
| Accuracy | 66.01% |

The model demonstrates that sentiment and behavioral features contain predictive information regarding trading outcomes.

---

# Visualizations

The project includes several analytical visualizations.

### Performance Analysis

* PnL Distribution During Fear vs Greed
* Average PnL Comparison
* Win Rate Comparison

### Behavioral Analysis

* Trade Frequency Across Sentiment Regimes
* Position Size Changes
* Long vs Short Bias by Sentiment

### Advanced Visualizations

* PnL Heatmap by Sentiment and Trade Direction
* Trader Behavior Map (Risk vs Profitability)
* Trading Activity Trends Over Time

These visualizations provide evidence-based insights into trader decision-making.

---

# Key Findings

### Sentiment Influences Profitability

Trader profitability varies significantly across Fear and Greed periods.

### Behavioral Shifts Are Observable

Traders modify:

* Trade frequency
* Position sizing
* Directional bias

based on prevailing market sentiment.

### Risk-Taking Increases During Greed

Periods of Greed often correspond with larger position sizes and more aggressive trading behavior.

### Defensive Behavior During Fear

Fear-driven markets encourage more cautious trading activity and reduced risk exposure.

### Predictive Potential

Behavioral and sentiment-based features can be leveraged to predict trade profitability with moderate accuracy.

---

# Trading Strategy Insights

## Sentiment-Aware Risk Management

### During Fear Markets

* Reduce position size
* Prioritize capital preservation
* Avoid excessive trading

### During Greed Markets

* Monitor overconfidence risk
* Maintain disciplined position sizing
* Avoid emotional decision-making

---

## Behavior-Aware Trading Discipline

Different trader types may benefit from different approaches:

### Frequent Traders

* Reduce overtrading during volatile Fear periods

### Consistent Winners

* Maintain disciplined strategies
* Increase activity selectively during strong momentum phases

Combining sentiment indicators with behavioral analysis can improve trading decisions and risk management.

---

# Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook

---

# Future Improvements

* Experiment with XGBoost and LightGBM
* Incorporate additional market indicators
* Build a real-time sentiment-aware trading dashboard
* Improve predictive performance using ensemble methods
* Explore deep learning approaches for profitability prediction

---

# Conclusion

This project demonstrates that market sentiment significantly affects trader behavior and performance. By integrating sentiment indicators with trading activity, meaningful behavioral patterns can be identified and leveraged to improve decision-making, risk management, and trading strategy development.

The findings highlight the value of combining behavioral finance, sentiment analysis, and machine learning to generate actionable trading insights.

