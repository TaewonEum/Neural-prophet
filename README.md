# Neural-prophet 단변량 시계열 분석

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

![image](https://user-images.githubusercontent.com/104436260/192939281-df84b4e9-2e73-4fde-9829-f31b114ae799.png)

24시에 해당하는 행 모두 삭제

날짜/시간 분리 하여 컬럼 생성->해당 분석은 시간대별로 발전량을 예측하는 Pilot분석임.
====
![image](https://user-images.githubusercontent.com/104436260/192940233-8ca8feec-3581-4c08-ab93-877d70b0b4f9.png)

![image](https://user-images.githubusercontent.com/104436260/192940532-d535b434-c49b-4ca9-a151-a50cfcfdd4a7.png)

7일치 샘플 발전량 데이터 시각화
====
![image](https://user-images.githubusercontent.com/104436260/192941602-ed830655-1364-4cfa-bcce-49b83934a330.png)

Train&Test Split
====
![image](https://user-images.githubusercontent.com/104436260/192942522-0d273244-ed97-4ac0-96af-877e3f446724.png)

약 9:1비율로 Train Test Split

![image](https://user-images.githubusercontent.com/104436260/192943274-57b4efa5-5ade-4f48-b634-90ce13ad8b0d.png)

Model Training
=====
![image](https://user-images.githubusercontent.com/104436260/192943962-89eeb870-f550-4cb4-82a1-363409b15bc5.png)

![image](https://user-images.githubusercontent.com/104436260/192944173-261bdacf-6b15-4b38-a2f6-8bf41c7ad06e.png)


Train Data 예측값
====
![image](https://user-images.githubusercontent.com/104436260/192963615-a572c8ad-3a3f-4594-b49c-cd5fc7774bbc.png)


![image](https://user-images.githubusercontent.com/104436260/192963872-4268df91-19e5-478c-b790-ee8c3e187c1e.png)

발전량만 사용하여 시계열 분석을 진행하였기 때문에 어느정도 발전량의 추세를 따라가는 것 처럼 보이지만

정확도가 많이 떨어짐 추후 일사량, 전운량등의 기상데이터를 결합시켜 다변량 예측 모델로 진행 예정

MAP, RSME 시각화
====
![image](https://user-images.githubusercontent.com/104436260/192966557-7c7f327c-24aa-4ba6-86f0-b6a784c19876.png)
![image](https://user-images.githubusercontent.com/104436260/192967147-bc1d8ea6-e97e-420d-8b77-f3e5d22e46d9.png)
![image](https://user-images.githubusercontent.com/104436260/192966937-bd2ecf42-2716-4dd0-a5a3-4ee0ee1fbd49.png)

test data와 예측값 비교
====
![image](https://user-images.githubusercontent.com/104436260/192973680-2a92aa2c-78e8-4f9e-a25e-e3cd223b67c1.png)
