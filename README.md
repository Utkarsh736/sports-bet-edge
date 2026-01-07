# Sports Betting Edge CLI

[![Tests](https://github.com/Utkarsh736/sports-bet-edge/actions/workflows/test.yml/badge.svg)](https://github.com/Utkarsh736/sports-bet-edge/actions)

A command-line tool that fetches live and historical sports data (**MLB/NBA** via `sportsipy`), runs **XGBoost** models to predict spreads and totals, compares them with bookmaker odds, and flags **+EV (expected value)** bets.

---

## 🚀 Quick Demo

```bash
pip install -r requirements.txt
python src/cli.py --mode live --league mlb --game_id 123456
```
Example output:

```bash
Bet: Yankees -1.5 | Pred Spread: -2.1 | Odds: -110 | EV: +4.2%
```
## 📊 Features
Data fetch using sportsipy (MLB, NBA, NFL)

Feature engineering:

Rolling statistics

Rest days

Matchup history

ML models:

XGBoost for spreads, totals, and moneyline

Expected value (EV) calculations:

American and decimal odds

Backtesting with Kelly Criterion

Designed to be extensible (cricket, football, etc.)

## 🛠 Install & Run
```bash
Copy code
git clone https://github.com/Utkarsh736/sports-bet-edge
cd sports-bet-edge
```
Install dependencies:

```bash

uv sync
# OR
pip install -r requirements.txt
```
Run the CLI:

```bash
uv run python src/cli.py --help
Requirements
Python 3.12+

pandas

sportsipy

xgboost

joblib

click
```

## 📈 Backtest Results (MLB 2025)
Strategy	ROI	Sharpe	Win %
Spread	5.2%	1.12	54%
Totals	3.8%	0.89	52%

## ⚠️ Disclaimer
This is an educational tool only.
Gambling involves risk — use responsibly.

## 🚧 Roadmap
 MLB data fetcher

 NBA extension

 Live odds API integration

 Streamlit dashboard

## ✏️ Lessons Learned
- Blog series:

    - Part 1: Data Fetch

## 🤝 Contributing
Pull requests are welcome.
Please see CONTRIBUTING.md for guidelines.

## 📄 License
MIT