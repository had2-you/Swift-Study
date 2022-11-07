

## Part 1. 함수
: 명령어의 묶음에 이름을 붙인 것  
왜 함수라고 부르는가? 언제든지 다시(반복해서) 실행할 수 있기 때문

__1) input이 있는 경우__
```swift
    func saySomething(name: String) {
        print("Hello \(name)")
    }
  
  // 함수 실행문
  saySomething(name: "Haeju")
```
<br>  

__2) output이 있는 경우__
```swift
    func sayHello() -> String {
        return "Hellow"
    }
    
    sayHello()
```
<br>

__3) input & output이 있을 경우__
```swift
    func sumNumber(num1: Int, num2: Int) -> Int {
        let sum = num1 + num2
        return sum
    }
    
    sumNumber(num1: 5, num2: 10)         // 15 출력
```
<br>

__4) return이 있는 함수 vs 없는 함수(void)__
```
- return이 있는 함수
return 다음의 표현식을 평가 후 그 결과를 리턴하고(함수를 중지) 함수를 벗어남

- return이 없는 함수
함수의 실행을 중지하고 함수를 벗어남
```
<br>

__5) Parameter & Argument__
```
Parameter : 함수 정의시, 함수 정의에 입력되는 값으로 내부에서 사용되는 변수(
            함수의 정의에 입력값으로 사용되는 변수(상수)
            값을 받아온 Parameter는 let으로 선언되었기 때문에 변경이 불가능하다.
            (치환 후 사용 가능 ex. a가 파라미터일 때, b = a + 1)            
            
Argumetn  : 함수 호출시, 함수가 필요한 파라미터의 타입과 일치하며 외부에서 사용하는 실제 값
            호출에 사용되는 실제값
            사용할 때의 이점 ➡️ Argument를 통해 더 명확하게 무엇을 요구하는지 알려줄 수 있음
```
```swift
    func printName(first name: String) {
        print("My name is \(name)")
    }
    
    printName(frist: "Haeju")
    
// 여기서 first = Argument, name = Parameter
```
- 와일드카드 패턴
```swift
    func addPrintFunc(_ firstNum: Int, _ secondNum: Int) {
        print(firstNum + secondNum)
    }
    
    addPrintFunc(4, 5)      // 9 출력
    
// Argument는 생략, Parameter는 firstNum/secondNum 이다.
```
- 가변 파라미터
```swift
    func numAvg(_ numbers: Double...) -> Double {
        let sum = 0.0
        
        for n in numbers {
            sum += n
        }
        
        return total / (Double)(numbers.count)      // count는 갯수를 나타냄
    
    numAvg(5, 6, 7, 8, 9)

// Parameter는 Double형으로 정해지지 않은, 여러 개의 값을 가질 수 있는 가변 파라미터라고 한다. (...)으로 
// Argument는 한 개의 파라미터를 통해 2개 이상을 전달할 수 있으며 배열의 형태로 전달된다.
```


---

## Part 2. 옵셔널

__1) 비교 연산자__

---

## Part 3. 컬렉션

__1) if문__  

---

## Part 4. 열거형

---
