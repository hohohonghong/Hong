# Hedge Action Plan

- run_id: hedgemate-refresh-20260520e3current
- engine_version: hedge_action_engine_v1
- formal gate: 기존 PASS_RECOMMEND 기준을 완화하지 않음

## Portfolio
- MSFT: 19.671008287690857%
- NVDA: 19.671008287690857%
- AVGO: 10.062930506163566%
- XOM: 11.253036343073006%
- 011200.KS: 19.671008287690857%
- 207940.KS: 19.671008287690857%

## Status Counts
- FAIL_ACTION: 3
- REVIEW_ACTION: 57

## Top Vulnerabilities
- 지정학·공급망 충격 (geopolitical_supply_chain): net=0.44535735, sources=NVDA, 207940.KS, 011200.KS, offsets=-
- 장기금리·성장주 듀레이션 (rate_shock_growth_duration): net=0.4124587, sources=NVDA, MSFT, AVGO, offsets=-
- 물가·에너지 재상승 (inflation_energy_shock): net=0.22580687, sources=NVDA, MSFT, AVGO, offsets=-
- 침체·유동성 스트레스 (recession_liquidity_stress): net=0.20252739, sources=NVDA, MSFT, AVGO, offsets=-
- 달러강세·원화약세 (usdkrw_fx_korea): net=0.15790587, sources=207940.KS, 011200.KS, NVDA, offsets=MSFT, XOM, AVGO
- AI·반도체 사이클 (semiconductor_ai_cycle): net=0, sources=-, offsets=-
- 한국 내수·신용 스트레스 (korea_domestic_credit): net=0, sources=-, offsets=-

## Selected Actions
- REVIEW_ACTION · TRIM_AND_HEDGE · geopolitical_supply_chain: IAU / delta=-0.04665108 / turnover=10.000002% / reason=취약성 기여가 큰 보유자산이 확인되어 단순 추가 헷지보다 TRIM_AND_HEDGE가 우선입니다.
  - expected_effect: 취약성 0.0467 감소; CVaR 0.25%p 개선; MDD 1.53%p 개선; stress 0.00%p 개선; Sharpe 0.00 악화
  - formal_action_gap: FORMAL_ACTION 제외 사유: 기존 추천 gate 상태가 REFERENCE_ONLY입니다. stress/backtest, CVaR·MDD 안정성, 거래 제약 검증이 추가로 충족되어야 정식 추천으로 올릴 수 있습니다.
- REVIEW_ACTION · TRIM_AND_HEDGE · rate_shock_growth_duration: TLT + IAU / delta=-0.03653118 / turnover=10.000002% / reason=취약성 기여가 큰 보유자산이 확인되어 단순 추가 헷지보다 TRIM_AND_HEDGE가 우선입니다.
  - expected_effect: 취약성 0.0365 감소; CVaR 0.26%p 개선; MDD 1.76%p 개선; stress 0.00%p 개선; Sharpe 0.02 악화
  - formal_action_gap: FORMAL_ACTION 제외 사유: 기존 추천 gate 상태가 REFERENCE_ONLY입니다. stress/backtest, CVaR·MDD 안정성, 거래 제약 검증이 추가로 충족되어야 정식 추천으로 올릴 수 있습니다.
- REVIEW_ACTION · TRIM_AND_HEDGE · inflation_energy_shock: IAU / delta=-0.03466032 / turnover=10.000002% / reason=취약성 기여가 큰 보유자산이 확인되어 단순 추가 헷지보다 TRIM_AND_HEDGE가 우선입니다.
  - expected_effect: 취약성 0.0347 감소; CVaR 0.25%p 개선; MDD 1.53%p 개선; stress 0.00%p 개선; Sharpe 0.00 악화
  - formal_action_gap: FORMAL_ACTION 제외 사유: 기존 추천 gate 상태가 REFERENCE_ONLY입니다. stress/backtest, CVaR·MDD 안정성, 거래 제약 검증이 추가로 충족되어야 정식 추천으로 올릴 수 있습니다.
- REVIEW_ACTION · TRIM_AND_HEDGE · recession_liquidity_stress: TLT / delta=-0.02529117 / turnover=10.000002% / reason=취약성 기여가 큰 보유자산이 확인되어 단순 추가 헷지보다 TRIM_AND_HEDGE가 우선입니다.
  - expected_effect: 취약성 0.0253 감소; CVaR 0.27%p 개선; MDD 1.99%p 개선; stress 0.00%p 개선; Sharpe 0.03 악화
  - formal_action_gap: FORMAL_ACTION 제외 사유: 기존 추천 gate 상태가 REFERENCE_ONLY입니다. stress/backtest, CVaR·MDD 안정성, 거래 제약 검증이 추가로 충족되어야 정식 추천으로 올릴 수 있습니다.
- REVIEW_ACTION · TRIM_AND_HEDGE · usdkrw_fx_korea: TLT / delta=-0.03857156 / turnover=10.000002% / reason=취약성 기여가 큰 보유자산이 확인되어 단순 추가 헷지보다 TRIM_AND_HEDGE가 우선입니다.
  - expected_effect: 취약성 0.0386 감소; CVaR 0.12%p 개선; MDD 1.70%p 개선; stress 0.01%p 개선; Sharpe 0.00 개선
  - formal_action_gap: FORMAL_ACTION 제외 사유: 기존 추천 gate 상태가 REFERENCE_ONLY입니다. stress/backtest, CVaR·MDD 안정성, 거래 제약 검증이 추가로 충족되어야 정식 추천으로 올릴 수 있습니다.
- REVIEW_ACTION · TRIM_AND_HEDGE · geopolitical_supply_chain: GLD / delta=-0.0464778 / turnover=10.000002% / reason=상위 sleeve 커버리지 이후 남은 후보 중 상태, 개선폭, turnover 기준으로 선택했습니다.
  - expected_effect: 취약성 0.0465 감소; CVaR 0.25%p 개선; MDD 1.53%p 개선; stress 0.00%p 개선; Sharpe 0.00 악화
  - formal_action_gap: FORMAL_ACTION 제외 사유: 기존 추천 gate 상태가 REFERENCE_ONLY입니다. stress/backtest, CVaR·MDD 안정성, 거래 제약 검증이 추가로 충족되어야 정식 추천으로 올릴 수 있습니다.
- REVIEW_ACTION · TRIM_AND_HEDGE · geopolitical_supply_chain: TLT + IAU / delta=-0.04426318 / turnover=10.000002% / reason=상위 sleeve 커버리지 이후 남은 후보 중 상태, 개선폭, turnover 기준으로 선택했습니다.
  - expected_effect: 취약성 0.0443 감소; CVaR 0.26%p 개선; MDD 1.76%p 개선; stress 0.00%p 개선; Sharpe 0.02 악화
  - formal_action_gap: FORMAL_ACTION 제외 사유: 기존 추천 gate 상태가 REFERENCE_ONLY입니다. stress/backtest, CVaR·MDD 안정성, 거래 제약 검증이 추가로 충족되어야 정식 추천으로 올릴 수 있습니다.
- REVIEW_ACTION · TRIM_AND_HEDGE · geopolitical_supply_chain: TLT + GLD / delta=-0.04417654 / turnover=10.000002% / reason=상위 sleeve 커버리지 이후 남은 후보 중 상태, 개선폭, turnover 기준으로 선택했습니다.
  - expected_effect: 취약성 0.0442 감소; CVaR 0.26%p 개선; MDD 1.76%p 개선; stress 0.00%p 개선; Sharpe 0.02 악화
  - formal_action_gap: FORMAL_ACTION 제외 사유: 기존 추천 gate 상태가 REFERENCE_ONLY입니다. stress/backtest, CVaR·MDD 안정성, 거래 제약 검증이 추가로 충족되어야 정식 추천으로 올릴 수 있습니다.
- REVIEW_ACTION · TRIM_AND_HEDGE · geopolitical_supply_chain: IEF + IAU / delta=-0.04319094 / turnover=10.000002% / reason=상위 sleeve 커버리지 이후 남은 후보 중 상태, 개선폭, turnover 기준으로 선택했습니다.
  - expected_effect: 취약성 0.0432 감소; CVaR 0.25%p 개선; MDD 1.73%p 개선; stress 0.00%p 개선; Sharpe 0.02 악화
  - formal_action_gap: FORMAL_ACTION 제외 사유: 기존 추천 gate 상태가 REFERENCE_ONLY입니다. stress/backtest, CVaR·MDD 안정성, 거래 제약 검증이 추가로 충족되어야 정식 추천으로 올릴 수 있습니다.
- REVIEW_ACTION · TRIM_AND_HEDGE · geopolitical_supply_chain: IEF + GLD / delta=-0.0431043 / turnover=10.000002% / reason=상위 sleeve 커버리지 이후 남은 후보 중 상태, 개선폭, turnover 기준으로 선택했습니다.
  - expected_effect: 취약성 0.0431 감소; CVaR 0.25%p 개선; MDD 1.73%p 개선; stress 0.00%p 개선; Sharpe 0.02 악화
  - formal_action_gap: FORMAL_ACTION 제외 사유: 기존 추천 gate 상태가 REFERENCE_ONLY입니다. stress/backtest, CVaR·MDD 안정성, 거래 제약 검증이 추가로 충족되어야 정식 추천으로 올릴 수 있습니다.

## Action Type Coverage
- ADD_HEDGE: present, not selected, count=1, selected=0 · 기존 보유자산을 유지하면서 헷지를 더하는 후보입니다.
  - not_selected_reason: 후보는 있었지만 selected action plan은 top vulnerability 다양성과 개선도 순서를 우선해 다른 액션을 선택했습니다.
- TRIM_AND_HEDGE: present, selected, count=59, selected=10 · 취약성 원인 보유자산을 일부 줄이고 헷지를 더하는 후보입니다.
- REPLACE_SLEEVE: absent, not selected, count=0, selected=0 · 대체 proxy가 이미 보유 중이거나 해당 sleeve를 방어하지 않아 생성되지 않았습니다.
  - not_selected_reason: REPLACE_SLEEVE 후보가 없습니다. 대체 proxy가 이미 보유 중이거나, 해당 sleeve를 방어하지 못했거나, bounded turnover/집중도 제약 안에서 취약성을 줄이지 못했습니다.
- NO_ACTION: absent, not selected, count=0, selected=0 · 모든 취약 sleeve에서 최소 하나 이상의 bounded action 후보가 생성되어 NO_ACTION row가 필요하지 않았습니다.
  - not_selected_reason: 모든 취약 sleeve에서 최소 하나 이상의 bounded action 후보가 생성되어 NO_ACTION row가 필요하지 않았습니다.

## Next Validation Needed
- REVIEW_ACTION을 FORMAL_ACTION으로 올리려면 기존 formal recommendation gate, stress/backtest 근거, CVaR/MDD 안정성, 거래 제약 검증이 모두 충족되어야 합니다.
- FORMAL_ACTION이 없을 때는 실행 추천이 아니라 실행 전 검토용 시뮬레이션으로만 해석해야 합니다.
