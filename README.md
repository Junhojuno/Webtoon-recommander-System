# Webtoon Recommender System (웹툰 분석 & 추천시스템)
--- 
## About
: 웹툰의 소개글과 장르를 활용하여 웹툰 추천 시스템을 구현하는 프로젝트입니다.

### Overview
|  데이터 수집   | 추천 모델 | 추천 API  | 사용자 UI |
| ------------- |:-------------:|:---------:|:---------:|
| Naver/Daum 웹툰 리스트 크롤링 | 소개글 바탕으로 웹툰간 Similarity 계산 | Most similar를 제공하는 RESTful-API | Most similar한 웹툰을 추천해주는 기능 |
| Requests, bs4, python 패키지 활용 | TF-IDF + Cosine Similarity <br> python 패키지 활용 | Flask <br> python 패키지 활용 | Bootstrap theme |
### 데이터 수집
  - 대상웹툰
    - Naver : 745개
    - Daum : 765개
  - 웹툰의 기본정보 데이터(웹툰id, 좋아요수, 장르, 소개글)
  - 웹툰의 회차별 데이터(웹툰id, 회차no, 회차별 좋아요 수, 회차별 댓글 수, 회차별 image)
  - 웹툰의 회차별 댓글 데이터
  - 웹툰의 이미지 및 회차별 썸네일이미지

### 데이터 전처리
  - Naver와 Daum간 장르 통합이 되지 않는 문제점
  - `웹툰 소개글 + 장르` --> 새로운 Column 생성
  - TF-IDF Vectorize하여 전체 단어 Corpus 및 가중치 Matrix 생성 --> Model화
  
### 추천 모델
  - 사용자로부터 최근에 본 웹툰명을 Input으로 받는다.
  - 해당 input의 `웹툰 소개글 + 장르`을 Model로 Transform --> Vector화
  - (가중치 Matrix) x (Input Vector)의 Cosine similarity 출력

--- 
