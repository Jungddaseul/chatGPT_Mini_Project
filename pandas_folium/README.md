### 📍 데이터셋 링크 : https://data.seoul.go.kr/dataList/OA-15272/F/1/datasetView.do
- 데이터셋 다운 ➖ [다운로드](https://github.com/Jungddaseul/chatGPT_Mini_Project/blob/main/pandas_folium/%EC%84%9C%EC%9A%B8%ED%8A%B9%EB%B3%84%EC%8B%9C_%EB%B0%95%EB%AC%BC%EA%B4%80%EB%AF%B8%EC%88%A0%EA%B4%80%EC%A0%95%EB%B3%B4_20230323.csv)
- 설명 : 서울특별시에 소재하는 박물관, 미술관 정보
- 시설명, 구분(공립, 사립), 도로명주소, 위도, 경도, 전화번호, 운영기관명, 홈페이지 주소, 관람료, 운영시간 정보 등을 제공

### 📍 데이터 전처리
> ####  1. 위치 시각화에 불필요한 데이터 삭제
- '박물관미술관구분', '소재지지번주소', '운영기관명', '편의시설정보', '교통안내정보',
- '관람료기타정보', '박물관미술관소개', '교통안내정보', '관리기관전화번호', '관리기관명',
- '교통안내정보', '데이터기준일자', '평일관람시작시각', '평일관람종료시각', '공휴일관람시작시각', '공휴일관람종료시각'

> #### 2. null 값 삭제
> #### 3. 관람료에 있는 0 데이터 행을 삭제

### 📍 데이터 위치 시각화
- folium을 활용한 위치 시각화
- 서울 시청을 중심으로 하는 지도 생성(chatGPT를 통해 서울시청 중심으로하는 위도, 경도 데이터 확인)
> <img width="1000" alt="image01" src="https://user-images.githubusercontent.com/114555218/237041804-3fec8d14-3f68-4db8-9056-b91411883da4.png">
- Marker()를 이용하여 위도, 경도에 따른 마커 및 해당정보 팝업 생성

 **1. 시설명만 표시**
> <img width="1000" alt="image02" src="https://user-images.githubusercontent.com/114555218/237042105-aabe3c6e-5e85-41e1-9b7b-b547e58daed8.png">

 **2. 시설명, 요금 표시**
> <img width="1000" alt="image03" src="https://user-images.githubusercontent.com/114555218/237042121-1f44aed7-4a09-41b5-b2a1-a0cba9b49f89.png">
