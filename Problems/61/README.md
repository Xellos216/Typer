## 🧠 Problem
로또 번호는 6개의 숫자로 이루어져 있고, 당첨 번호도 6개입니다.  
알고 있는 로또 번호 중 일부는 `0`으로 표기되며, 이는 **알 수 없는 번호**를 의미합니다.

로또 번호 배열 `lottos`와 당첨 번호 배열 `win_nums`가 주어질 때,  
당첨 가능한 **최고 순위**와 **최저 순위**를 순서대로 담은 배열을 반환하는 함수를 작성하세요.

---

### Constraints
- `lottos`의 길이는 6이고, 0 ≤ `lottos[i]` ≤ 45
- `win_nums`의 길이도 6이며, 1 ≤ `win_nums[i]` ≤ 45
- 중복되는 숫자는 없습니다.

---

### Example

- Input:
```python
lottos = [44, 1, 0, 0, 31, 25]
win_nums = [31, 10, 45, 1, 6, 19]
```

- Output:
```python
[3, 5]
```

- 설명:
  - 알 수 없는 번호(`0`)는 2개
  - 실제 맞춘 번호는 2개 (`1`, `31`)
  - 최고: 2 + 2 = 4개 일치 → 3등
  - 최저: 2개 일치 → 5등

---

## 🐍 Python Reference Code
```python
def solution(lottos, win_nums):
    zero = lottos.count(0)
    match = len(set(lottos) & set(win_nums))

    def get_rank(x):
        return 7 - x if x >= 2 else 6

    return [get_rank(match + zero), get_rank(match)]
```
