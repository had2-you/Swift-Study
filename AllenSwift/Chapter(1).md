# Chapter 1. Part 1-6


## Part 1. 변수와 상수

- __변수(var)__
~~~
    var a = 4           // print(a) = 4
    var b = 6           // print(b) = 6
    a = 3               // print(a) = 3
~~~

즉, 변수는 안의 값이 바뀔 수 있는 것
<span style="color:red"> 글씨색 변경 </span>


- __상수(let)__
~~~
    let a = 3
    let b = 5 
    a = b               // 오류 발생
~~~
즉, 상수는 안의 값이 변할 수 없는 것



- __데이터타입__
~~~
    var a: Int = 4
    a = 3.14            // 오류 발생
~~~

데이터 타입은 선언할 때 주었던 형태와 맞는 값을 변수로 사용할 수 있다.



- __Character와 String의 차이__
~~~
    let Str: String = ""
    let Cha: Character = " "
~~~    
String은 빈 문자열을 저장할 수 있다.
Charater는 빈 문자열을 저장할 수 없음(공백은 가능)



- __타입추론__

Option + 변수며 클릭시 어떤 타입인지 추론할 수 있음

- __타입형변환__
### Stirng to Int 

    let str: String = "123"
    let num = Int(str)


### String to etc

    let str: String = "123.4"
    let num1 = Double(str)          // 결과 : 123.4
    let num2 = Int(str)             // int형이 아니기 때문에 nil 반환
    
    let Int: number = 1
    let num3 = Double(number)       // 결과 : 1.0


### 스위프트는 다른 타입끼리 계산할 수 없다. 

    let num1: int =  5
    let num2: double = 3.14
    let result = num1 + num2        // 에러발생


### Type Alias
기존에 선언되어 있거나 내가 만든 타입 등에 새로운 별칭을 붙여서 가독성을 높이는 데에 사용

#### TypeAlias Name = String

---
## Part 2. 기본 연산자
## Part 3. 조건문

## Part 4. 튜플

---
## Part 5. 삼항 연산자
## Part 6. 반복문


