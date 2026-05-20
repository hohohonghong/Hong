# Daily Market State Summary

- 기준일: `2026-05-19`
- 상태 분포: STRESS 1 / ACTIVE 3 / WATCH 3 / OFF 3
- contract note: this scenario vector is diagnostic-only market-state evidence, not a buy/sell, hedge, or portfolio recommendation.
- 해석 범위: Phase 4 정형 데이터 기반 설명 요약입니다. 포트폴리오 자동 변경 신호가 아니라 시장 상태 해석 보조 신호입니다.
- confidence 읽는 법: 현재 값은 데이터 coverage와 신호 breadth 기반의 임시 confidence proxy입니다. 뉴스/정책문 병합 confidence는 Phase 6 범위입니다.

## 팩터 압축 요약
- 추가 지표는 개별 신호를 그대로 나열하지 않고 8개 팩터로 압축해 시나리오 판단을 보조합니다.
- `Rates Pressure` — 리스크 팩터, ELEVATED (score=82.44, confidence=91.65, coverage=1.00)
  - 해석: 장기채·중기채 가격 하락과 장단기 구간 부담을 통해 금리 압박을 봅니다.
- `Credit Stress` — 리스크 팩터, ELEVATED (score=81.91, confidence=79.03, coverage=1.00)
  - 해석: 하이일드·투자등급 신용자산과 변동성으로 스트레스 확산 여부를 봅니다.
- `USD / KRW Pressure` — 리스크 팩터, ELEVATED (score=72.92, confidence=62.90, coverage=0.85)
  - 해석: 달러 강세와 원화 약세가 한국 투자자 관점의 리스크로 작동하는지 봅니다.
- `Inflation / Commodity Pressure` — 리스크 팩터, ELEVATED (score=68.13, confidence=74.04, coverage=1.00)
  - 해석: 유가·원자재·에너지 섹터와 물가연동채 반응으로 재인플레 압력을 봅니다.

## 전체 시나리오 스냅샷
- 모든 시나리오의 최신 상태와 대표 driver를 함께 표시합니다.
- `higher_for_longer_long_rate_shock` Higher-for-Longer / Long-Rate Shock · 장기금리 부담장: STRESS, score=78.85, confidence=84.79, coverage=1.00
  - supporting: TLT 20d return (+0.3270, z=-1.87) | TLT minus SHY 20d return (+0.1347, z=-1.80) | HYG 20d return (+0.1242, z=-1.66)
  - offsetting: -
- `usd_strength_krw_weakness` USD Strength / KRW Weakness · 달러강세/원화약세장: ACTIVE, score=73.69, confidence=64.30, coverage=0.87
  - supporting: USD/KRW level (+0.2607, z=+1.74) | USD/KRW 20d return (+0.1505, z=+1.20) | FXI 20d return (+0.0576, z=-0.77)
  - offsetting: -
- `stagflation_reinflation_energy_shock` Stagflation / Reinflation / Energy Shock · 물가·에너지 재상승장: ACTIVE, score=64.46, confidence=72.57, coverage=1.00
  - supporting: TLT 20d return (+0.1869, z=-1.87) | USO 20d return (+0.1256, z=+0.84)
  - offsetting: TIP 20d return (-0.1024, z=-1.37)
- `china_trade_fragmentation_shock` China / Trade Fragmentation Shock · 중국·무역분절 충격장: ACTIVE, score=59.53, confidence=55.85, coverage=0.83
  - supporting: FXI 20d return (+0.1152, z=-0.77) | USD/KRW 20d return (+0.0903, z=+1.20) | FXI minus SPY 20d return (+0.0810, z=-1.62)
  - offsetting: -
- `acute_global_stress_liquidity_crunch` Acute Global Stress / Liquidity Crunch · 급성 리스크오프/유동성 경색장: WATCH, score=59.36, confidence=65.32, coverage=0.92
  - supporting: HYG 5d return (+0.1392, z=-1.86) | LQD 5d return (+0.1000, z=-2.14)
  - offsetting: TLT 5d return (-0.0988, z=-1.98)
- `geopolitical_escalation_supply_shock` Geopolitical Escalation / Supply Shock · 지정학 확전·공급충격장: WATCH, score=49.19, confidence=68.23, coverage=1.00
  - supporting: USD/KRW 20d return (+0.0602, z=+1.20) | Geopolitical event overlay score (+0.0250, z=+1.00)
  - offsetting: PPA minus SPY 20d return (-0.1255, z=-1.67) | GLD 5d return (-0.1132, z=-1.51)
- `soft_landing_goldilocks` Soft Landing / Goldilocks · 우호적 위험선호장: WATCH, score=46.27, confidence=60.25, coverage=0.87
  - supporting: QQQ 20d return (+0.1325, z=+1.06)
  - offsetting: TLT 20d return (-0.1402, z=-1.87) | USD/KRW 20d return (-0.0903, z=+1.20)
- `semiconductor_ai_cycle_shock` Semiconductor / AI Cycle Shock · AI·반도체 사이클 충격장: OFF, score=38.15, confidence=47.89, coverage=0.75
  - supporting: USD/KRW 20d return (+0.0602, z=+1.20)
  - offsetting: SOXX 20d return (-0.0960, z=+0.77) | SOXX minus SPY 20d return (-0.0811, z=+0.81)
- `korea_domestic_financial_stress` Korea Domestic Financial Stress · 한국 내수 금융스트레스장: OFF, score=26.81, confidence=44.53, coverage=0.55
  - supporting: USD/KRW 20d return (+0.0602, z=+1.20)
  - offsetting: Korea AA- 3Y credit spread (-0.1579, z=-1.58) | Korea CP-CD 91D spread (-0.0854, z=-1.71)
- `slowdown_recession_deflation_risk` Slowdown / Recession / Deflation Risk · 경기둔화/침체 우려장: OFF, score=20.94, confidence=68.64, coverage=0.92
  - supporting: -
  - offsetting: TLT 60d return (-0.2500, z=-2.14) | IEF 60d return (-0.1000, z=-3.32) | QQQ 60d return (-0.0890, z=+1.19)

## 1. Higher-for-Longer / Long-Rate Shock · 장기금리 부담장
- 관점 lens: `us_global` (관련: `korea_semiconductor|fx_krw`)
- 상태 해석: `STRESS` (raw: `STRESS`) — 강한 스트레스 구간입니다. 단기 리스크 해석을 보수적으로 봐야 합니다.
- 수치: score=78.85 | confidence=84.79(높음) | coverage=1.00(충분)
- 장세 설명: 장기금리와 달러 강세 부담이 채권·성장주·신용자산을 압박하는 장세입니다. 고밸류 성장주와 반도체 factor 민감도를 점검합니다.
- 사용자 관점: 장기채와 성장주처럼 금리에 민감한 자산의 해석을 보수적으로 봐야 합니다.
- 주요 지지 근거:
  - `TLT 20d return` — 지지 (contribution=+0.3270, normalized=-1.8688)
  - `TLT minus SHY 20d return` — 지지 (contribution=+0.1347, normalized=-1.7960)
  - `HYG 20d return` — 지지 (contribution=+0.1242, normalized=-1.6556)
- 반대/완화 근거:
  - 상위 영향 지표 기준 뚜렷한 반대 신호는 제한적입니다.
- 주의점: 현재 정형 proxy 기준으로 큰 결측 caveat는 없습니다.

## 2. USD Strength / KRW Weakness · 달러강세/원화약세장
- 관점 lens: `fx_krw` (관련: `korea_market`)
- 상태 해석: `ACTIVE` (raw: `ACTIVE`) — 활성 구간입니다. 현재 시장을 설명하는 주요 상태로 볼 수 있습니다.
- 수치: score=73.69 | confidence=64.30(중간) | coverage=0.87(충분)
- 장세 설명: 달러가 강하고 원화가 약해져 KRW 기준 투자자의 환율 리스크가 커지는 장세입니다. 한국 자산과 USD 노출의 역할을 분리해 봅니다.
- 사용자 관점: KRW 기준 투자자는 환율 노출과 USD 방어력을 함께 점검해야 합니다.
- 주요 지지 근거:
  - `USD/KRW level` — 지지 (contribution=+0.2607, normalized=+1.7377)
  - `USD/KRW 20d return` — 지지 (contribution=+0.1505, normalized=+1.2041)
  - `FXI 20d return` — 지지 (contribution=+0.0576, normalized=-0.7681)
- 반대/완화 근거:
  - 상위 영향 지표 기준 뚜렷한 반대 신호는 제한적입니다.
- 주의점: 현재 정형 proxy 기준으로 큰 결측 caveat는 없습니다.

## 3. Stagflation / Reinflation / Energy Shock · 물가·에너지 재상승장
- 관점 lens: `us_global` (관련: `fx_krw`)
- 상태 해석: `ACTIVE` (raw: `ACTIVE`) — 활성 구간입니다. 현재 시장을 설명하는 주요 상태로 볼 수 있습니다.
- 수치: score=64.46 | confidence=72.57(높음) | coverage=1.00(충분)
- 장세 설명: 성장 부담이 있는데 유가·원자재·인플레이션 압력이 다시 커지는 장세입니다. 에너지/원자재 수혜와 장기채 부담을 함께 봅니다.
- 사용자 관점: 원자재·물가 압력과 성장 부담이 동시에 나타나는지 확인해야 합니다.
- 주요 지지 근거:
  - `TLT 20d return` — 지지 (contribution=+0.1869, normalized=-1.8688)
  - `USO 20d return` — 지지 (contribution=+0.1256, normalized=+0.8374)
- 반대/완화 근거:
  - `TIP 20d return` — 완화/반대 (contribution=-0.1024, normalized=-1.3655)
- 주의점: 현재 정형 proxy 기준으로 큰 결측 caveat는 없습니다.

## 데이터 커버리지 메모
- quality status: `DEGRADED`
- 정렬 기준일: `2026-05-19`
- anchor coverage: 35/44 (79.5%)
- expected/loaded tickers: 44/44
- 70개 자산 breadth 원천 ticker 수: 0
- synthetic basket latest: `AI_BASKET=660.17 (AMD|AVGO|GOOGL|MSFT|NVDA), KR_SEMIS_BASKET=807.03 (000660.KS|005930.KS), KR_FINANCIAL_BASKET=375.65 (032830.KS|055550.KS|105560.KS), KR_CONSTRUCTION_BASKET=232.75 (000720.KS|006360.KS|047040.KS)`
- low-frequency indicators forward-filled: `KR_CREDIT_SPREAD_AA3Y_GOV3Y:last=2026-04-30, stale=19d, source_quality=seed, KR_CP_CD_SPREAD_91D:last=2026-04-30, stale=19d, source_quality=seed, KR_HOUSEHOLD_LOAN_YOY:last=2026-04-30, stale=19d, source_quality=seed, GEOPOLITICAL_EVENT_OVERLAY:last=2026-05-11, stale=8d, source_quality=manual`
- low-frequency/event sources: `C:\Users\석민\Documents\cau_2026_ss\금융인공지능실습1\scenario_research\inputs\market_state_external_indicators.csv, C:\Users\석민\Documents\cau_2026_ss\금융인공지능실습1\scenario_research\outputs\events\event_overlay_daily_event-refresh-20260518.csv, C:\Users\석민\Documents\cau_2026_ss\금융인공지능실습1\scenario_research\outputs\events\event_overlay_daily_event-refresh-20260519.csv, C:\Users\석민\Documents\cau_2026_ss\금융인공지능실습1\scenario_research\outputs\events\event_overlay_daily_event-refresh-20260519ralph.csv, C:\Users\석민\Documents\cau_2026_ss\금융인공지능실습1\scenario_research\outputs\events\event_overlay_daily_event-refresh-20260519ralph2.csv, C:\Users\석민\Documents\cau_2026_ss\금융인공지능실습1\scenario_research\outputs\events\event_overlay_daily_event-refresh-20260520.csv, C:\Users\석민\Documents\cau_2026_ss\금융인공지능실습1\scenario_research\outputs\events\event_overlay_daily_event-refresh-20260520e2e.csv, C:\Users\석민\Documents\cau_2026_ss\금융인공지능실습1\scenario_research\outputs\events\event_overlay_daily_event-refresh-20260520e2efast.csv, C:\Users\석민\Documents\cau_2026_ss\금융인공지능실습1\scenario_research\outputs\events\event_overlay_daily_phase5-wave2-combined-20260514.csv, C:\Users\석민\Documents\cau_2026_ss\금융인공지능실습1\scenario_research\outputs\events\event_overlay_daily_phase5-wave2-stress-20260514.csv, C:\Users\석민\Documents\cau_2026_ss\금융인공지능실습1\scenario_research\outputs\events\event_overlay_daily_v2-geopolitical-seed.csv`
- anchor date에 없어 제외된 ticker: `000660.KS, 000720.KS, 005930.KS, 006360.KS, 032830.KS, 047040.KS, 055550.KS, 105560.KS, ^KS200`
- 이 summary는 데이터 coverage가 낮거나 특정 핵심 ticker가 빠진 경우 보수적으로 해석해야 합니다.
