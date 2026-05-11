# MES 내 AI 제조 예지보전 기능 개발 — 제안 분석 로그

> 생성일: 2026-05-11
> 공고 URL: https://www.wishket.com/project/155235/

## 1. 공고 파싱 결과

```yaml
job:
  title: "MES 내 AI 제조 예지보전 기능 개발 (화장품 제조공장)"
  category: "AI 모델 구축 / 데이터 분석·BI / 내부 시스템 연동"
  budget_range: "25,000,000원"
  duration: "60일 (착수 후 2개월 이내)"
  client_team: "자사 PM 1명 + JAVA 개발자 2명"
  start_date: "2026-07-01 ~ 2026-07-08 (예정)"
  deadline: "2026-05-25"
  priority:
    - "1순위: 금액"
    - "2순위: 산출물 완성도"
    - "3순위: 일정 준수"
  tech_stack:
    - "Python (FastAPI, TensorFlow/PyTorch, SciPy)"
    - "Java Spring Boot (기존 MES)"
    - "MQTT / REST API / PostgreSQL"
    - "Grafana"
  scope:
    - "이기종 PLC(LS·Cimon·중국산) 데이터 수집 미들웨어"
    - "Spring Boot ↔ Python 데이터 연계 아키텍처"
    - "AI 모델 (진동 FFT, AutoEncoder 이상 탐지, LSTM 시계열 예측)"
    - "FastAPI 기반 AI 서버 + MES 연동 REST API"
    - "Grafana 실시간 대시보드"
    - "알람 시스템 (MES 팝업·SMS·경광등)"
  non_functional:
    - "호환성: 매뉴얼 부족 이기종 PLC 환경 대응 (미들웨어)"
    - "안정성: AI 서버 다운 시 재시도, 데이터 누락 방지"
  client_questions:
    - "개발 포트폴리오 제시 및 구축 경험 확인, 비용 사전 협의 후 진행"
  qualification:
    - "Python AI 모델링 + 백엔드 개발 경험"
    - "제조 현장 이기종 PLC 데이터 수집·파이프라인 구축 경험"
    - "서울/경기(오산·부천 1시간 30분 이내) 거주, 현장 미팅 가능"
  preferred:
    - "Java Spring Boot 연동 아키텍처 설계 경험"
    - "진동 데이터 FFT 분석 및 신호 처리 경험"
  deliverables:
    - "소스 코드 원본 (AI 모델 학습 코드 포함)"
    - "데이터 파이프라인 및 API 연동 문서"
    - "설치 및 운영 매뉴얼"
  job_post_url: "https://www.wishket.com/project/155235/"
  urls: []
  images: []
```

## 2. URL/이미지 분석

공고에 첨부된 URL 및 이미지 없음. 추가 분석 단계 스킵.

## 3. 실현 가능성 분석 (내부용)

### 프로젝트 유형
- **AI 모델 + 데이터 파이프라인 + 레거시 연동 + 하드웨어(PLC) 통합** 복합 프로젝트
- Feasibility 매트릭스 기준: "조건부 가능 ~ 주의" 구간 (+15~20% 버퍼)
- 주요 리스크: 중국산 PLC 매뉴얼 부재, 현장 검증 출장 부담, AI 모델 학습 데이터 가용성 불확실

### 공수 산정

| 영역 | 기본 공수 (AI 보조 없이) | AI 절감 후 (50%) |
|---|---|---|
| 기획/설계 | 5 M/D | 3 M/D |
| PLC 수집 미들웨어 (LS·Cimon·중국산) | 12 M/D | 7 M/D |
| 데이터 파이프라인 (PostgreSQL, MQTT, FFT) | 9 M/D | 5 M/D |
| AI 모델 (AutoEncoder + LSTM + FFT 규칙) | 10 M/D | 5 M/D |
| FastAPI AI 서버 + Spring Boot MES 연동 | 9 M/D | 5 M/D |
| Grafana 대시보드 | 5 M/D | 3 M/D |
| 알람 시스템 (팝업·SMS·경광등) | 4 M/D | 2 M/D |
| QA/배포/문서/현장 검증 | 6 M/D | 3 M/D |
| **소계** | **60 M/D** | **33 M/D** |

- AI 절감 후 공수: 33 M/D
- 버퍼(+20%, PLC 하드웨어 리스크): 39.6 M/D → 반올림 **40 M/D**
- 달력 일수 환산: 40 M/D × 7/5 ≈ 56일 + 현장 검증 여유 4일 = **60일**

### 판정
- 클라이언트 예상 기간(60일) 내 수행 가능
- 새 기간 제안 불필요 — 클라이언트 기간 그대로 사용
- 1순위 "금액" 우선순위 반영 — 22,500,000원 (예상의 90%)

## 4. 포트폴리오 매칭

### 매칭 점수 산정

| 프로젝트 | 기술 일치 (40%) | 도메인 (30%) | 기능 (20%) | 규모 (10%) | 총점 |
|---|---|---|---|---|---|
| **AI Agent** | 35 (Python/TS/MCP) | 28 (AI 도메인) | 18 (자동화/통합) | 9 | **90** |
| **Series-B** | 32 (OpenAI 통합) | 24 (B2B 백엔드) | 18 (AI 보고서·외부 시스템 연동) | 10 (200+ API) | **84** |
| **Harmony Link** | 30 (실시간/AI 분석) | 22 (모니터링 도메인) | 20 (실시간 데이터·다중 알람) | 8 | **80** |
| **P2P Funding** | 28 (Python/Django) | 18 (금융) | 14 (다중 외부 시스템) | 8 | **68** |
| **EZ-Approve** | 22 (NestJS) | 18 (B2B) | 16 (대시보드) | 9 | **65** |

### 최종 선정
1. **AI Agent** — AI 시스템 배포·운영 경험 (FastAPI AI 서버 구축의 직접 참조)
2. **Series-B** — OpenAI 통합 + 외부 시스템(VICS) 연동 패턴 (FastAPI ↔ Spring Boot 연동 패턴과 구조적으로 동일)
3. **Harmony Link** — 실시간 데이터 수집 + AI 분석 + 다중 채널 알람 (PLC→AI→MES 팝업/SMS/경광등 패턴과 거의 동일)

## 5. 최종 제안 요약

### 금액·기간
- **지원 금액**: 22,500,000원 (VAT 별도) — 클라이언트 예상의 90%
- **지원 기간**: 60일 — 클라이언트 예상 기간 그대로

### 핵심 제안 포인트
1. **이기종 PLC 대응 미들웨어** — LS/Cimon/중국산 PLC 어댑터 추상화, 매뉴얼 부재 PLC는 패킷 캡처·역분석으로 보강
2. **Spring Boot ↔ Python 양방향 연계 아키텍처** — MQTT 단방향 스트림 + REST API + 비동기 큐로 AI 서버 다운 대비
3. **AI 모델 단계적 고도화** — FFT 규칙 → AutoEncoder → LSTM 순차 적용, 데이터 부족 구간 대응
4. **운영 안정성** — 로컬 SQLite 버퍼(24시간), 헬스체크 자동 재시작, MQTT QoS 1+, DLQ
5. **유사 프로젝트 경험 기반 효율적 진행** — AI 시스템 배포·외부 시스템 연동·실시간 알람 구조 직접 경험 보유

### 1순위(금액) 대응 전략
- 클라이언트 예상의 90% 지원 (22,500,000원)으로 경쟁력 확보
- 명확한 산출물·단계 분리로 산출물 완성도(2순위) 확신 제공
- 60일 일정 그대로 수용하여 일정 준수(3순위)에 부담 없음을 어필

## 6. 최종 산출물

(8단계 완료 후 추가)
