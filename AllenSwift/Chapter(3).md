


## Part 1. 클래스와 구조체

<details>
<summary> 클래스와 구조체 기본 구조 </summary>
	
__1) 클래스__
```
🔎 변수와 함수를 어떤 묶음으로 다룰 수 있는 것
   클래스 내부에는 직접 메서드(함수) 실행문이 올 수 없다.
```
<br>
    
    
- 클래스 생성
```swift
    calss Dog {
        var name = "강아지"
        var weight = 0
	
        func sit() {
            print("앉았습니다.")
        }
	
        func layDown() {
            print("누웠습니다.")
        }
    }
```
<br>
    
    
- 클래스 객체 생성
```swift
    var bori = Dog()
    //초기값 name = 강아지 / weight = 0

    bori.name = "보리"
    bori.weight = 15
    //설정 후 name = 보리 / weight = 15
    
    bori.sit()      // 앉았습니다.
    bori.layDown()  // 누웠습니다.
```
<br>
    
    
__2) 구조체__
- 구조체 생성
```swift
    struct Bird {
        var name = "새"
        var weight = 0.0
    
        func fly() {
            print("날아갑니다.")
        }
    }
```
<br>
    
    
- 구조체 객체 생성
```swift
    var aBird = Bird()
    //초기값 name = 새 / weight = 0.0
    
    aBird.name = "참새"
    aBird.weight = 0.3
    //설정 후 name = 참새 / weight = 0.3
    
    aBird.fly()     // 날아갑니다.
```
<br>
    
    
</details>

__3) 클래스와 구조체의 차이__
<br>


<img width="656" alt="image" src="https://user-images.githubusercontent.com/72385538/208584800-8f272687-4f03-4795-b4ed-a708ee042982.png">


<br>


- 클래스와 구조체의 let과 var
```swift
    class PersonClass {
        var name = "사람"
        var age = 0
    }
    
    struct AnimalStruct {
        var name = "동물"
        var age = 0
    }
    
    let pclass = PersonClass()
    let astruct = AnimalStruct()
    
    pclass.name = "사람1"     // 사람1이 출력
    astruct.name = "동물1"    // let이기 때문에 변경 불가하다는 에러메세지 출력
```
<br>


__4) 클래스와 구조체 초기화(initializer)__
```
🔎 생성자(이니셜라이저)는 인스턴스를 만들 때 사용하는 특별한 메서드

init(파라미터)
모든 저장속성(변수)를 초기화 해야 한다(구조체, 클래스 동일)
생성자 실행 종료 시점에는 모든 속성의 초기값이 저장되어 있어야 함(초기화 미완료시 컴파일 에러)
생성자이 목적은 결국 "저장속성(변수) 초기화"
클래스, 구조체, (열거형)은 모두 설계도 일뿐, 실제 데이터(속성), 동작(메서드)를 사용하기 위해서는 ⭐️초기화 과정이 반드시 필요⭐️
```
<br>


```swift
    //클래스 생성
    
    class Dog {
        var name: String
        var weight: Int
        
        init(n: String, w: Int) {
            self.name = n
            self.weight = w
        }
        
        func sit() {
            print("\(self.name)가 앉아있습니다.")
        }
        
        func layDown() {
            print("\(self.name)가 누워있습니다.")
        }
    }
    
    //클래스 선언 및 초기화
    var choco = Dog(n: 초코, w: 6)
    var choco = Dog.init(n: 초코, w: 6) // 위와 같은 의미 init생략 가능
    
   choco.name
   choco.weight
   choco.sit()
   choco.layDown()
```
```
💡 self키워드는 클래스/구조체 내에서 해당 인스턴스(자기자신)을 가리킴
   인스턴스 내에서 동일한 변수/상수명을 사용할 때 가리키는 것을 명확하게 하기 위해 사용
```

## Part 2. 

<details>
<summary> </summary>


</details>




