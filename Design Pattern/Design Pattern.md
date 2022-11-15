### Design pattern stduy w. Group 5
#### 2022. 11. 11. Fri. 1:00 p.m
<br>  

```
🔸 디자인 패턴? 소프트웨어 공학의 소프트웨어 설계에서 공통으로 발생하는 문제에 대해 자주 쓰이는 설계방법을 정리한 패턴

🔸 디자인 패턴의 사용 이유? 디자인 패턴을 참고하여 개발할 경우 개발의 효율성과 유지보수성,
   운용성이 높아지며 프로그램의 최적화에 도움이 된다.
```
<br>  

## MVC  
![image](https://user-images.githubusercontent.com/72385538/201844871-02adb5b3-d3eb-4fdd-9aaf-bf6bf0a18b23.png)
<br>  

- MVC의 구성
```
🔸  Model : 핵심 기능과 데이터를 보관
🔸  View : 사용자가 보는 곳(UI)
🔸  Controller : 뷰에서 일어나는 입력(Action)을 받는 곳, 모델과 뷰 사이에 존재
```
```
🔸 Model - View - Controller는 별도의 컴포넌트로 분리되어 있고 서로 영향을 받지 않고 개발 가능
🔸 여러 개의 뷰를 만들 수 있기 때문에 한 개의 모델에 대한 여러 개의 뷰를 필요로 하는 대화형 애플리케이션에 적합 

💡 대화형 애플리케이션? 온라인 쇼핑몰 사이트나 스마트폰 앱과 같이 사용자의 요구가 발생하면 시스템이 처리하고 반응하는 SW
```
<br>  

- 동작 과정
```
1. 사용자의 액션은 Controller로 부터 받음
2. Controller는 사용자의 액션을 확인하고 모델은 업데이트
3. Controller는 모델을 나타내줄 View를 선택
4. View는 Model을 이용하여 화면을 나타냄

💡 MVC에서 View가 업데이트 되는 방법
   - View가 Model을 이용하여 직접
   - Model에서 View에게 Notify
   - View가 Polling으로 주기적으로 Model의 변경을 감지
```
<br>  

```
🔸 특징
  - 가장 단순한 패턴
  - Controller는 여러 개의 View를 선택할 수 있는 1:n 구조
  - Controller는 View를 ⭐️선택⭐️만, 업데이터는 하지 않음 ➡️ View는 Controller를 모름

🔸 장점
  - 단순하기 때문에 보편적으로 많이 사용
  
🔸 단점
  - View와 Model사이의 의존성이 높다는 문제가 발생
    왜? 하나의 Controller가 다수의 View를 관리하고 있기 때문
  
  - 어플리케이션이 커질수록 복잡해지고 유지보수가 어렵다.
  - 의존성 문제에 의해 다른 패턴을 파생시킴(해당 문제를 해결하기 위해 MVVM이 파생)
```
<br>  

## MVP 
![image](https://user-images.githubusercontent.com/72385538/201844787-034860f3-7c90-45e2-9a17-382100a001d1.png)
<br>  

- MVP 구성
```
    - Presenter
    - View
    - Model
```
<br>  

- 동작 과정


<br>  

```
🔸 특징
  모델과 뷰의 의존성이 없다는 장점
  
🔸 장점
  
  
🔸 단점
  

```
<br>  

## MVVM 

![image](https://user-images.githubusercontent.com/72385538/201844632-7f29b046-8ebd-4b56-ba64-e02a48dead7b.png)
<br>  

- MVVM의 구성
```
 Model
 View
 View Model
 ```
 <br>  
 
- 동작 과정
```
Command 패턴 : 사용자가
```
<br>  

```
🔸 특징


🔸 장점


🔸 단점 


커맨드 패턴과 데이터바인딩 패턴을 이용해 의존성을 없앰
뷰와 모델 사이에 의존성이 없음
각 독립적이기 때문에 모듈화하여 개발 가능
뷰모델 
```




