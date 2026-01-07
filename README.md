# Sports Betting Edge CLI

[![Tests](https://github.com/Utkarsh736/sports-bet-edge/actions/workflows/test.yml/badge.svg)](https://github.com/Utkarsh736/sports-bet-edge/actions)

A command-line tool that fetches live and historical sports data (**MLB/NBA** via `sportsipy`), runs **XGBoost** models to predict spreads and totals, compares predictions with bookmaker odds, and flags **+EV (expected value)** betting opportunities.

This project is built as part of a **Boot.dev-style backend/CLI learning workflow**, focusing on data pipelines, modeling, and clean CLI design.

---

## Motivation

The goal of this project is to practice building a production-style CLI application that integrates:

- External data sources (sports APIs)
- Feature engineering pipelines
- Machine learning models
- Probabilistic decision-making (EV, Kelly Criterion)

It is intended as a **learning project**, not a betting product, emphasizing software engineering fundamentals alongside applied ML.

---

## Quick Start

Clone the repository:

```bash
git clone https://github.com/Utkarsh736/sports-bet-edge
cd sports-bet-edge
```
### Install dependencies:
```bash
uv sync
# OR
pip install -r requirements.txt
```

### Verify the CLI:
```
python src/cli.py --help
```
## Usage

Run the CLI in live or historical mode:
```bash
python src/cli.py --mode live --league mlb --game_id 123456
```


Example output:
```bash
Bet: Yankees -1.5 | Pred Spread: -2.1 | Odds: -110 | EV: +4.2%
```

## Supported features:

- Leagues: MLB (NBA planned)

- Models: XGBoost (spreads, totals, moneyline)

- Odds formats: American and decimal

- Backtesting with Kelly Criterion sizing

## Contributing

Contributions are welcome and encouraged.

Typical contribution ideas:

- Improving feature engineering

- Adding new leagues (NBA, NFL)

- Integrating a live odds API

- Improving backtesting and evaluation

- Adding tests and documentation

Please open an issue or submit a pull request.
For larger changes, discuss the approach first.

## Disclaimer

This project is for educational purposes only.
It is not financial advice. Gamble responsibly.

## License

MIT