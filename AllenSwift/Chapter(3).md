


## Part 1. 클래스와 구조체

<details>
<summary> </summary>
	
__1) 클래스__
```
🔎 변수와 함수를 어떤 묶음으로 다룰 수 있는 것
```

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
    
- 구조체 객체 생성
```swift
    var aBird = Bird()
    //초기값 name = 새 / weight = 0.0
    
    aBird.name = "참새"
    aBird.weight = 0.3
    //설정 후 name = 참새 / weight = 0.3
    
    aBird.fly()     // 날아갑니다.
```
</details>



__3) 클래스와 구조체의 차이__
```
💡 가장 큰 차이는 메모리 저장 방식 차이

- 구조체
값형식(
```

## Part 2. 

<details>
<summary> </summary>


</details>




