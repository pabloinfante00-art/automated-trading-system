# 📈 Automated Daily Trading System

An automated daily trading system that uses machine learning to predict stock market movements for 5 US large-cap equities. Built with Python, Scikit-learn, and Streamlit.

**Author:** Pablo Infante  
**Programme:** Master of Business Analytics and Data Science, IE School of Science and Technology

---

## 🌐 Live Application

[![Live App](https://img.shields.io/badge/Live_App-Trading_System-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)](https://trading-system-gnvcjp4j8kqekggfhwpfl2.streamlit.app)

---

## Overview

This system consists of two main parts:

1. **Data Analytics Module** — An ETL pipeline processes historical stock data from SimFin, then a Logistic Regression model is trained to predict whether the next day's closing price will go UP or DOWN.
2. **Web Application** — A three-page Streamlit app: the Go Live page fetches real-time data from the SimFin API and generates live trading signals; the Backtesting page runs the ML strategy against a buy-and-hold baseline with full performance metrics.

## Coverage Universe

| Ticker | Company |
|--------|---------|
| AAPL | Apple Inc. |
| MSFT | Microsoft Corp. |
| GOOG | Alphabet Inc. |
| AMZN | Amazon.com Inc. |
| TSLA | Tesla Inc. |

## Project Structure

```
.
├── src/                        # Core Python modules
│   ├── etl.py                  # ETL pipeline & feature engineering
│   └── model.py                # ML model training & export
├── data/
│   └── processed/              # Feature-engineered CSVs
├── models/                     # Trained model .pkl files
├── trading-system/             # Streamlit web application
│   ├── app/
│   │   ├── Home.py             # Home page
│   │   └── pages/
│   │       ├── 1_Go_Live.py    # Real-time predictions
│   │       └── 2_Backtesting.py
│   └── src/                    # App-level modules
├── development_notebook.ipynb  # Exploration & analysis
├── requirements.txt
└── README.md
```

## Technologies Used

| Technology | Purpose |
|---|---|
| Python 3.11 | Core language |
| Pandas | Data manipulation |
| Scikit-learn | Logistic Regression model |
| Streamlit | Web application |
| SimFin API | Financial data source |
| Joblib | Model serialization |

## Local Setup

```bash
# 1. Clone
git clone https://github.com/pabloinfante00-art/automated-trading-system.git
cd automated-trading-system

# 2. Install dependencies
pip install -r requirements.txt

# 3. Run ETL pipeline
python src/etl.py

# 4. Train models
python src/model.py

# 5. Launch Streamlit app
streamlit run trading-system/app/Home.py
```

---

> ⚠️ **Disclaimer:** This project is for educational purposes only and does not constitute financial advice.
