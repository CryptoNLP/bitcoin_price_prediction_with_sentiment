# bitcoin_price_prediction_with_sentiment

## Goal
비트코인 가격기반예측 모델에 SNS 감성 점수를 Feature로 추가하여 예측 성능을 높이는 프로젝트 <br>
Base Model: OHLCV + fluct + MA + ETC <br>
Sentiment Model: OHLCV + fluct + MA + ETC + sentiment Feature <br>
Sentiment Model > Base Model

## Data
1. price data: Binance
2. SNS text data: Reddit r/Bitcoin - daily discussion, r/CryptoCurrency - daily discussion

## Sentiment Analysis
- Using VADER
- 비트코인 커뮤니티 기반 빈도수 Top1000 어휘중 정성적인 평가하에 Lexicon추가
- 기존 Lexicon에 crypto 관련 어휘 추가
- 어휘추가는 빈도수 기준 상위 1000개 단어들중 선별하여 VADER 방식으로 

## 
## Confusion Matrix

![image](https://user-images.githubusercontent.com/28949162/157691854-061ee33e-ba0a-429f-8a8e-144ea4576060.png)

1. Origin

![image](https://user-images.githubusercontent.com/28949162/157691931-d350fbd9-ef61-4ba0-b7d1-109ad76b6c34.png)

2. V1: Bitcoin subreddit의 daily discussion comment에서 빈도수 Top1000개 단어 중 정성적 판단하에 필터링 후 추가

![image](https://user-images.githubusercontent.com/28949162/157691964-65be3f68-52ff-457b-ab54-31b5a8fea846.png)

3. V2: Bitcoin subreddit의 daily discussion comment에서 1000개의 문장들 잘못 분류한 것 cross checking 하면서 단어 추가, 두 단어 이상으로 결합한 단어

![image](https://user-images.githubusercontent.com/28949162/157691983-63ef198b-d20c-45f8-93e4-9e77defcece2.png)

4. V3: cryptocurrency subreddit에서 추출한 문장 중 잘못 분류한 문장들을 읽어본 후 직접 필요한 단어 추가

## Model
LSTM

## Problem
- Sentiment Feature를 추가해도 성능이 좋아지지 않음.
- Filtering
- 


## ToDo List
1. CryptoCurrency Subreddit 크롤링 과정에서 결측치가 많이 생기는 것 해결
2. 대댓글 수집
3. 필터링 문제
4. 

## 의문점
1. Base Model 성능 이슈
2. Filtering. Opinion Finder







