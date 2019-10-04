# Digital Trend Analyzer
'제 5회 L.point Big Data Competition' 공모전 

### 주제

Digital Trend Analyzer (부제: 온라인 행동 기반 트렌드 예측)

### 세부 과제

1. 주요 상품군별 온라인 선호지수 생성
2. 상품군별 수요 트렌드 예측 및 인사이트 도출
3. 1.과2.를 활용한 신규 서비스 제안

### 분석 방향
0. 데이터 전처리
- 구매 데이터에서 6개월 내 30건 이상 팔린 상품만 선별하여 분석에 사용 \
(Over30: 30건 이상 팔린 데이터, Under30 : 30건 미만 팔린 데이터)

1. 주요 상품군별 온라인 선호지수 생성
- '같은 고객이라도 각 상품을 대하는 태도는 다르다'는 점에서 착안하여 '페이지 탐색 시간'과
'히트 수'의 조합으로 세 개의 행동 패턴을 만들어 상품을 분류하는 군집 분석 시행
- 소비자 구매 중심 데이터를 제품 중심의 데이터로 재구성한 뒤, 각 제품을 구매하는 소
비자들의 특성(여성 고객의 비율, 재구매 횟수 등)을 나타내는 여러 변수들 생성
- 검색 데이터를 활용하여 브랜드 파워 변수 생성
- 파생 변수들의 특성을 고려하여 L(Lotte Members), P(Product), O(Outer) 세 개의 카테고
리로 분류한 뒤 종합하여 선호지수 생성

2. 상품군별 수요 트렌드 예측 및 인사이트 도출
- P 지수를 수요에 가장 가까운 지수(반응 변수)로 설정하고 나머지 L 지수와 O 지수를
설명 변수로 설정하여 Random Forest를 이용하여 수요 트렌드 예측
- Under30에 있는 제품의 수요 트렌드를 예측하기 위해 제품명과 가장 가까운 10개의 Over30 제품 선택

3. 1.과2.를 활용한 신규 서비스 제안
- **선물 서비스 제안**
- 선물받을 대상 정보를 반영하는 적절한 제품을 군집별로 추천
- Under30에 있는 상품도 함께 추천
