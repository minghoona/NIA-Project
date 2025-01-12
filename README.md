# 2021 공공빅데이터 청년 인턴십 데이터 해커톤
주제 : 장흥군청 정보공개청구 민원 수요 패턴 분석
-------------
* 소속 : 한국지능정보사회진흥원(NIA)
* 부서명 : 공공데이터본부 데이터기반행정팀 
* 팀원 : [김명훈](https://github.com/minghoona) [김영욱](https://github.com/kjfms) [유혜림](https://github.com/YuHyeRim) [장건희](https://github.com/kuma987)
* 기간 : 2021.11.01 ~ 2021.11.16
* 분석도구 : python, R, Excel
* 분석기법 : 텍스트마이닝, TF-IDF

* * *

## 1. 분석 개요
- 2020년 장흥군청 정보공개청구 민원 데이터를 활용해 민원 신청의 현황, 추이 등을 다양한 방면에서 분석 진행
  - 정보공개 신청 현황을 여러 유형별(월별, 요일별, 부서별 등)로 분석 진행
  - 전체 주요 민원 키워드 및 부서별 주요 민원 키워드의 현황 및 추이 분석 진행 

* * *

## 2. 분석 데이터
- 2020년 장흥군청 정보공개청구 민원 데이터

* * *

## 3. 민원 현황 및 유형 분석
### (1) 분석 프로세스
<p align="center"><img src =https://user-images.githubusercontent.com/82136585/142090397-6ba31dbb-241e-42e8-acb2-903670f2e7a9.png>

#### 1)	파생변수 생성
장흥군청에서 요구한 형태로 데이터를 분석하기 위해 필요한 파생변수를 생성한다.

#### 2)	변수별 민원 건수 파악
원본 데이터에서 장흥군청이 요구한 변수에 따라 민원건수를 집계한다. 변수별로 민원 건수를 집계하였을 때, 변수값이 누락된 경우 해당 민원을 제거한다.

#### 3)	데이터 시각화
변수별로 집계된 데이터를 시각화하여 제시한다.

* * *
  
## 4. 민원 키워드 분석
### (1) 분석 프로세스
<p align="center"><img src =https://user-images.githubusercontent.com/82136585/142091689-aad6858d-694c-4a2c-b726-f7bc50d943e0.png>

#### 1) 민원 텍스트 수집

#### 2)	한글 형태소 분석기를 활용한 명사추출
Python 한글 형태소 분석기 Okt(Open Korean Text)를 활용해 앞선 과정에서 수집된 텍스트 내에서 2글자 이상의 명사를 추출하도록 한다.

#### 3)	1차 불용어 처리
기존의 민원분석 사례를 참고해 수집한 텍스트에서 추출된 2글자 이상의 명사에 대해 1차 불용어 제거를 하도록 한다. 참고한 불용어는 총 145개이다.
> ###### * ‘도시데이터표준분석모델 : 민원분석편(서울디지털재단, 2020)’
  
#### 4)	 TF-IDF 점수 계산
단어 별 언급빈도를 집계할 경우, 민원 키워드 파악에 있어 유의미하지 않지만 전체 민원에서 자주 언급되어 상위에 집계되는 단어들이 많아 핵심 키워드 선정에 어려움이 있다. 이에 전체 민원에서의 빈도 뿐만아니라, 개별 민원에서의 중요도를 고려해 특정 단어가 해당 문서내에서 얼마나 중요한지를 나타내는 통계적 수치인 TF-IDF가중치를 활용해 민원 키워드를 파악한다.

#### 5) 2차 불용어 처리
1차 불용어 처리에서 제거되지 않은 불용어를 직접 제거한다.

  
### (2) 분석 내용 및 방법
#### 1) 주요 민원 분석 
#### 가) 주요 민원 키워드 추출
원본데이터 전체를 대상으로 Python에서 제공하는 Okt모듈을 이용하여 각 민원에서 명사만을 추출하여 데이터 프레임을 구축한다.
#### 나) TF-IDF 점수 계산
앞서 추출한 키워드들을 대상으로 1차 불용어 처리 후 TF-IDF 점수를 계산한다.
#### 다) 2차 불용어 처리
1차 불용어 처리에서 제거되지 않은 불용어를 직접 제거한다.
  

#### 2) 보건소 민원 분석
가장 민원이 많은 총 3개의 부서에 대해서 분석을 진행하였다. 분석 과정은 모두 동일하므로 보건소의 분석 과정만 기재하고, 분석코드는 Code폴더에 업로드 하기로 한다. 
#### 가) 주요 민원 키워드 추출
처리부서가 '보건소'인 민원 데이터들을 대상으로 Python에서 제공하는 Okt모듈을 이용하여 각 민원에서 명사만을 추출하여 데이터 프레임을 구축한다.
#### 나) TF-IDF 점수 계산
앞서 추출한 키워드들을 대상으로 1차 불용어 처리 후 TF-IDF 점수를 계산한다.
#### 다) 2차 불용어 처리
1차 불용어 처리에서 제거되지 않은 불용어를 직접 제거한다. 


  
  

  
  
  

