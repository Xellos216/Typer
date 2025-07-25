## 🔹 사용된 함수 설명
- `zip(a, b)` → 리스트 a와 b를 쌍(pair)으로 묶어주는 함수  
  예: `zip([1,2], [True, False])` → `(1, True), (2, False)`

## 🔹 사용된 문법 설명
- `for num, sign in zip(...)`  
  → zip을 통해 나온 두 값을 각각 `num`, `sign`으로 분리해서 반복

- `if sign:`  
  → sign이 `True`일 때만 실행되는 조건문.  
    불리언 비교는 `== True` 대신 이렇게 축약 가능.

- `+=`, `-=`  
  → 값을 누적해서 더하거나 빼는 축약 대입 연산자
