# Webtoon Recommender System

## About
: 웹툰의 소개글과 장르를 활용하여 웹툰 추천 시스템을 구현하는 프로젝트입니다.

## Implement

## Overview
|  데이터 수집   | 추천 모델 | 추천 API  | 사용자 UI |
|:-------------:|:-------------:|:---------:|:---------:|
| Naver/Daum 웹툰 리스트 크롤링 | 소개글 바탕으로 웹툰간 Similarity 계산 | Most similar를 제공하는 RESTful-API | Most similar한 웹툰을 추천해주는 기능 |
| Requests, bs4, python 패키지 활용 | Content-based filtering <br> Cosine-Similarity | Flask <br> python 패키지 활용 | Bootstrap theme |
## Dataset
    - Naver : 745개 웹툰 
        - 연재중 (전체)
        - 완결 (전체)
    - Daum : 741개 웹툰 
        - 연재중 (성인 웹툰 일부 제외)
        - 완결 (성인웹툰 일부 제외)
  
## Modeling
  - 사용자로부터 최근에 본 웹툰명을 Input으로 받는다.
  - 해당 웹툰 정보를 바탕으로 Content-based filterning

## More Detail
