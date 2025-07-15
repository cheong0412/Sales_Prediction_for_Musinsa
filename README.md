# MUSINSA 판매량 예측

## 목차
  - [프로젝트 기본 정보](#프로젝트-기본-정보)
  - [프로젝트 개요](#프로젝트-개요)
  - [프로젝트 설명](#프로젝트-설명)
  - [EDA](#EDA)
  - [분석 결과](#분석-결과)
  - [기대 효과](#기대-효과)
  - [Lesson & Learned](#lesson--learned)

## 프로젝트 기본 정보
- 프로젝트 이름: MUSINSA 판매량 예측
- 프로젝트 기간: 2024.01.02 ~ 2024.01.25
- 프로젝트 참여인원: 5명
- 사용 언어: Python

## 프로젝트 개요
- 국내 이커머스 시장은 5년 이상 꾸준히 성장하고 있음.
- 그 중 패션 분야에서 무신사가 다른 앱들을 제치고 1위로 차지하며 트렌드로 자리 잡음.
- 따라서 패션앱 시장에서 독보적인 위치를 가진 무신사 제품 정보를 크롤링하여 제품의 1년 누적 판매량을 예측해보고자 함.
<img width="1193" height="621" alt="1 개요" src="https://github.com/user-attachments/assets/393de178-9553-4f6e-b533-d0421e966af4" />
<img width="1127" height="625" alt="2 개요" src="https://github.com/user-attachments/assets/489915df-40ee-4bca-bd05-cfc893cca8b7" />


## 프로젝트 설명
무신사 상품과 리뷰 데이터를 기반으로 판매량을 예측하는 Lasso 회귀 모델을 개발한 프로젝트

## EDA
**Feature 탐색**
- 배송일(delivery_date)는 큰 영향이 없으나 현상만으로 봤을 때, 판매가 많이 일어나는 제품들의 경우 배송일이 10일 이내인 제품들이 많음.
- 종속 변수인 누적 판매량(buy)과 상관도가 높은 feature: 조회수(view), 좋아요(like), 리뷰수(review)
<img width="1158" height="290" alt="4 EDA" src="https://github.com/user-attachments/assets/6accae15-522a-4516-b550-af72e7ecf02b" />
<img width="870" height="287" alt="5 EDA" src="https://github.com/user-attachments/assets/ef5c348d-049c-4930-a53c-557870b3ded9" />
<img width="602" height="632" alt="6 EDA" src="https://github.com/user-attachments/assets/1d0e8e8d-5cd9-4562-be82-95431b3579a8" />

**리뷰 데이터를 활용한 등장 빈도수**
- stopword 반영, 100위까지 추출
- 등장 빈도수를 통해 실제 구매자들이 제품에 대한 평가를 내릴 때, 핏, 사이즈, 색감, 디자인, 재질 순으로 고려하는 인사이트를 도출함.
<img width="1270" height="367" alt="7 리뷰데이터 등장 빈도수" src="https://github.com/user-attachments/assets/30677036-2273-4dcf-be93-20983fdf4929" />

**리뷰 데이터를 활용한 워드 클라우드**
    - 150위까지추출
<img width="802" height="415" alt="8 리뷰데이터 워드 클라우드" src="https://github.com/user-attachments/assets/b0f7ba1f-3f19-47a9-aef3-8c292181634b" />


## 분석 결과
### 1. 5개 회귀 모델 성능 비교
<img width="717" height="615" alt="9 분석결과" src="https://github.com/user-attachments/assets/05ee7e3c-05ad-4401-bede-2f6293a5b237" />

### 2. 판매량 예측
<img width="723" height="642" alt="10 분석결과" src="https://github.com/user-attachments/assets/76ad8d85-2321-4754-913f-247597976240" />


## 기대 효과
- Lasso 모델을 사용하여 1년 간의 판매량을 예측함.
- 1년 간의 판매량 예측을 통해 다음과 같은 효과를 기대할 수 있음.
    - 향후 수요 파악이 가능함. 이를 기반으로 재고 최적화하여 효율적인 재고 관리가 가능하여 재고로 인한 손실을 최소화할 수 있음.
    - 마케팅 예산을 효과적으로 할당할 수 있음.
    - 경쟁사의 활동에 더 민감하게 대응할 수 있음. 경쟁사의 행보를 고려하여 판매 전략을 조정하고 시장에서의 경쟁 우위를 유지할 수 있음.

 
## Lesson & Learned
- 데이터 수집 과정에서 무신사 웹 내의 태그 값과 웹 구조 변동으로 인한 지속적인 코드 확인 및 수정이 필요하다는 것을 배움.
- 팀원들과 결측치 처리 기준에 대해 논의할 때, 명확한 기준과 근거가 필요하다는 것을 배움.
- 모델 결과가 과적합으로 판단되어 과적합 해결에 대한 방법론을 생각함.
- 모델 성능 결과 해석 방법에 대해 배움.
- 프로젝트 진행 시,  슬랙을 활용하여 팀원들과 실시간으로 진행 상황 및 코드 공유, 문제점 논의 등의 방법으로 협력하는 방을 배움.
