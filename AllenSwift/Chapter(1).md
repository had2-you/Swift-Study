
## Part 1. 변수와 상수
<details>
<summary> </summary>

__1) 변수(var)__
```swift
    var a = 4           // print(a) = 4
    var b = 6           // print(b) = 6
    a = 3               // print(a) = 3
```
💡 즉, 변수는 안의 값이 바뀔 수 있는 것

<br>  

__2) 상수(let)__
```swift
    let a = 3
    let b = 5 
    a = b               // 오류 발생
```
💡 즉, 상수는 안의 값이 변할 수 없는 것

<br>  

__3) 데이터타입__
```swift
    var a: Int = 4
    a = 3.14            // 오류 발생
```
💡 데이터 타입은 선언할 때 주었던 형태와 맞는 값을 변수로 사용할 수 있다.

<br>  

__4) Character와 String의 차이__
```swift
    let Str: String = ""
    let Cha: Character = " "
```
💡String은 빈 문자열을 저장할 수 있다. Charater는 빈 문자열을 저장할 수 없음(공백은 가능)

<br>  

__5) 타입형변환__
- Stirng to Int 
```swift
    let str: String = "123"
    let num = Int(str)
```

- String to etc
```swift
    let str: String = "123.4"
    let num1 = Double(str)          // 결과 : 123.4
    let num2 = Int(str)             // int형이 아니기 때문에 nil 반환
    
    let number: Int= 1
    let num3 = Double(number)       // 결과 : 1.0
```

<br>  

__6) 스위프트는 다른 타입끼리 계산할 수 없다.__
```swift
    let num1: Int =  5
    let num2: double = 3.14
    let result = num1 + num2        // 에러발생
```

<br>  

__7) 타입추론__  
```
Option + 변수명 클릭시 어떤 타입인지 추론할 수 있음
```
<br>

__8) Type Alias__
```
기존에 선언되어 있거나 내가 만든 타입 등에 새로운 별칭을 붙여서 가독성을 높이는 데에 사용  
TypeAlias Name = String
```
</details>




## Part 2. 기본 연산자
<details>
<summary>  </summary>
    
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
</details>





## Part 3. 조건문
<details>
<summary> </summary>

__1) if문__  
조건은 항상 참/거짓  

- 조건문의 특징  

```
1) 논리적인 구조 및 조건의 순서가 중요하다.
   범위가 작은 조건이 먼저 와야한다.
2) 조건은 &&와 ||로 연결이 가능하다.
3) 중첩 if문이 가능하다.
```

<br>  

- if
```swift
    var num: Int = 10
    if num >= 10 {
        print("10이상 입니다.")
    }
```
- if-else
```swift
    var num: Int = 10
    if num >= 10 {
        print("10이상 입니다.")
    }
    else {
        print("10이하 입니다.")
    }
```
- if-else if-else
```swift
    var num: Int = 15
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

__2) Switch__
표현식/변수를 분기처리할 때 사용하는 조건문

- 스위치문의 특징
```
1) 스위치문에서 ,(콤마)는 또는의 의미로 여러 매칭 값을 넣을 수 있다.
2) 스위치문은 모든 경우의 수를 다루어야 하며 모든 사례를 다루지 않았을 경우 default 케이스가 반드시 필요하다.
3) 각 케이스에는 문장이 최소 하나 이상 있어야 하며 없다면 컴파일 에러 발생
   실행하지 않으려면 break문을 사용
4) 부등식을 사용할 수 없으므로 범위 매칭을 사용
   ex) case < 0 ➡️ case ..<0 // ..은 정수(음수까지 포함)의 범위를 의미
       case >= 10 && case <= 20 ➡️ case 10...20
```

- break
```swift
    var num: Int = 10
    
    switch num {
    case ..<10 :
        print("1")      //print nothing
        break
    case 10 :
        print("2")      // print 2
        break
    default :
        print("3")      // print nothing
    }
```
<br>  

- fallthrough
```swift
    var num: Int = 10
    
    switch num {
    case ..<10 :
        print("1")
        fallthrough     //print nothing
    case 10 :
        print("2")
        fallthrough     // print 2
    default :
        print("3")      // print 3
    }
```

<br>  

- binding
```swift
    var num: Int = 7
    
    switch num {
    case let x where x % 2 == 0:       // let x = num
        print("짝수입니다.")
    case let x where % 2 != 0: 
        print("홀수입니다.")
    default:
        break
    }
```
💡 상수(변수도 가능) 바인딩은 주로 where와 함께 사용 
</details>


## Part 4. 튜플
<details>
<summary>  </summary>

```
🔎 2개 이상의 연관된 데이터를 저장하는 혼복합 타입
```
<br>
    
- 튜플의 특징
```
1) 타입이 특별하게 정해져 있지 않다.
2) 포함될 데이터의 개수는 마음대로 정할 수 있다.
3) 데이터의 종류 및 갯수는 튜플을 만들 때 결정되므로 추가/삭제는 불가능하다.
```

- 튜플의 접근
```swift
    let threeValues = (name : "홍길동", age : 20, live : "서울")
    threeValues.0       // 홍길동
    threeValues.1       // 20
    threeValues.2       // 서울
    
    threeValues.name
    threeValues.age
    threeValues.live
```

- 튜플의 바인딩

</details>

    
    
    
    
    
## Part 5. 삼항 연산자
<details>
<summary>  </summary>
</details>

    
    
    
    
    

## Part 6. 반복문
<details>
<summary>  </summary>
</details>




