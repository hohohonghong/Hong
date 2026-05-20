# Phase 10E Rebalance-cost Path Walk-forward Backtest

- run_id: `backtest-refresh-20260520e3current`
- historical_validation_run_id: `phase10a-wave5-20260514`
- hedgemate_run_id: `hedgemate-refresh-20260520e3current`
- engine_version: `phase10e_rebalance_cost_path_walk_forward_v1`
- data_mode: API-free cached raw market prices
- transaction_cost_bps: 10
- slippage_bps: 5
- rebalance_frequency: `formation_only`
- bootstrap_iterations: 200
- bootstrap_ci_level: 0.95
- return_path_model: formation_only uses buy-and-hold weights; monthly/daily modes rebalance to target weights
- implementation_cost_model: one-time formation turnover cost deducted from proposed returns
- recurring_rebalance_cost_model: monthly/daily modes deduct turnover cost at each scheduled rebalance
- evaluated_rows: 528
- insufficient_history_rows: 66
- insufficient_evaluation_window_rows: 0
- out_of_price_range_rows: 0
- beats_cash_rows: 209
- lags_cash_rows: 319

## Verdict Counts
- IMPROVED: 504
- MIXED: 0
- WORSENED: 24
- INSUFFICIENT_HISTORY: 66

## Hedge vs Cash Baseline
- BEATS_CASH: 209
- MIXED_CASH: 0
- LAGS_CASH: 319

## Price Window Counts
- NO_COMMON_PRICE_DATES: 66
- PRICE_WINDOW_AVAILABLE: 528

## Price Blocking Tickers
- 207940.KS: 66
- AVGO: 66

## Pre-inception Tickers
- 207940.KS: 66
- AVGO: 66

## Missing Price Tickers
- none

## Notes
- Verdict counts use cost-adjusted proposed returns.
- Bootstrap intervals resample paired daily base/proposed-net returns by candidate and stress case.
- Insufficient-history cases are never counted as successful detection or backtest wins.
