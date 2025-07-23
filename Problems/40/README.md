## 🧠 Problem
자연수 `n`이 주어졌을 때, 다음 과정을 거친 값을 리턴하는 함수를 작성하시오:

1. `n`을 **3진법**으로 변환
2. 그 값을 **뒤집음**
3. 뒤집힌 값을 **다시 10진법 정수**로 변환하여 반환

### Constraints
- 1 ≤ n ≤ 100,000,000

### Example

- Input: `45`  
  → 3진법: `"1200"`  
  → 뒤집기: `"0021"`  
  → 10진수: `7`  
  → Output: `7`

- Input: `125`  
  → 3진법: `"11122"`  
  → 뒤집기: `"22111"`  
  → 10진수: `229`  
  → Output: `229`

---

## 🐍 Python Reference Code

```python
def solution(n):
    ternary = ''
    while n:
        ternary = str(n % 3) + ternary
        n //= 3
    reversed_ternary = ternary[::-1]
    return int(reversed_ternary, 3)
```
