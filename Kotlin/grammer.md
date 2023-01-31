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
+ `!!`연산자: 객체가 null이 아닌 것을 보장해줌. `getString()!!`

- `?` 키워드가 `선언` / `안전 접근` 두 가지로 쓰이기 때문에 잘 구분할 것!

### 삼항 연산자
- 코틀린에는 삼항 연산자가 없다.
- 삼항 연산자를 if-else 한줄구문으로 구현 가능.

### 엘비스 연산자
- `?:`
- ex) `b?.length ?: -1`
- 있으면 그대로 출력, 아니면 기본값 출력 (JS와 Lua의 `or` 처럼)