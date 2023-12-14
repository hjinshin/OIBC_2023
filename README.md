# 2023 POSTECH X DERShare OIBC 태양광 발전입찰 경진대회
![img.png](img.png)
[2023 POSTECH OIBC CHALLENGE 태양광 발전량 예측 경진대회](https://o.solarkim.com/cmpt2023)에서 대상 (1등/73팀)을 받은 김최신이팀의 소스코드 및 발표자료

## 김최신이 팀
김시형(경북대학교 수학과)    

최지원(경북대학교 수학과)    

신형진(경북대학교 컴퓨터학부)  

이한빈(경북대학교 수학과)

## 대회 소개
* 대회 미션: 다종 예측 모형들의 특성을 파악하고 활용하여 예측 성능 향상이 가능한 앙상블 기법 개발  


* 대회 목표: 전날 기상 예측 데이터와 예측모델 5종의 발전량 예측 데이터를 활용하여 다음날 실제 태양광 발전소의 시간별 발전량 예측


* 대회 일정
    * 2023년 10월 22일 ~ 2023년 11월 11일: 사전 대회 기간 (태양광 발전량 예측 모델 구축 기간)
    * 2023년 11월 13일 ~ 2023년 11월 17일: 경진 대회 기간 (실제 태양광 발전량 예측)
    * 2023년 11월 28일: 발표 평가
    * 2023년 12월 01일: 시상식


## 디렉토리 구성
레포지토리 구성
```
root
│
├── README.md                                    # 디렉토리 안내 파일
│
├── 2023_OIBC_KCSL.pdf                           # 발표 자료
│
├── data/                                        # 데이터 폴더
│   ├── gens.csv                                 # 과거 발전량 데이터
│   ├── incentive.csv                            # 과거 모델별 획득 인센티브 데이터
│   ├── pred.csv                                 # 과거 모델별 발전량 예측 데이터
│   ├── weather_actual.csv                       # 과거 기상 데이터
│   ├── weather_forecast.csv                     # 과거 기상 예측 데이터
│   └──preporcessed/                             # 전처리된 데이터 폴더 (생략) 
└── notebooks/                                   # ipynb 파일 폴더
    ├── PreProcessing.ipynb                      # gens.csv, incentive.csv, pred.csv,
    │                                            weather_actual.csv, weather_forecast.csv 전처리 및 병합
    └── StackingRegression.ipynb                 # XGBoosting을 활용한 Stacking Regression 및 데이터 동화
```

## 코드 실행
1. ```notebooks/PreProcessing.ipynb```를 실행하여 gens.csv, incentive.csv, pred.csv, weather_actual.csv, weather_forecast.csv 전처리 및 병합 -> 전처리된 데이터는 data/preprocessed에 저장


2. ```notebooks/StackingRegression.ipynb```에 본인의 API_KEY를 넣고 실행하여 XGBoosting으로 데이터 학습, 데이터 동화, 예측, 제출

## 문의
모든 데이터는 대회 주관사인 [POSTECH 오픈이노베이션 빅데이터 센터 (OIBC)](https://oibc.postech.ac.kr/)에 문의