# Backtest Gate Summary

- generated_at_utc: 2026-05-20T08:40:10Z
- hedgemate_run_id: hedgemate-refresh-20260520e3current
- backtest_run_id: backtest-refresh-20260520e3current
- one_to_one_rows: 33
- multi_rows: 33
- one_to_one_status_counts: `{"FAIL_GATE": 24, "REFERENCE_ONLY": 9}`
- multi_status_counts: `{"FAIL_GATE": 14, "REFERENCE_ONLY": 19}`
- post_backtest_qa_md: C:\Users\석민\Documents\cau_2026_ss\금융인공지능실습1\HedgeMate\outputs\reports\recommendation_status_qa_post_backtest_hedgemate-refresh-20260520e3current_backtest_gated.md
- backtest_attribution_csv: C:\Users\석민\Documents\cau_2026_ss\금융인공지능실습1\HedgeMate\outputs\reports\backtest_attribution_backtest-refresh-20260520e3current.csv
- backtest_attribution_md: C:\Users\석민\Documents\cau_2026_ss\금융인공지능실습1\HedgeMate\outputs\reports\backtest_attribution_backtest-refresh-20260520e3current.md
- formal_gate_audit_csv: C:\Users\석민\Documents\cau_2026_ss\금융인공지능실습1\HedgeMate\outputs\reports\formal_gate_audit_hedgemate-refresh-20260520e3current_backtest_gated.csv
- formal_gate_audit_md: C:\Users\석민\Documents\cau_2026_ss\금융인공지능실습1\HedgeMate\outputs\reports\formal_gate_audit_hedgemate-refresh-20260520e3current_backtest_gated.md
- formal_gate_blocker_counts: `{"bootstrap_not_robust": 57, "cash_baseline_lag": 56, "fail_gate": 38, "return_drag_reference": 34, "validation_thin": 30, "liquidity_below_formal": 28, "reference_only": 28, "validation_insufficient": 9, "target_worsened": 1}`

## Policy

- Backtest verdicts are treated as cost-adjusted when cost fields are present.
- WORSENED candidates are not allowed to remain PASS_RECOMMEND.
- INSUFFICIENT_HISTORY is shown as validation insufficient, never as success.
- Formal recommendations require at least 2 evaluated target stress cases.
- Formal recommendations must beat a cash-only de-risking baseline in target stress cases.
- If bootstrap confidence fields are present, every evaluated target stress case must be ROBUST_IMPROVE for a formal recommendation.
- Formal recommendations require combo_min_adv_60 of at least 100,000,000,000 KRW.
- Formal recommendations require target max turnover no higher than 0.50.
- Candidates without matching backtest evidence are downgraded from formal recommendation to reference-only.
