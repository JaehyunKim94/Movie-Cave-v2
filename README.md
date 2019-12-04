# Project Movie Cave - version 2

## 1. At version 1

1. Seed data crowling
   1. `movie.naver.com` 의 평점순 영화랭킹(현재 상영영화 + 모든 영화)을 기준으로 7일 간격 50주간의 데이터(영화이름 & 영화코드)를 수집
   2. 수집된 데이터를 [NAVER 영화 검색 API](https://developers.naver.com/docs/search/movie/) 와 네이버 영화 상세보기 페이지의 크롤링을 통해 Seed data를 수집
   3. 수집된 데이터는 각각 `movies.json`, `directors.json`, `genre.json`, `actors.json` 파일로 저장됨
2. Django Rest Framework
3. Vue & Vuetify

