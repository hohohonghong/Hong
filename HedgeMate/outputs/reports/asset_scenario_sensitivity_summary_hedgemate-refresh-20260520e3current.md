# HedgeMate 시나리오 민감도 요약

- run_id: hedgemate-refresh-20260520e3current
- data_version: 20260520
- scenario_vector: `scenario_research\outputs\scenario_vectors\current_scenario_vector_final-refresh-20260520e2efast.csv`
- as_of_date: 2026-05-19
- selected_by: explicit_path
- scenario_vector_candidates: 1
- 해석: 현재 장세: 장기금리 부담장(STRESS, us_global, score=78.845293) / 달러강세/원화약세장(ACTIVE, fx_krw, score=73.685808) / 물가·에너지 재상승장(ACTIVE, us_global, score=64.455958)
- row_count: 700

## Lens 분포
- china_asia: 70
- fx_krw: 70
- geopolitical: 70
- korea_market: 70
- korea_semiconductor: 70
- us_global: 350

## Scenario 분포
- acute_global_stress_liquidity_crunch: 70
- china_trade_fragmentation_shock: 70
- geopolitical_escalation_supply_shock: 70
- higher_for_longer_long_rate_shock: 70
- korea_domestic_financial_stress: 70
- semiconductor_ai_cycle_shock: 70
- slowdown_recession_deflation_risk: 70
- soft_landing_goldilocks: 70
- stagflation_reinflation_energy_shock: 70
- usd_strength_krw_weakness: 70

## v2 Evidence 분포
- sensitivity_version: v3
- gate_eligible rows: 140
- method `rolling_beta`: 700
- evidence_quality `high`: 420
- evidence_quality `low`: 70
- evidence_quality `medium`: 210
- source_quality `manual`: 70
- source_quality `market`: 560
- source_quality `seed`: 70

## Active adverse scenario
- 장기금리 부담장
- 달러강세/원화약세장
- 물가·에너지 재상승장
- 중국·무역분절 충격장
- 급성 리스크오프/유동성 경색장
- 지정학 확전·공급충격장

## Trade-gated adverse scenario
- 장기금리 부담장
- 물가·에너지 재상승장

## 주의
- 현재 민감도 v2는 가격 기반 beta/stress feature와 구조 태그를 결합합니다.
- positive scenario_beta는 해당 시나리오 활성 시 취약도가 커지는 방향, negative는 방어/상쇄 가능성을 의미합니다.
- WATCH/manual/seed 시나리오는 기본적으로 context로만 표시하며 trade gate에는 사용하지 않습니다.
