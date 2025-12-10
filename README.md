Risk-to-Strategy: A Regime-Aware Algorithmic Trading System for Gold Futures

This repository presents a two-phase quantitative research project that begins with statistical risk and econometric modelling of Gold Futures (Phase 1) and extends into a regime-aware algorithmic trading system (Phase 2).

The project demonstrates a complete quantitative workflow:

Risk Analysis → Econometric Modelling → Volatility Forecasting → Regime Identification → Strategy Design → Backtesting → Performance Evaluation

It reflects how risk analytics can naturally evolve into systematic trading frameworks used in quantitative finance.

1. Project Overview

Gold Futures display pronounced volatility clustering and distinct market regimes. Understanding these dynamics is essential both for accurate risk measurement and for designing robust, adaptive trading strategies.

This project studies these properties empirically and uses the findings to construct a regime-aware algorithmic trading system.

Phase 1 focuses on modelling return behaviour, volatility patterns, and tail risks.

Phase 2 integrates these insights into a set of tradable, backtestable systematic strategies.

The goal is to show the full progression from risk modelling to strategy implementation.

2. Phase 1 — Statistical Risk and Econometric Analysis

Phase 1 replicates the analytical approach of an academic risk-modelling study.

Data Sources

MCX Gold Futures

LBMA Gold Spot prices

USD/INR exchange rate

Optional macroeconomic variables (e.g., crude oil prices)

Analytical Components

Time-series exploration and return characteristics

Rolling volatility, autocorrelation, and drawdown analysis

ARIMA/ARIMAX modelling

GARCH family models (GARCH, EGARCH, TGARCH)

Value at Risk (VaR) and Expected Shortfall (ES)

Stress testing around major macro events

Key Findings

Gold Futures exhibit:

persistent volatility clustering,

identifiable regime shifts, and

asymmetric tail-risk behaviour.

These findings motivate Phase 2, where risk patterns are translated into trading rules.

3. Phase 2 — Regime-Aware Algorithmic Trading System

Phase 2 extends the insights from Phase 1 into a systematic trading framework.

Regime Detection

GARCH-based volatility thresholds

Hidden Markov Models for latent regime identification

Volatility quantile segmentation

Strategy Design

Strategies are designed to exploit specific volatility regimes:

Trend-following in low-volatility environments

Mean-reversion in high-volatility environments

VaR-based or volatility-based position sizing

Hybrid models combining econometric signals with technical indicators

Backtesting and Evaluation

A custom backtesting module evaluates:

Sharpe Ratio

Sortino Ratio

Maximum Drawdown

Calmar Ratio

Tail-risk and regime-wise return attribution

Comparisons are made against baseline strategies to assess the value added by regime awareness.

4. Repository Structure
project-root/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   ├── phase1_risk_analysis/
│   └── phase2_strategy_development/
│
├── src/
│   ├── data/
│   ├── models/
│   ├── risk/
│   ├── strategies/
│   └── backtesting/
│
├── reports/
│   ├── figures/
│   └── tables/
│
├── utils/
├── requirements.txt
└── README.md

5. Technologies Used

Python

NumPy, Pandas

Statsmodels

arch (for GARCH modelling)

hmmlearn

Scikit-Learn

Matplotlib, Seaborn, Plotly

Backtrader or a custom backtesting engine

6. Planned Enhancements

Incorporation of machine learning models for volatility or directional forecasting

Expansion to multi-asset trading strategies

Event-driven backtesting

Deployment of a dashboard for live simulation and visualisation

7. How to Use This Repository

Clone the repository:

git clone https://github.com/<your-username>/risk-to-strategy-gold-futures.git


Install dependencies:

pip install -r requirements.txt


Begin with the Phase 1 notebooks:

notebooks/phase1_risk_analysis/


Proceed to strategy development:

notebooks/phase2_strategy_development/

8. Author

Nandini Wadhwa
nandini20017@gmail.com
