# Nestflow Pipeline

# 🏡 Nestflow Pipeline
> 전사 DW 구조 기반의 분양·임대 청약 추천 데이터 파이프라인 및 데이터 모델링 프로젝트  
> _Designed to mirror the mission and execution of Data Analytics Engineers (DAE)_

---

## 🎯 목적과 직무 연관성

이 프로젝트는 **Data Analytics Engineer 직무의 핵심 역할**을 학습 및 시뮬레이션하기 위해 설계. 수집·분석,  **전사적 데이터 전략 관점의 문제 해결 능력**을 기르고 보여주는 것이 목적.

### ✅ 전사 관점의 데이터 설계
- 청약 데이터를 통합하고, DW에 적재 가능한 **표준 스키마**를 정의합니다.
- `dim_house_type`, `fact_listing`, `fact_subscription` 등 **재사용 가능한 구조화된 DW 테이블**을 설계함으로써, 도메인 간 확장성과 신뢰성을 동시에 확보합니다.

### ✅ 품질과 신뢰 기반 데이터 제공
- 크롤링 및 ETL 과정에서의 **DQ 검증 로직**을 Great Expectations로 구현하고, Airflow DAG 내 자동화합니다.
- “누구나 신뢰하고 사용할 수 있는 Single Source of Truth”를 목표로, 데이터 정합성 및 이력관리(SCD)를 적용합니다.

### ✅ 도메인 오너십 기반 마트 설계
- `mart_active_listings`, `mart_user_eligibility` 등을 통해 **실제 추천·분석 업무에 즉시 활용 가능한 소비 마트**를 구성합니다.
- 도메인 팀(Growth, Pay, Ads)이 독립적으로 활용할 수 있도록 **표준 영역 vs 소비 영역을 명확히 분리**합니다.

### ✅ 제품/비즈니스 의사결정 지원
- 사용자별 청약 자격조건을 기반으로 한 **추천 알고리즘 Feature Store**를 설계합니다.
- 향후 A/B 실험, 광고 타게팅, 주택담보대출 전환 유도 등 **제품 KPI 연계 가능성**을 고려해 확장합니다.

---

## 역량 정리리

| 핵심 역량 | 이 프로젝트 내 실현 방식 |
|-----------|----------------------------|
| DW 구조 설계 | 공공 청약 통합 스키마 정의 및 계층화 모델링 |
| 데이터 표준화 | 분양/임대 공고의 필드 정규화 및 Glossary 정리 |
| 품질 관리 | DQ 룰 자동화, 메타 관리, 변경 이력 추적 |
| 파이프라인 운영 | Kafka → Spark → DW → Mart의 일관된 계층 구성 |
| AARRR 활용 | 관심 등록 클릭률, 추천→청약 신청율 등 지표 설계 |
| 협업 관점 설계 | DW 레벨에서 Cross-domain 연결 가능하도록 설계 (`user_id`, `listing_id` 중심 설계) |

