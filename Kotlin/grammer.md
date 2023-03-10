# 코틀린 문법

### var, val
- var이 그냥 변수고
- **val**이 상수!

### ☆Nullable
- 선언: `:Type?` 을 붙여 선언하기
- 안전한 접근: `value?.member`로 `?`를 붙여 접근하기
  - 만약 `null`이라면 멤버를 호출하고 에러 터지는 대신에, `null`을 반환함.
- null이 아닐 때 코드 실행: `value?.let { ~ }`
  - 이는 if문을 사용하는 것과 같다.

+ `?`이 안 붙어있으면 당연히 `Non-nullable`이라 `null`이 될 수 없음.
+ `!!` 연산자: `Nullable` 타입을 `Non-nullable`으로 변환해줌.
  + ∴ `NPE`가 발생 가능!
  + risky 하므로 `null`이 아닌 것을 확신할 때만 사용할 것.

- `?` 키워드가 `선언` / `안전 접근` 두 가지로 쓰이기 때문에 잘 구분할 것!

### 삼항 연산자
- 코틀린에는 삼항 연산자가 없다.
- 삼항 연산자를 if-else 한줄구문으로 구현 가능.

### 엘비스 연산자
- `?:`
- ex) `b?.length ?: -1`
- 있으면 그대로 출력, 아니면 기본값 출력 (JS와 Lua의 `or` 처럼)


### 클래스

```java
class Person(var a: String, var b: String) {
  init {
    println("${a} ${b}")
  }
}
```
- class 선언 줄에 생성 변수를 지정할 수 있다.
  - ∴ 이렇게 선언하면 JAVA와 다르게 `this.x = x`를 할 필요없다.

### 다중 생성자 (오버로딩)

```java
class Person(var firstName: String, var lastName: String) {
    var age: Int? = null
    var eyeColor: String? = null
    
    // Secondary Constructor
    constructor(firstName: String, lastName: String, age: Int) : this(firstName, lastName)  {
        this.age = if(age > 0) age else throw IllegalArgumentException("Age must be greater than zero")
    }
 
    // Secondary Constructor
    constructor(firstName: String, lastName: String, age: Int, eyeColor: String) : this(firstName, lastName, age)  {
        this.eyeColor = eyeColor
    }
}
```

## Collection
- List, Set, Map
- 기본적으로 Immutable이다. mutable로 선언해야 한다.
- `mutableListOf<String>("a", "b")` 이런 식으로.









## 상식
- 코틀린에서도 멤버 변수를 `프로퍼티`라고 부른다.
- 코틀린에서 모든 클래스는 기본적으로 `final`이다.
  - ∴ 상속을 허용하려면 `open` 키워드를 붙여야 한다.
- 간단하게 타입 체크가 가능하다. `is` 키워드를 사용하면 된다.