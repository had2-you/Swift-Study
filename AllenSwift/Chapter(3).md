


## 클래스와 구조체

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
<img width="656" alt="image" src="https://user-images.githubusercontent.com/72385538/208585383-c0aa9498-4ea1-4771-bd86-d3d2ecdb6cf8.png">

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
<br>


__5) 속성 옵셔널__
```swift
    class Dog {
        var name: String?       // 옵셔널 선언시 nil 출력
        var weight: Int
        
        init(weight: Int) {     
            self.weight = weight
            //self.name = name
            //옵셔널 때문에 초기화를 하지 않아도 됨
        }
        
        func sit() {
            print("\(self.name)이 앉아있습니다.")
        }
        
        func layDown() {
            print("\(self.name)이 앉아있습니다.")
        }
    }
    
    var Bori = Dog(weight: 10) //name은 nil출력, name은 초기값을 설정하지 하든 안 하든 무관
    //if let bounding 등으로 옵셔널 벗기고 사용 
```
```
💡 옵셔널 타입을 가진 변수의 경우는 반드시 초기화 값이 있을 필요는 없음 ➡️ nil로 초기화 되기 때문에
```

- 식별 연산자
```
🔎 두 개의 차모가 갗은 인스턴스를 가리키고 있는지를 비교하는 방법
﹒ ===
﹒ !==
```



## 클래스와 구조체의 속성

__1) 저장 속성(Stored Properties)__
```
🔎 값이 저장되는 일바적인 속성(변수)
﹒let 또는 var로 선언 가능 단, let으로 선언 시 값을 바꿀 수 없음
﹒저장 속성은 각 속성 자체가 고유의 메모리 공간을 가짐
﹒초기화 이전에 값을 가지고 있거나, 생성자 메서드를 통해 값을 반드시 초기화 해야함
```
<br>

__2) 지연 저장 속성(Lazy Stored Properties)__
```
지연(Lazy)의 의미?
"해당 저장속성"의 초기화를 지연시키는 것
메모리에 공간과 값을 갖는 것이 아니라
⭐️해당 속성(변수)에 접근하는 순간에 해당 저장 속성만 개별적으로 초기화 됨⭐️

따라서 lazy var로만 선언이 가능하다. lazy let은 불가능
```

```swift
    sturct Bird {
        var name: String
        lazy var weight: Double = 0.2
        
        init(name: String) {
            self.name = name
        }
        
        func fly() {
            print("날아갑니다.")
        }
    }
    
    var aBird1 = Bird1(name: "새")
    aBird1.weight       // 해당 변수에 접근하는 이 시점에 초기화 됨(메모리 공간 생기고 숫자 저장)
```

```
﹒생성자에서 초기화를 시키지 않기 때문에 ⭐️선언시점에 기본값을 저장⭐️ 해야한다.
﹒값을 넣거나 표현식(함수 실행문)을 넣을 수 있다.
﹒함수호출 코드, 계산코드, 클로저 코드 등 모두 가능(저장하려는 속성과 리턴형만 일치하면 됨)
﹒지연 저장 속성으로 선넌된 해당
```

