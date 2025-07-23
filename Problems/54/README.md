## 🧠 Problem
2016년 1월 1일은 금요일입니다.  
2016년 a월 b일은 무슨 요일일까요?

두 수 `a`, `b`를 입력받아 2016년 a월 b일의 요일을  
`"SUN", "MON", "TUE", "WED", "THU", "FRI", "SAT"` 형식으로 리턴하는 함수를 작성하세요.

---

### Constraints
- 2016년은 윤년입니다 (2월이 29일까지 존재)
- 입력되는 날짜는 실제 존재하는 날짜만 주어집니다

### Example
```python
a = 5, b = 24 → return "TUE"
```

---

## 🐍 Python Reference Code

### ✅ 1. `datetime` 모듈 사용 (권장)

```python
import datetime

def solution(a, b):
    date = datetime.date(2016, a, b)
    return date.strftime('%a').upper()
```

- `datetime.date(2016, a, b)`: 날짜 객체 생성
- `strftime('%a')`: 요일을 3글자 약어로 반환 → `'Tue'`
- `.upper()`: `'TUE'`

---

### ✅ 2. 수학적 계산 방식

```python
def solution(a, b):
    month_days = [31, 29, 31, 30, 31, 30, 31, 31, 30, 31, 30, 31]
    days = ["FRI", "SAT", "SUN", "MON", "TUE", "WED", "THU"]

    total_days = sum(month_days[:a - 1]) + (b - 1)
    return days[total_days % 7]
```

- `2016년 1월 1일 = FRI` → 요일 인덱스 기준
- a월 b일까지 총 날짜 수 계산 후 `7로 나눈 나머지`로 요일 인덱스를 구함

---

## ✅ Summary

| 방식 | 장점 | 비고 |
|------|------|------|
| `datetime` | 코드가 매우 간단함 | 실무에선 가장 많이 사용됨 |
| 수학 계산 | 로직 구조 연습 가능 | 모듈 없이도 동작 |

