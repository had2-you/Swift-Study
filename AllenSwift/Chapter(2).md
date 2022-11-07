

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
    
    sumNumber(num1: 5, num2: 10)         // 15출력
```
<br>

__4) return이 있는 함수 vs 없는 함수(void)__
```
- 
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
