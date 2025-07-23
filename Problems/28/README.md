## 🧠 Problem
0부터 9까지의 숫자 중 일부가 담긴 리스트 `numbers`가 주어진다.  
이때, **리스트에 없는 숫자들을 모두 찾아 더한 값**을 반환하는 함수를 작성하라.

### Constraints
- `numbers`는 길이 1 이상 9 이하의 리스트
- `numbers`의 원소는 0 이상 9 이하의 서로 다른 숫자
- 0부터 9까지 모든 숫자 중 빠진 숫자는 반드시 존재함

### Example
- Input: `[1, 2, 3, 4, 6, 7, 8, 0]`
- Output: `14`  
  (없는 숫자: 5, 9 → 5 + 9 = 14)

- Input: `[5, 8, 4, 0, 6, 7, 9]`
- Output: `6`  
  (없는 숫자: 1, 2, 3 → 1 + 2 + 3 = 6)

---

## 🐍 Python Reference Code

```python
def solution(numbers):
    return sum(set(range(10)) - set(numbers))
```
