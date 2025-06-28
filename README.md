# 🧠 Enhanced Portfolio Optimizer (NIFTY 50)

A high-performance investment tool that fuses **Modern Portfolio Theory** with **Machine Learning** to construct optimized portfolios from the **NIFTY 50** universe. Designed exclusively for the **Indian equity market**, it integrates market-specific parameters, live data feeds, and robust statistical techniques.

---

## 🚀 Overview

The **Enhanced Portfolio Optimizer** is a sophisticated investment framework combining:

- 📈 **Financial Theory**: Modern Portfolio Theory for risk-return balance  
- 🧠 **Machine Learning**: PCA, clustering, composite scoring  
- 🇮🇳 **India-Specific Adjustments**: Risk-free rate, NSE tickers, volatility  
- 📊 **Real-Time Analysis**: Live data pulled via Yahoo Finance API  

---

## ✨ Key Features

- 🎯 **Multi-Objective Optimization** – Target return with strict risk constraints  
- 📊 **Advanced Analytics** – Momentum scoring, volatility clustering, regime analysis  
- 🧠 **Machine Learning Integration** – PCA-based factor models, K-means grouping  
- 📉 **Risk Management Tools** – Drawdown tracking, volatility-based filtering  
- 🇮🇳 **India-Specific Calibrations** – Uses Indian market risk-free rates  
- 📈 **Live Market Data** – Integrated Yahoo Finance data pipeline  

---

## 🛠️ Installation

### ✅ Prerequisites
- Python 3.8 or higher  

### 📦 Dependencies
- `numpy`, `pandas`, `yfinance`, `matplotlib`, `seaborn`, `scipy`, `scikit-learn`  

---

## 📋 Usage

### 🧪 Basic Usage

```python
from enhanced_portfolio_optimizer import EnhancedPortfolioOptimizer, nifty50_tickers

# Initialize optimizer
optimizer = EnhancedPortfolioOptimizer(
    tickers=nifty50_tickers,
    start_date="2020-01-01",
    end_date="2025-01-01",
    risk_free_rate=0.07,  # 7% risk-free rate for India
    target_return=0.15    # 15% target return
)

# Generate optimized portfolio
portfolio = optimizer.generate_optimized_portfolio()


⚙️ Advanced Configuration
python
Copy
Edit
# Custom parameters for different market conditions
optimizer = EnhancedPortfolioOptimizer(
    tickers=custom_ticker_list,
    start_date="2022-01-01",
    end_date="2025-01-01",
    risk_free_rate=0.065,      # Adjust based on current rates
    momentum_window=126,        # 6-month momentum window
    sentiment_factor=0.08       # Market sentiment adjustment
)

🎯 Core Methodology
1. 📥 Data Processing & Validation
Fetches historical price data from Yahoo Finance

Cleans missing values using forward fill

Filters stocks with insufficient data history

2. 📊 Metric Weighting Model

| Metric                  | Description                        | Weight in Scoring |
| ----------------------- | ---------------------------------- | ----------------- |
| **Momentum Score**      | 3-month + 6-month momentum returns | 45%               |
| **Regime Performance**  | Bull/bear adaptability             | 35%               |
| **Drawdown Resilience** | Recovery from historical drawdowns | 20%               |

3. 🧠 ML-Based Feature Engineering
PCA Analysis: Identify latent market factors

Volatility Clustering: Group stocks by risk regimes

Composite Scoring: Multi-factor, risk-adjusted ranking

4. 🧮 Portfolio Construction
Optimization Tool: scipy.optimize.minimize()

Constraints:

Weight bounds: 2%–15% per stock

Target return: Defined by user

Max volatility: Risk budgeted

Fallback: Max Sharpe optimization if target is infeasible

⚙️ Configuration Parameters
📉 Market Parameters
| Parameter         | Description                      |
| ----------------- | -------------------------------- |
| `RISK_FREE_RATE`  | 0.07 (Indian 10-year G-Sec rate) |
| `TARGET_RETURN`   | 0.15 (15% annual target return)  |
| `MAX_VOLATILITY`  | 0.25 (Max portfolio risk)        |
| `MOMENTUM_WINDOW` | 126 (6-month rolling window)     |

📌 Portfolio Constraints
| Constraint       | Value                              |
| ---------------- | ---------------------------------- |
| `MIN_WEIGHT`     | 0.02 (2% minimum allocation)       |
| `MAX_WEIGHT`     | 0.15 (15% max per stock)           |
| `TOP_CANDIDATES` | 40 (Number of stocks to shortlist) |

📈 Performance Features
🔐 Risk Metrics
Sharpe Ratio: Return per unit risk

Maximum Drawdown: Largest historical dip

Volatility Clustering: Identifies high-risk periods

Beta Analysis: Sensitivity to broader market

🚀 Return Enhancement Techniques
Momentum: Riding price trends

Mean Reversion: Capitalizing on overbought/oversold moves

Regime Switching: Adaptive logic in bull/bear markets

Factor Exposure: Balanced multi-factor model via PCA

🤝 Contributing
We welcome all contributors! Here’s how you can help:

Fork this repository

Create a feature branch

Commit your changes

Push to your branch

Open a Pull Request 🚀

⚠️ Disclaimer
This project is built for educational and research purposes only.
It does not constitute investment advice.
Past performance ≠ future returns.
Always consult certified professionals before investing.

⚠️ Key Risks
🔺 Market Volatility: Returns can swing wildly

🕰️ Historical Bias: Past data may not reflect future conditions

🏛️ Regulatory Risks: Indian market policies can shift

💱 Currency & Political Risk: Especially relevant in emerging markets

🙏 Acknowledgments
📡 Yahoo Finance – Real-time market data

🐍 NumPy & Pandas – Core data manipulation

⚙️ SciPy – Optimization engine

🤖 Scikit-learn – Machine learning algorithms
