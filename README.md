# os2019

부동산 시세 알림 챗봇

서울시열린데이터광장에서 제공하는 서울특별시 전월세가 정보(http://data.seoul.go.kr/dataList/datasetView.do?infId=OA-15549&srvType=S&serviceKind=1&currentPageNo=1)를 이용해 시세를 예측한다.

geopandas를 사용해 구 이름과 좌표 등이 입력되어 있는 서울시 행정구역 데이터 seoul_municipalities_geo.json을 읽어와 사용자가 입력한 평수와 건물 유형에 해당하는 서울시 전/월세 지도 이미지를 생성한다.

Exobrain Api를 사용해 빠르고 정확한 챗봇 서비스를 제공한다.

①	사용자가 프로그램을 실행해 질문을 입력한다. 질문 양식은 제한이 없으나 분석에 필요한 ‘자치구 명’, ’법정동 명’, ’전월세’, ‘거주 형태’를 입력해야 한다.
정확한 주소를 몰라 구 정보를 입력하지 않아도 시스템이 찾아 입력하지만 그 외 정보는 미 입력 시 추가 입력을 요청한다. 

②	챗봇은 사용자 질문을 서버로 전송한다. 서버가 질문을 분석해 형태소, 단어 별 태그로 라벨링한 결과를 다시 챗봇으로 전송한다. 챗봇은 이 결과를 분석 모델이 사용할 수 있는 딕셔너리 형태로 가공한다.

③	분석 모델은 챗봇이 입력한 정보를 바탕으로 예측한 답변과 그래프를 인터페이스로 전달한다. 

④	사용자는 답변과 그래프를 확인한다.



