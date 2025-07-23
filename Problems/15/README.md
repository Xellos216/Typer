## 🧠 Problem
자연수 `n`이 주어질 때, `n`을 `x`로 나누었을 때 나머지가 1이 되는 가장 작은 자연수 `x`를 구하여 반환하는 함수를 작성하시오.

### Constraints
- 3 ≤ `n` ≤ 1,000,000

### Example
- Input: `n = 10`
- Output: `3`  
  (10 % 3 = 1, 3보다 작은 자연수 중 조건을 만족하는 수 없음)

- Input: `n = 12`
- Output: `11`  
  (12 % 11 = 1)

---

## 🐍 Python Reference Code

```python
def solution(n):
    for x in range(2, n):
        if n % x == 1:
            return x
```
