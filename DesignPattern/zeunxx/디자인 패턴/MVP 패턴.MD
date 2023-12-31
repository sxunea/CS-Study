# MVP 패턴 Model-View-Presenter Pattern

## MVP 패턴이란?

MVC 패턴으로부터 파생되었으며 MVC에서 C에 해당하는 컨트롤러가 프레젠터(Presenter)로 교체된 패턴

![image](https://github.com/zeunxx/Inflearn-Spring-RoadMap/assets/81572478/030b01d1-6ee1-4173-9afd-78a984696ec2)

뷰와 프레젠터는 일대일 관계이므로 MVC 패턴보다 더 강한 결합을 지닌 디자인 패턴

### Presenter
View에서 요청한 정보로 Model을 가공해 View에 전달해준다.

- View 에서 발생하는 이벤트를 처리합니다.
- View 를 직접적으로 제어하거나 업데이트하며 UI 단의 로직 처리를 담당합니다.


#### 💡 단점
View 와 Presenter 가 1 대 1 관계로 매칭됨에 따라, View 쪽의 의존성이 증가한다. 
따라서 View 쪽 중심적으로 설계되므로, 다양한 View 에 대한 Presenter 기능의 재사용이 힘들어진다.