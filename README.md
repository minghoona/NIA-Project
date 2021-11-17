# 2021 공공빅데이터 청년 인턴십 데이터 해커톤
주제 : 장흥군청 정보공개청구 민원 수요 패턴 분석
-------------
* 소속 : 한국지능정보사회진흥원(NIA)
* 부서명 : 공공데이터본부 데이터기반행정팀 
* 팀원 : [김명훈](https://github.com/minghoona) [김영욱](https://github.com/kjfms) [유혜림](https://github.com/YuHyeRim) [장건희](https://github.com/kuma987)
* 기간 : 2021.11.01 ~ 2021.??.??
* 분석도구 : python, R, Excel
* 분석기법 : 텍스트마이닝, TF-IDF

* * *

## 1. 분석 개요
- #### 2020년 장흥군청 정보공개청구 민원 데이터를 활용해 민원 신청의 현황, 추이 등을 다양한 방면에서 분석 진행
  - 정보공개 신청 현황을 여러 유형별(월별, 요일별, 부서별 등)로 분석 진행
  - 전체 주요 민원 키워드 및 부서별 주요 민원 키워드의 현황 및 추이 분석 진행 

## 2. 분석 데이터
- #### 2020년 장흥군청 정보공개청구 민원 데이터

## 3. 민원 현황 및 유형 분석
### 분석 프로세스
<p align="center"><img src =https://user-images.githubusercontent.com/82136585/142090397-6ba31dbb-241e-42e8-acb2-903670f2e7a9.png>

1)	파생변수 생성
장흥군청에서 요구한 형태로 데이터를 분석하기 위해 필요한 파생변수를 생성한다.

2)	변수별 민원 건수 파악
2020년 장흥군청 정보공개청구 민원 데이터에서, 장흥군청이 요구한 변수에 따라 민원건수를 집계한다. 변수별로 민원 건수를 집계하였을 때, 변수값이 누락된 경우 해당 민원을 제거한다.

3)	데이터 시각화
변수별로 집계된 데이터를 시각화하여 제시한다.

