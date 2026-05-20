# HedgeMate Recommendation Status QA (Post-Backtest)

- generated_at_utc: 2026-05-20T08:40:10Z
- hedgemate_run_id: hedgemate-refresh-20260520e3current
- backtest_run_id: backtest-refresh-20260520e3current
- basis: post-backtest gated recommendation CSVs
- portfolio_1to1_gated_csv: C:\Users\석민\Documents\cau_2026_ss\금융인공지능실습1\HedgeMate\outputs\reports\portfolio_1to1_hedge_hedgemate-refresh-20260520e3current_backtest_gated.csv
- portfolio_multi_gated_csv: C:\Users\석민\Documents\cau_2026_ss\금융인공지능실습1\HedgeMate\outputs\reports\portfolio_multi_hedge_hedgemate-refresh-20260520e3current_backtest_gated.csv

## Status Counts

- PASS_RECOMMEND: 0
- REFERENCE_ONLY: 28
- FAIL_GATE: 38
- INSUFFICIENT_DATA: 0

## Backtest Gate Counts

- FAIL_BACKTEST: 1
- REFERENCE_ONLY_CASH_BASELINE: 27
- VALIDATION_INSUFFICIENT: 9
- VALIDATION_THIN: 29

## Formal Gate Blocker Counts

- bootstrap_not_robust: 57
- cash_baseline_lag: 56
- fail_gate: 38
- return_drag_reference: 34
- validation_thin: 30
- liquidity_below_formal: 28
- reference_only: 28
- validation_insufficient: 9
- target_worsened: 1

## Backtest Attribution Summary

- attribution_csv: C:\Users\석민\Documents\cau_2026_ss\금융인공지능실습1\HedgeMate\outputs\reports\backtest_attribution_backtest-refresh-20260520e3current.csv
- attribution_md: C:\Users\석민\Documents\cau_2026_ss\금융인공지능실습1\HedgeMate\outputs\reports\backtest_attribution_backtest-refresh-20260520e3current.md
- evaluated_count: 528
- improved_count: 504
- worsened_count: 24

| candidate | scenario | evaluated | worsened | worsened_rate | worst_metric | worst_delta | worst_case |
|---|---|---:|---:|---:|---|---:|---|
| USO | acute_global_stress_liquidity_crunch | 6 | 6 | 1.0 | cost_adjusted_return_drag | -0.514008 | 2023 US Regional Bank / Credit Stress |
| XLE | acute_global_stress_liquidity_crunch | 6 | 6 | 1.0 | cost_adjusted_return_drag | -0.48492 | 2023 US Regional Bank / Credit Stress |
| XLU | acute_global_stress_liquidity_crunch | 6 | 5 | 0.8333 | cost_adjusted_return_drag | -0.334168 | 2023 US Regional Bank / Credit Stress |
| DBC | acute_global_stress_liquidity_crunch | 6 | 3 | 0.5 | cost_adjusted_return_drag | -0.452005 | 2023 US Regional Bank / Credit Stress |
| USO | higher_for_longer_long_rate_shock | 3 | 1 | 0.3333 | cash_net_MDD | -0.110352 | 2022 Global Rate Shock |
| USO | usd_strength_krw_weakness | 3 | 1 | 0.3333 | cost_adjusted_return_drag | -0.090099 | 2022 KRW Weakness / USD Strength |
| XLE | higher_for_longer_long_rate_shock | 3 | 1 | 0.3333 | cash_net_MDD | -0.075303 | 2022 Global Rate Shock |
| XLE | stagflation_reinflation_energy_shock | 3 | 1 | 0.3333 | cash_net_MDD | -0.068123 | Russia-Ukraine / War-Energy Shock |
| DBC | china_trade_fragmentation_shock | 3 | 0 | 0.0 | net_stress_loss | -0.342576 | China Slowdown / Property Stress |
| DBC | geopolitical_escalation_supply_shock | 3 | 0 | 0.0 | cash_net_CVaR | -0.001668 | 2024 Middle East / Shipping Supply Shock |

## Zero Formal Recommendation Message

- 현재 검증 기준에서 정식 추천 가능한 후보는 없습니다. 참고용 후보는 있으나, backtest evidence가 부족하거나 일부 구간에서 위험 악화가 확인되어 정식 추천으로 분류하지 않았습니다.

## Policy Audit

- WORSENED candidates still marked PASS_RECOMMEND: 0
- INSUFFICIENT_HISTORY-only candidates marked as successful PASS_RECOMMEND: 0
- Missing backtest evidence is treated as validation missing and cannot upgrade a formal recommendation.
- Combination candidates require evidence for the same combination; component evidence alone is not used for upgrade.

## Examples By Final Status

| recommendation_status | candidate | backtest_gate_status | worsened | insufficient_history | reason |
|---|---|---|---:|---:|---|
| PASS_RECOMMEND | - | - | 0 | 0 | no rows in this run |
| REFERENCE_ONLY | TLT | VALIDATION_THIN | 0 | 0 | target-scenario backtest has only 1 evaluated stress case; 표본 부족 |
| REFERENCE_ONLY | IEF | VALIDATION_THIN | 0 | 0 | target-scenario backtest has only 1 evaluated stress case; 표본 부족 |
| REFERENCE_ONLY | GLD | VALIDATION_THIN | 0 | 0 | target-scenario backtest has only 1 evaluated stress case; 표본 부족 |
| REFERENCE_ONLY | IAU | VALIDATION_THIN | 0 | 0 | target-scenario backtest has only 1 evaluated stress case; 표본 부족 |
| REFERENCE_ONLY | XLP | VALIDATION_INSUFFICIENT | 0 | 0 | target-scenario historical validation has insufficient history; 검증 부족 |
| REFERENCE_ONLY | XLU | VALIDATION_INSUFFICIENT | 0 | 0 | target-scenario historical validation has insufficient history; 검증 부족 |
| REFERENCE_ONLY | XLV | VALIDATION_INSUFFICIENT | 0 | 0 | target-scenario historical validation has insufficient history; 검증 부족 |
| REFERENCE_ONLY | GLD | VALIDATION_THIN | 0 | 0 | target-scenario backtest has only 1 evaluated stress case; 표본 부족 |
| REFERENCE_ONLY | IAU | VALIDATION_THIN | 0 | 0 | target-scenario backtest has only 1 evaluated stress case; 표본 부족 |
| REFERENCE_ONLY | TLT + GLD | REFERENCE_ONLY_CASH_BASELINE | 0 | 0 | target-scenario hedge did not beat cash-only de-risking in 2 stress case |
| FAIL_GATE | SHY | VALIDATION_THIN | 0 | 0 | target-scenario backtest has only 1 evaluated stress case; 표본 부족 |
| FAIL_GATE | DBC | VALIDATION_THIN | 0 | 0 | target-scenario backtest has only 1 evaluated stress case; 표본 부족 |
| FAIL_GATE | USO | VALIDATION_THIN | 0 | 0 | target-scenario backtest has only 1 evaluated stress case; 표본 부족 |
| FAIL_GATE | XLE | VALIDATION_THIN | 0 | 0 | target-scenario backtest has only 1 evaluated stress case; 표본 부족 |
| FAIL_GATE | TLT | VALIDATION_THIN | 0 | 0 | target-scenario backtest has only 1 evaluated stress case; 표본 부족 |
| FAIL_GATE | IEF | VALIDATION_THIN | 0 | 0 | target-scenario backtest has only 1 evaluated stress case; 표본 부족 |
| FAIL_GATE | SHY | VALIDATION_THIN | 0 | 0 | target-scenario backtest has only 1 evaluated stress case; 표본 부족 |
| FAIL_GATE | DBC | VALIDATION_THIN | 0 | 0 | target-scenario backtest has only 1 evaluated stress case; 표본 부족 |
| FAIL_GATE | XLP | VALIDATION_INSUFFICIENT | 0 | 0 | target-scenario historical validation has insufficient history; 검증 부족 |
| FAIL_GATE | XLU | VALIDATION_INSUFFICIENT | 0 | 0 | target-scenario historical validation has insufficient history; 검증 부족 |
| INSUFFICIENT_DATA | - | - | 0 | 0 | no rows in this run |
