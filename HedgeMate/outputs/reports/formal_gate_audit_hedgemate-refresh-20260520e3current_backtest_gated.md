# Formal Gate Audit

- candidate_rows: 66
- status_counts: `{"PASS_RECOMMEND": 0, "REFERENCE_ONLY": 28, "FAIL_GATE": 38, "INSUFFICIENT_DATA": 0}`

## Blocker Counts

- bootstrap_not_robust: 57 - Target stress bootstrap confidence is not robust.
- cash_baseline_lag: 56 - Hedge lags a cash-only de-risking baseline in target stress.
- fail_gate: 38 - Candidate failed a hard gate.
- return_drag_reference: 34 - Pre-backtest scoring kept the candidate reference-only because of return drag.
- validation_thin: 30 - Target stress validation sample is too small for formal use.
- liquidity_below_formal: 28 - 60-day ADV evidence is missing or below the formal threshold.
- reference_only: 28 - Candidate remains reference-only after formal gate checks.
- validation_insufficient: 9 - Target stress validation has insufficient history.
- target_worsened: 1 - Target stress backtest worsened risk metrics.

## Liquidity Capacity Audit

- BELOW_FORMAL_ADV_FLOOR_NO_ORDER_SIZE: 17
- MISSING_ADV: 11
- OK_ADV_FLOOR_NO_ORDER_SIZE: 38

| candidate | source | status | ADV KRW | order KRW | ADV usage % | capacity status |
|---|---|---|---:|---:|---:|---|
| DBC | one_to_one | FAIL_GATE | 73595336412.57709 |  |  | BELOW_FORMAL_ADV_FLOOR_NO_ORDER_SIZE |
| DBC | one_to_one | FAIL_GATE | 73595336412.57709 |  |  | BELOW_FORMAL_ADV_FLOOR_NO_ORDER_SIZE |
| GLD + DBC | multi | REFERENCE_ONLY | 73595336412.57709 |  |  | BELOW_FORMAL_ADV_FLOOR_NO_ORDER_SIZE |
| GLD + DBC | multi | REFERENCE_ONLY | 73595336412.57709 |  |  | BELOW_FORMAL_ADV_FLOOR_NO_ORDER_SIZE |
| GLD + DBC | multi | FAIL_GATE | 73595336412.57709 |  |  | BELOW_FORMAL_ADV_FLOOR_NO_ORDER_SIZE |
| IAU + DBC | multi | REFERENCE_ONLY | 73595336412.57709 |  |  | BELOW_FORMAL_ADV_FLOOR_NO_ORDER_SIZE |
| IAU + DBC | multi | REFERENCE_ONLY | 73595336412.57709 |  |  | BELOW_FORMAL_ADV_FLOOR_NO_ORDER_SIZE |
| IAU + DBC | multi | FAIL_GATE | 73595336412.57709 |  |  | BELOW_FORMAL_ADV_FLOOR_NO_ORDER_SIZE |
| IEF + DBC | multi | REFERENCE_ONLY | 73595336412.57709 |  |  | BELOW_FORMAL_ADV_FLOOR_NO_ORDER_SIZE |
| IEF + DBC | multi | FAIL_GATE | 73595336412.57709 |  |  | BELOW_FORMAL_ADV_FLOOR_NO_ORDER_SIZE |
| IEF + DBC | multi | FAIL_GATE | 73595336412.57709 |  |  | BELOW_FORMAL_ADV_FLOOR_NO_ORDER_SIZE |
| SHY + DBC | multi | REFERENCE_ONLY | 73595336412.57709 |  |  | BELOW_FORMAL_ADV_FLOOR_NO_ORDER_SIZE |

## Highest-friction Candidates

| candidate | source | status | readiness | blockers | target eval | cash lags | robust/boot | min p | min cash stress | reason |
|---|---|---|---:|---|---:|---:|---:|---:|---:|---|
| DBC | one_to_one | FAIL_GATE | 34.5 | fail_gate, validation_thin, cash_baseline_lag, bootstrap_not_robust, liquidity_below_formal, return_drag_reference | 1 | 1 | 0/1 | 0.725 | 0.032303 | target-scenario backtest has only 1 evaluated stress case; 표본 부족 |
| XLE | one_to_one | FAIL_GATE | 38.6 | fail_gate, target_worsened, validation_thin, cash_baseline_lag, bootstrap_not_robust, liquidity_below_formal | 1 | 1 | 0/1 | 0.93 | 0.12727 | target-scenario backtest worsened risk metrics; 정식 추천 불가 |
| GLD + DBC | multi | REFERENCE_ONLY | 39.2 | validation_thin, cash_baseline_lag, bootstrap_not_robust, liquidity_below_formal, return_drag_reference, reference_only | 1 | 1 | 0/1 | 0.46 | -0.003265 | target-scenario backtest has only 1 evaluated stress case; 표본 부족 |
| GLD + DBC | multi | REFERENCE_ONLY | 39.4 | validation_thin, cash_baseline_lag, bootstrap_not_robust, liquidity_below_formal, return_drag_reference, reference_only | 1 | 1 | 0/1 | 0.47 | -0.00653 | target-scenario backtest has only 1 evaluated stress case; 표본 부족 |
| IAU + DBC | multi | REFERENCE_ONLY | 39.9 | validation_thin, cash_baseline_lag, bootstrap_not_robust, liquidity_below_formal, return_drag_reference, reference_only | 1 | 1 | 0/1 | 0.495 | -0.006258 | target-scenario backtest has only 1 evaluated stress case; 표본 부족 |
| IAU + DBC | multi | REFERENCE_ONLY | 41.0 | validation_thin, cash_baseline_lag, bootstrap_not_robust, liquidity_below_formal, return_drag_reference, reference_only | 1 | 1 | 0/1 | 0.55 | -0.003129 | target-scenario backtest has only 1 evaluated stress case; 표본 부족 |
| TLT | one_to_one | FAIL_GATE | 23.7 | fail_gate, validation_thin, cash_baseline_lag, bootstrap_not_robust, liquidity_below_formal | 1 | 1 | 0/1 | 0.185 | -0.084772 | target-scenario backtest has only 1 evaluated stress case; 표본 부족 |
| IEF | one_to_one | FAIL_GATE | 27.4 | fail_gate, validation_thin, cash_baseline_lag, bootstrap_not_robust, liquidity_below_formal | 1 | 1 | 0/1 | 0.37 | -0.04456 | target-scenario backtest has only 1 evaluated stress case; 표본 부족 |
| GLD | one_to_one | FAIL_GATE | 28.2 | fail_gate, validation_thin, cash_baseline_lag, bootstrap_not_robust, liquidity_below_formal | 1 | 1 | 0/1 | 0.41 | -0.024356 | target-scenario backtest has only 1 evaluated stress case; 표본 부족 |
| IAU | one_to_one | FAIL_GATE | 29.5 | fail_gate, validation_thin, cash_baseline_lag, bootstrap_not_robust, liquidity_below_formal | 1 | 1 | 0/1 | 0.475 | -0.023845 | target-scenario backtest has only 1 evaluated stress case; 표본 부족 |
| GLD + DBC | multi | FAIL_GATE | 31.2 | fail_gate, validation_thin, cash_baseline_lag, bootstrap_not_robust, liquidity_below_formal | 1 | 1 | 0/1 | 0.56 | 0.004765 | target-scenario backtest has only 1 evaluated stress case; 표본 부족 |
| IAU + DBC | multi | FAIL_GATE | 31.2 | fail_gate, validation_thin, cash_baseline_lag, bootstrap_not_robust, liquidity_below_formal | 1 | 1 | 0/1 | 0.56 | 0.005071 | target-scenario backtest has only 1 evaluated stress case; 표본 부족 |

## Closest Formal Near-misses

| candidate | source | status | readiness | blockers | target eval | cash lags | robust/boot | min p | avg cash stress | reason |
|---|---|---|---:|---|---:|---:|---:|---:|---:|---|
| GLD + SHY | multi | REFERENCE_ONLY | 68.1 | cash_baseline_lag, bootstrap_not_robust, return_drag_reference, reference_only | 2 | 2 | 0/2 | 0.405 | -0.014164 | target-scenario hedge did not beat cash-only de-risking in 2 stress case |
| IEF + IAU | multi | REFERENCE_ONLY | 68.1 | cash_baseline_lag, bootstrap_not_robust, return_drag_reference, reference_only | 2 | 2 | 0/2 | 0.405 | -0.010013 | target-scenario hedge did not beat cash-only de-risking in 2 stress case |
| SHY + IAU | multi | REFERENCE_ONLY | 67.9 | cash_baseline_lag, bootstrap_not_robust, return_drag_reference, reference_only | 2 | 2 | 0/2 | 0.395 | -0.00727 | target-scenario hedge did not beat cash-only de-risking in 2 stress case |
| SHY + IAU | multi | REFERENCE_ONLY | 67.8 | cash_baseline_lag, bootstrap_not_robust, return_drag_reference, reference_only | 2 | 2 | 0/2 | 0.39 | -0.01386 | target-scenario hedge did not beat cash-only de-risking in 2 stress case |
| GLD + SHY | multi | REFERENCE_ONLY | 67.4 | cash_baseline_lag, bootstrap_not_robust, return_drag_reference, reference_only | 2 | 2 | 0/2 | 0.37 | -0.007443 | target-scenario hedge did not beat cash-only de-risking in 2 stress case |
| IEF + IAU | multi | REFERENCE_ONLY | 67.2 | cash_baseline_lag, bootstrap_not_robust, return_drag_reference, reference_only | 2 | 2 | 0/2 | 0.36 | -0.020026 | target-scenario hedge did not beat cash-only de-risking in 2 stress case |
| IEF + GLD | multi | REFERENCE_ONLY | 66.7 | cash_baseline_lag, bootstrap_not_robust, return_drag_reference, reference_only | 2 | 2 | 0/2 | 0.335 | -0.010165 | target-scenario hedge did not beat cash-only de-risking in 2 stress case |
| IEF + GLD | multi | REFERENCE_ONLY | 66.6 | cash_baseline_lag, bootstrap_not_robust, return_drag_reference, reference_only | 2 | 2 | 0/2 | 0.33 | -0.020329 | target-scenario hedge did not beat cash-only de-risking in 2 stress case |
| TLT + GLD | multi | REFERENCE_ONLY | 65.6 | cash_baseline_lag, bootstrap_not_robust, return_drag_reference, reference_only | 2 | 2 | 0/2 | 0.28 | -0.014227 | target-scenario hedge did not beat cash-only de-risking in 2 stress case |
| TLT + IAU | multi | REFERENCE_ONLY | 65.6 | cash_baseline_lag, bootstrap_not_robust, return_drag_reference, reference_only | 2 | 2 | 0/2 | 0.28 | -0.014075 | target-scenario hedge did not beat cash-only de-risking in 2 stress case |
| TLT + IAU | multi | REFERENCE_ONLY | 65.5 | cash_baseline_lag, bootstrap_not_robust, return_drag_reference, reference_only | 2 | 2 | 0/2 | 0.275 | -0.028148 | target-scenario hedge did not beat cash-only de-risking in 2 stress case |
| TLT + GLD | multi | REFERENCE_ONLY | 65.4 | cash_baseline_lag, bootstrap_not_robust, return_drag_reference, reference_only | 2 | 2 | 0/2 | 0.27 | -0.028452 | target-scenario hedge did not beat cash-only de-risking in 2 stress case |
