# 쇼핑몰 리뷰 감성분석을 통한 감성 점수 계산 머신러닝
## 감성 점수 계산 방법
- 기존에 쇼핑 분야 한국어 감성 사전이 따로 구축되어 있는 것이 없어 Logistic 회귀 계수를 감성 사전으로 이용
- 해당 리뷰 문장의 각 감성 단어의 회귀 계수를 모두 더한 후 0과 10사이로 정규화
## 연구 목표 및 연구 방법
<img width="832" alt="image" src="https://github.com/0chaechae2/sentiment-score-analysis/assets/173161886/182393be-7acf-47b0-a591-55f4f82781bd">

## 분석 파일 목록 및 설명
### **1. sentiment_project_data_processing.ipynb & crawling.ipynb**  
데이터 전처리 및 토큰화 & 하나의 제품에 대한 별점 및 쇼핑 리뷰 크롤링 과정
### **2. sentiment_project_modeling.ipynb & sentiment_project_apply_crawling.ipynb & misclassified_data_sentimetscore.ipynb**  
모델링 및 모델 검증 & 긍정 클래스지만 모델이 부정으로 분류한 데이터 추출
- 용량이 커서 따로 올렸지만 2-2 파일들은 '2. sentiment_project_modeling.ipynb'파일에 이어서 붙여야 합니다.
### **3. wordcloud_frequency.ipynb & wordcloud_regression_coefficient.ipynb**  
시각화 과정 - 모델 적용 전 빈도수 기준 & 모델 적용 후 회귀 계수 기준
### **4. survey_refining.ipynb**  
Ground-truth 이상치 제거 과정

---

## 프로젝트 정보

- 경희대학교 머신러닝기초및응용 3조 팀 프로젝트 (2024년 1학기, 2024.05 ~ 2024.06)
- 팀: 김소륜, 김예진, 이채영 (3인)
- 원본 저장소: [0chaechae2/sentiment-score-analysis](https://github.com/0chaechae2/sentiment-score-analysis)

## 내 역할 (김소륜)

- 연구 배경과 선행연구 정리 (별점 대신 텍스트 감성 점수를 쓰는 근거)
- 나이브 베이즈(TF-IDF) 비교 모델 구현
- 배깅과 부스팅의 과적합 비교 분석
- 설문조사 검증 파트: 리뷰 선정, 대푯값 비교 방식 설계, 분석과 보고서 작성
- 워드클라우드 시각화 (빈도 기준, 회귀 계수 기준)
- 발표 후반부 담당

로지스틱 베이스라인과 하이퍼파라미터 튜닝은 이채영, 크롤링과 감성 점수 함수, 학습 곡선은 김예진이 맡았습니다.
