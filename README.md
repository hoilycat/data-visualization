# 📊 Data Visualization Projects

데이터 수집, 정제, 시각화 프로젝트 모음입니다.
공공데이터와 직접 수집한 데이터를 분석하고 Tableau로 시각화했습니다.

---

## 🏛️ 01. 땅에서 박물관까지 — 유물은 어디서 와서 어디로 가는가

> "어떻게 지저분한 문화유산 데이터를 분석 가능한 구조로 바꾸는가"

### 데이터 수집
- Selenium 기반 국립중앙박물관 웹 크롤링
- 원본 데이터 9,000개+ 수집

### 데이터 정제 과정
- V1 ~ V21 반복 정제 (중복 제거, 결측 처리, 분류 기준 설계)
- 7개 대분류 규칙 직접 설계
- '기타' 항목 1,000개 → 288개로 축소
- 기계적 분류의 한계를 인정하고 Human-in-the-loop 방식으로 마무리
- 최종 정제 데이터: 5,259개

### 결과물
- [📊 Tableau 대시보드 보기](https://public.tableau.com/app/profile/kim.seoyoung6184/viz/_17675712350940/sheet6)

### Tech Stack
`Python` `Selenium` `Pandas` `Google Colab` `Tableau`

---

## 🛣️ 02. 고속도로 휴게소는 왜 사람이 많을까?

> "사람이 많이 찾는 휴게소, 소비가 집중되는 휴게소, 머무르는 시간이 긴 휴게소는 서로 다를 수 있다"

### 데이터
- 한국도로공사 공공데이터 5종 활용
  - 소비성향에 따른 휴게소 이용 특성
  - 인구통계특성에 따른 시설별 이용 특성
  - 시간대별 체류시간
  - 이용객 및 교통량 현황
  - 지역사회 개방형 휴게소 이용 특성

### 분석 방향 및 주요 발견

**시간대별 특성**
- 오전: 짧은 체류, 화장실·간단 휴식 목적
- 점심·저녁: 체류시간 증가, 식음료 비중 확대
- 야간: 이용객 감소 but 체류시간은 상대적으로 긺
→ 휴게소는 시간대에 따라 기능이 바뀌는 공간

**소비 행태**
- 식음료 소비 성향 이용자가 가장 큰 비중
- 기념품·특산물 소비는 특정 휴게소에 집중
- 고소비 성향 이용자 = 체류시간도 긺

**분야별 1위 도출 (3개 기준 분리)**
- 소비 규모 1위: 총 판매액 기준
- 체류시간 1위: 평균 체류시간 기준
- 소비 효율 1위: 판매액 ÷ 이용객 수 기준
→ 세 기준의 1위 휴게소가 모두 다름

### 결과물
- [📊 Tableau 대시보드 보기](https://public.tableau.com/app/profile/kim.seoyoung6184/viz/_17675283241480/sheet7)

### Tech Stack
`CSV` `Tableau`

---

## 🎡 03. 대한민국 사람들의 문화생활 엿보기

> "문화 역세권은 단순한 공간 개념이 아니라, 연령과 생활 단계에 따라 다르게 작동한다"

### 데이터
- 문화체육관광부 국민여가활동조사 데이터
- 문화시설 이용 현황, 문화행사 참여 데이터, 연령대별 문화생활 지표
- 엑셀 기반 정제 및 재구조화

### 분석 방향 (시간 × 지역 × 연령 3축)

**휴일에 무엇을 할까?**
- 평일 vs 휴일 문화시설 이용률 비교
- 문화 소비가 일상적 활동인지, 특별한 날에 집중되는지 분석

**지역마다 어떤 문화생활을 즐기는가?**
- 대도시 vs 지방 도시 문화생활 유형 차이
- 지역 특화 문화생활 존재 여부 및 문화 접근성 불균형

**나이에 따른 문화 역세권**
- 연령대별 선호 문화생활 유형과 시설 접근성 분석
- 문화 역세권이 연령/생활 단계에 따라 다르게 작동함을 확인

**대한민국 Top 5 문화생활 유형 도출**
- 앞선 분석 종합 → 가장 많이 즐기는 문화생활 상위 5가지

### 결과물
- [📊 Tableau 대시보드 보기](https://public.tableau.com/app/profile/kim.seoyoung6184/viz/_17675710943530/sheet5)

### Tech Stack
`Excel` `Tableau`

---

## 📛 04. 당신의 이름은 어떤 시대인가요? — 130년의 기록

> "집단주의에서 개인주의로, 종교 중심에서 대중문화 중심으로"

### 데이터
- 1880 ~ 2010년 미국 신생아 이름 공공데이터

### 분석 방향
기승전결 구조로 설계한 대시보드:
1. **기 (Intro):** Top 10 점유율 하락 + 고유 이름 폭발 → 획일화의 종말
2. **승 (Body 1):** Mary vs Jennifer, Riley & Taylor → 종교/성별 경계 변화
3. **전 (Body 2):** 이름 길이 변화, 마지막 글자 차트→ 스타일 변화
4. **결 (Outro):** John/Mary → Noah/Emma 세대교체

### 결과물
- [📊 Tableau 대시보드 보기](https://public.tableau.com/app/profile/kim.seoyoung6184/viz/_17681820857810/12)
- KMeans 군집화 실험 (이름 문자 벡터화)

### 📸 대시보드 미리보기

![01 시대의 변화 - Top10 점유율](https://raw.githubusercontent.com/hoilycat/data-visualization/main/04_names/screenshots/01_01_era_of_change.png)

![01 시대의 변화 - 시대에 따른 점유율](https://raw.githubusercontent.com/hoilycat/data-visualization/main/04_names/screenshots/01_02_era_of_change.png)

![01 시대의 변화 - 다양성의 폭발](https://raw.githubusercontent.com/hoilycat/data-visualization/main/04_names/screenshots/01_03_era_of_change.png)

![02 이름 감각의 변화 - 메리 vs 제니퍼](https://raw.githubusercontent.com/hoilycat/data-visualization/main/04_names/screenshots/02_01_shifting_name_sense.png)

![02 이름 감각의 변화 - 성별 경계 없는 이름](https://raw.githubusercontent.com/hoilycat/data-visualization/main/04_names/screenshots/02_02_shifting_name_sense.png)

![02 이름 감각의 변화 - 이름 길이와 소리](https://raw.githubusercontent.com/hoilycat/data-visualization/main/04_names/screenshots/02_03_shifting_name_sense.png)

![03 왕좌는 바뀌었습니다](https://raw.githubusercontent.com/hoilycat/data-visualization/main/04_names/screenshots/03_throne_change.png)

### Tech Stack
`Python` `Pandas` `scikit-learn` `Google Colab` `Tableau`
