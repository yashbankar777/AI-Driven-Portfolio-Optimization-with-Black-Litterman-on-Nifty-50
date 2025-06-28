🚀 Overview
The Enhanced Portfolio Optimizer is a sophisticated investment tool that combines modern portfolio theory with advanced machine learning techniques to construct optimal portfolios from the NIFTY 50 universe. Built specifically for the Indian equity market, it incorporates market-specific parameters and risk factors.
✨ Key Features

🎯 Multi-Objective Optimization: Target return optimization with risk constraints
📊 Advanced Analytics: Momentum scoring, volatility clustering, and regime analysis
🧠 Machine Learning: PCA-based factor analysis and K-means clustering
📉 Risk Management: Maximum drawdown analysis and volatility-based filtering
🇮🇳 India-Specific: Calibrated for NSE markets with appropriate risk-free rates
📈 Real-Time Data: Fetches live market data using Yahoo Finance API

🛠️ Installation
Prerequisites: Python 3.8 or higher
Dependencies: numpy, pandas, yfinance, matplotlib, seaborn, scipy, scikit-learn
📋 Usage
Basic Usage
pythonfrom enhanced_portfolio_optimizer import EnhancedPortfolioOptimizer, nifty50_tickers

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
Advanced Configuration
python# Custom parameters for different market conditions
optimizer = EnhancedPortfolioOptimizer(
    tickers=custom_ticker_list,
    start_date="2022-01-01",
    end_date="2025-01-01",
    risk_free_rate=0.065,      # Adjust based on current rates
    momentum_window=126,        # 6-month momentum window
    sentiment_factor=0.08       # Market sentiment adjustment
)
🎯 Core Methodology
1. Data Processing & Validation

Fetches historical price data from Yahoo Finance
Validates data quality and handles missing values
Filters out stocks with insufficient trading history


PCA Analysis: Factor exposure identification
Volatility Clustering: Risk-based stock grouping
Composite Scoring: Multi-factor ranking system

4. Portfolio Construction

Constraint-based optimization using scipy
Weight limits: 2% - 15% per stock for diversification
Risk budgeting with volatility constraints


Market Parameters

RISK_FREE_RATE: 0.07 (Indian 10-year G-Sec rate)
TARGET_RETURN: 0.15 (15% annual target return)
MAX_VOLATILITY: 0.25 (25% maximum portfolio volatility)
MOMENTUM_WINDOW: 126 (6-month momentum calculation)

Portfolio Constraints

MIN_WEIGHT: 0.02 (2% minimum allocation per stock)
MAX_WEIGHT: 0.15 (15% maximum allocation per stock)
TOP_CANDIDATES: 40 (Number of stocks to consider)

📈 Performance Features
Risk Metrics

Sharpe Ratio: Risk-adjusted return measurement
Maximum Drawdown: Worst peak-to-trough decline
Volatility Clustering: Risk regime identification
Beta Analysis: Market correlation assessment

Return Enhancement

Momentum Factors: Price trend analysis
Mean Reversion: Long-term equilibrium modeling
Regime Switching: Bull/bear market adaptation
Factor Exposure: Multi-factor risk model

🤝 Contributing
We welcome contributions! Please follow these steps:

Fork the repository
Create a feature branch
Commit your changes
Push to the branch
Open a Pull Request

⚠️ Disclaimer

Important: This tool is for educational and research purposes only. It does not constitute financial advice. Always consult with qualified financial advisors before making investment decisions. Past performance does not guarantee future results.

Risk Factors

Market volatility can affect portfolio performance
Historical data may not predict future market conditions
Regulatory changes can impact investment outcomes
Currency and political risks in emerging markets


🙏 Acknowledgments

Yahoo Finance for providing market data API
NumPy & Pandas teams for excellent data manipulation libraries
SciPy for optimization algorithms
Scikit-learn for machine learning capabilities

