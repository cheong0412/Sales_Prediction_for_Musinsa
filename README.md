# 회귀 모델을 이용한 무신사 판매량 예측

## 목차
  - [프로젝트 기본 정보](#프로젝트-기본-정보)
  - [프로젝트 개요](#프로젝트-개요)
  - [프로젝트 설명](#프로젝트-설명)
  - [분석 결과](#분석-결과)
  - [기대 효과](#기대-효과)

## 프로젝트 기본 정보
- 프로젝트 이름: 회귀 모델을 이용한 무신사 판매량 예측
- 프로젝트 기간: 2023.01
- 프로젝트 참여인원: 5명
- 사용 언어: Python

## 프로젝트 개요
- 국내 이커머스 시장은 5년 이상 꾸준히 성장하고 있음.
- 그 중 패션 분야에서 무신사가 다른 앱들을 제치고 1위로 차지하며 트렌드로 자리 잡음.
- 따라서 패션앱 시장에서 독보적인 위치를 가진 무신사 제품 정보를 크롤링하여 제품의 1년 누적 판매량을 예측해보고자 함.
![image](https://github.com/cheong0412/Sales_Prediction_for_Musinsa/assets/153011230/662deeb2-9387-4d6b-b5e8-477a5e073153)

## 프로젝트 설명


## 분석 결과
### 1. 5개 회귀 모델 성능 비교
![image](https://github.com/cheong0412/Sales_Prediction_for_Musinsa/assets/153011230/889d1552-e1f7-4e19-abe6-28e9fcdadc03)

### 2. 최종 모델 선정: Multiple Regression + Lasso
- R2_score 만으로 보았을 때 설명력이 가장 높은 모델은 아니지만, 종합적인 성능지표를 비교했을 때 우수한 것으로 판단
- 트레인, 테스트 데이터의 과적합을 가장 효과적으로 해결한 모델
- - Lasso의 alpha값 도출 그래프 참고
![image](https://github.com/cheong0412/Sales_Prediction_for_Musinsa/assets/153011230/457a58fb-fed2-4f0c-a3ac-f4d2465f3416)

- - train, test set의 RMSE
![image](https://github.com/cheong0412/Sales_Prediction_for_Musinsa/assets/153011230/99c07a78-f46c-41e2-9cc3-9277fb06a474)
![image](https://github.com/cheong0412/Sales_Prediction_for_Musinsa/assets/153011230/5dcd99b5-bc95-42eb-a07f-6041eca9a662)

## 기대 효과
- 효율적인 재고 관리가 가능하여 재고로 인한 손실을 최소화할 수 있음.
- 마케팅 예산을 효과적으로 할당할 수 있음.
- 걍젱사의 활동에 더 민감하게 대응할 수 있음.
