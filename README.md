# Neural-prophet

산자부 태양광 보급사업 예산사업 효율화 및 연계활용을 위한 Pilot분석 코드입니다.

데이터 출처: Dacon 동서발전 태양광 발전량 예측 AI 경진대회

데이터분석 환경: Jupyter lab

사용모델: Neural Prophet 시계열 모델

발전량 예측은 대표적인 시계열 분석에 해당하기 때문에 기존의 시계열 분석에서 Neural Network 알고리즘은 반영한 Neural Prophet 모델 사용

This is a Sample Neural Prophet Code(Univariate)
====
![image](https://user-images.githubusercontent.com/104436260/192928122-e0fe2865-cf13-4b6e-80c0-5861ebc1fe69.png)

Package Load & Sample data Load

1.데이터 소개
=====

발전소 용량 및 위치정보 데이터 셋
====
![image](https://user-images.githubusercontent.com/104436260/192928454-9818622b-553f-4fd6-8930-e41caf456406.png)

발전소 용량 시각화
====
![image](https://user-images.githubusercontent.com/104436260/192936348-53b8d1d2-1841-4ba1-9d2a-53ce57e5ed35.png)

발전소별 실제 발전량 데이터 셋
====
![image](https://user-images.githubusercontent.com/104436260/192936768-558eb9ed-db4a-42da-9136-2b8f8da79324.png)

발전소 데이터 셋 EDA
====
![image](https://user-images.githubusercontent.com/104436260/192937027-8b51e6e8-171e-44a0-a986-169cd73ad962.png)

결측값 처리
=====
![image](https://user-images.githubusercontent.com/104436260/192938116-ddbe745a-6ca3-437b-83d5-e0943e941bb1.png)

인근 발전소 발전량으로 결측값 대체

날짜 변수 전처리
====
![image](https://user-images.githubusercontent.com/104436260/192938459-6e23a0ff-65e9-4974-8326-868340f09837.png)

24시 정각의 값은 모두 정수로 표현되어 있음, 하지만 24시 정각에는 발전량이 거의 없으므로 해당 Pilot 분석에서 해당 행들은 삭제하고 진행
