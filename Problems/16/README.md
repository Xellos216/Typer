## 🧠 Problem
정수 `x`와 자연수 `n`이 주어질 때, `x`부터 시작해 `x`씩 증가하는 숫자를 `n`개 담은 리스트를 반환하는 함수를 작성하시오.

### Constraints
- `x`: -100,000,000 이상, 100,000,000 이하의 정수
- `n`: 1 이상 1,000 이하의 자연수

### Example
- Input: `x = 2`, `n = 5`
- Output: `[2, 4, 6, 8, 10]`

- Input: `x = 4`, `n = 3`
- Output: `[4, 8, 12]`

- Input: `x = -4`, `n = 2`
- Output: `[-4, -8]`

---

## 🐍 Python Reference Code

```python
def solution(x, n):
    return [x * i for i in range(1, n + 1)]
```
