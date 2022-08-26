# 부동산 데이터 분석 프로젝트
## 프로젝트 소개 
최근 ‘벼락 부자’, ‘벼락 거지’ 라는 신조어가 생길 정도로 지난 몇년간 유래없는 부동산 가격 폭등이 있었습니다.   
앞으로 부동산 시장의 거품이 꺼지고 구매 시점이 온다면, 지역 또는 아파트 선택에 도움이 될 수 있는 인사이트를 찾기 위해 이 프로젝트를 진행하였습니다.

## 사용 라이브러리
Pandas, numpy, plotly, matplotlib

## 사용 데이터
아파트 실거래가 데이터 (매매, 서울특별시, 2006-2021년) - 국토교통부   
네이버 Geocoding 데이터 (도로명주소 -> 위도,경도 변환) - 네이버   
서울시 전입지 이동사유별 인구이동 통계 (2017-2021년) - 서울 열린데이터 광장   
공급물량 데이터 (1986-2026년) - 아파트 실거래가(아실)   

## 결과
### 계약날짜
● 거래량과 아파트 가격 두가지로만 가격 형성이 이루어지지 않음   
● 3월과 9월이 거래량↑ 가격↓   
● 시간이 지날수록, 분포↑ 밀도↓ : 아파트 간의 평당 금액 차이가 크다   
### 평형대
● 대부분의 구에서 많이 거래되는 평형대는 18평 이하와 25평-30평   
● 18평 이하와 25-30평의 거래비율이 전체 평형 거래의 약 60-70%를 차지   
● 18평 이하 아파트의 수요가 증가되고 있음   
### 부동산 시장 변동
● 2006-2021년에 평균 223%가량 상승하였다   
● 평당 가격 상승이 높은 지역은 서울의 서쪽과 북쪽인 서대문구, 강서구, 노원구 등이다   
● 세대수가 클수록, 가격 상승에 유리   
● 평형대가 작은 순으로 상승폭도 크다   
강세기   
● 2017-2021년에 평균 97%가량 상승   
● 세대수가 작을수록 상대적으로 상승폭이 작다   
● 작은 평형대로 갈수록 상승폭이 커짐   
약세기   
● 모든 구의 최대 하락폭 평균은 약 -7%   
● 대단지일수록 가격 방어가 좋다   
● 평형대가 커질수록 하락도 커지는 모습   
### 인구이동
● 서울 전입 수는 시도내 이동이 65-70%를 차지   
● 송파/강남/관악/강서구는 타 구에 비해 높은 부동산 거래와 인구 밀집   
● 금천/용산/종로/중구는 타 구에 비해 거주 관심도가 떨어지는 구   
● 노원구, 성동구, 구로구, 도봉구 -> 아파트 수요가 많다   
● 광진구, 은평구, 관악구, 강북구 -> 빌라/오피스텔/원룸 등의 수요가 많다   
### 브랜드
● 최상위브랜드와 상위브랜드는 10% 거래비율   
● 약 91% 거래가 이외브랜드   
● 래미안과 푸르지오가 약 53%로 브랜드 거래 비중의 절반 이상   
● 래미안은 상대적 평당 가격 ↓ 거래량↑으로 점유율 확보   
● 상위브랜드 대비 이외브랜드의 아파트 가격 비율이 떨어지고 있음   
● 이외브랜드는 거래량이 방어X, 하락폭이 크다   
● 상위브랜드는 이외브랜드보다 거래량이 유지   
● 상위브랜드는 거래량은 적지만 해당 브랜드로의 꾸준한 수요 존재   
### 부동산 정책
● 큰 대책인 총 6개만 추려서 분석을 진행   
● 정책 발표 3개월 전후 비교를 통해 각 구의 가격과 거래량 확인   
● 가격의 경우 6개의 정책 이후 상승이 우세한 경우가 6번   
● 거래량의 경우 6개의 정책 이후 상승이 2번, 하락이 4번   

### 앞으로 추가적으로 보완/진행할 사항
1. 부동산 강세기/약세기 데이터    
- 이 경우는 2009년에서 2013년(약세기), 2017년에서 2021년(강세기)로 총 한 번씩의 해당 데이터만 가지고 진행할 수밖에 없었다.    
따라서 앞으로 지속적으로 데이터를 추가한다면 두 번 이상의 강세기/약세기 데이터를 통해 비교를 진행할 수 있을 것이다.
2. 인구이동 데이터    
- 이 경우 아파트 전입신고 건수뿐만 아니라 해당 지역의 빌라, 오피스텔, 원룸 등의 모든 전입신고 건수가 포함이 되어있어 아파트만의 전입신고 건수는 확인할 수 없었다.    
데이터를 추출해 온 '서울 열린데이터 광장'을 지속적으로 확인을 통해 아파트만의 전입신고와 관련된 데이터가 올라오게 되면 이를 심층적으로 분석이 가능할 것이다.
3. 지하철역 데이터    
- 지하철역 데이터를 추출하여 해당 역이 완공된 시기와 위도/경도 데이터를 추가한다면 주변의 아파트가 해당 역의 완공과 함께 어떠한 변화를 보였는지 확인이 가능할 것으로 보인다.   
5. 현 프로젝트는 Colab 환경에서 진행되었고 차트로 시각화의 경우 대부분 Plolty 라이브러리를 사용하여 interactive 가능하게 만들었으나 현 Github의 경우 Plotly 차트 결과가 표시되지 않는 것을 확인    
- 앞으로의 차트 시각화 자료들은 Matplotlib 라이브러리를 사용

## 라이센스   
MIT @ PremiumCJ
