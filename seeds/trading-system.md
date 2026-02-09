# Trading System - Seed

## Project
Trading system (e.g., BTCUSDT 4h)

## Goal
One tested, rules-based strategy from idea → code → backtest → forward test.

## Stack
- TradingView: Pine Script strategy
- Backtester: Python (backtrader / vectorbt)
- Data source: [TBD]
- Logging: Trade log + results CSV

## Constraints
- Simple, interpretable rules
- Risk per trade defined
- Prop-firm or personal account compatible
- Cost efficient

## Current state
- [ ] Market + timeframe locked
- [ ] Entry/exit rules (plain English)
- [ ] Risk rules (per-trade %, daily max loss)
- [ ] Initial code skeleton

## Open questions
- Exact filters (trend, volatility)?
- Handling news / regime shifts?
- Which data provider?

## Next actions
1. Finalize rules
2. Implement code
3. Run backtest + log results
