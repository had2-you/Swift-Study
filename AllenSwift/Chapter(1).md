
## Part 1. 변수와 상수

__1) 변수(var)__
```swift
    var a = 4           // print(a) = 4
    var b = 6           // print(b) = 6
    a = 3               // print(a) = 3
```
즉, 변수는 안의 값이 바뀔 수 있는 것

<br><br>
__2) 상수(let)__
```swift
    let a = 3
    let b = 5 
    a = b               // 오류 발생
```
즉, 상수는 안의 값이 변할 수 없는 것

<br><br>
__3) 데이터타입__
```swift
    var a: Int = 4
    a = 3.14            // 오류 발생
```
데이터 타입은 선언할 때 주었던 형태와 맞는 값을 변수로 사용할 수 있다.

<br><br>
__4) Character와 String의 차이__
```swift
    let Str: String = ""
    let Cha: Character = " "
```
String은 빈 문자열을 저장할 수 있다.
Charater는 빈 문자열을 저장할 수 없음(공백은 가능)

<br><br>
__5) 타입형변환__
#### Stirng to Int 
```swift
    let str: String = "123"
    let num = Int(str)
```

#### String to etc
```swift
    let str: String = "123.4"
    let num1 = Double(str)          // 결과 : 123.4
    let num2 = Int(str)             // int형이 아니기 때문에 nil 반환
    
    let Int: number = 1
    let num3 = Double(number)       // 결과 : 1.0
```

<br><br>
__6) 스위프트는 다른 타입끼리 계산할 수 없다.__
```swift
    let num1: int =  5
    let num2: double = 3.14
    let result = num1 + num2        // 에러발생
```

<br><br>
__7) 타입추론__  
```
Option + 변수명 클릭시 어떤 타입인지 추론할 수 있음
```
<br><br>
__8) Type Alias__
```
기존에 선언되어 있거나 내가 만든 타입 등에 새로운 별칭을 붙여서 가독성을 높이는 데에 사용  
TypeAlias Name = String
```
---

## Part 2. 기본 연산자

__1) 비교 연산자__
```
== : Euqal to operator  
!= : Not equal to operator  
>  : Grater than operator  
>= : Grater than or equal to operator  
<  : Less than operator  
<= : Less than or equal to operator   
```
<br>

__2) 논리 연산자__  
```
! : Not operator
&& : AND operator
|| : OR operator
```
<br>

__3) 연산 우선순위__  
```
곱셈/나눗셈 > 덧셈/뺄셈 > 비교연산자 > 논리연산자 > 할당/복합할당 연산자  
```

---

## Part 3. 조건문

__1) if문__  
조건은 항상 참/거짓  

- if
```swift
    num = 10
    if num >= 10 {
        print("10이상 입니다.")
    }
```
- if-else
```swift
    num = 10
    if num >= 10 {
        print("10이상 입니다.")
    }
    else {
        print("10이하 입니다.")
    }
```
- if-else if-else
```swift
    num = 15
    if num <= 10 {
        print("10이하 입니다.")
    }
    else if num >= 20 {
        print("20이상 입니다.")
    }
    else {
        print("10보다 크고 20보다 작습니다.")
    }
```  
- 조건문의 특징  

```
    1) 논리적인 구조 및 조건의 순서가 중요하다.
       범위가 작은 조건이 먼저 와야한다.
    2) 조건은 &&와 ||로 연결이 가능하다.
    3) 중첩 if문이 가능하다.
```

__2) Switch 문 : if문 보다 한정적인 상황에서 사용(분기처리할 때)__


---

## Part 4. 튜플

---

## Part 5. 삼항 연산자

---

## Part 6. 반복문




