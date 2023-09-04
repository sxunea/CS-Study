# MVVM 패턴 Model-View-ViewModel 패턴

## MVVM 패턴이란?

MVC에서 C에 해당하는 컨트롤러가 뷰모델(ViewModel)로 교체된 패턴

![image](https://github.com/zeunxx/Inflearn-Spring-RoadMap/assets/81572478/72412115-62d3-40b0-b1f0-389cd1525044)

뷰모델은 뷰를 더 추상화한 계층이며, MVVM 패턴은 MVC 패턴과는 다르게 커맨드와 데이터 바인딩을 가지는 것이 특징이다.


> 데이터 바인딩
> 두 개의 데이터 소스(또는 동일한 데이터에 대한 두 개의 개별 표현)를 함께 연결하고 동기화 상태를 유지하는 일반적인 기술


## View Model

뷰와 뷰모델 사이의 양방향 데이터 바인딩을 지원하며 UI를 별도의 코드 수정없이 재사용할 수 있고, 단위 테스팅하기 쉽다.

데이터 바인딩 구조를 토애 사용자와의 상호작용으로 View의 내용이 바뀌면 바인딩된 데이터 소스인 View Model의 데이터가 자동으로 변경되고, View Model 데이터 소스가 변경되면 자동으로 바인딩된 View의 값이 변경된다.


1. View에 입력이 들어오면 ViewModel에게 명령을 한다.

2. ViewModel은 필요한 데이터를 Model에게 요청한다.

3. Model은 ViewModel에게 요청된 데이터를 응답한다.

4. ViewModel은 응답 받은 데이터를 가공해서 저장한다.

5. View는 ViewModel과의 Data Binding으로 인해 자동으로 갱신된다.


➡️ View와 Model이 서로 전혀 알지 못하기에 독립성을 유지할 수 있다.