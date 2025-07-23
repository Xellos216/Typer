## Syntax

## 🔹 사용된 문법 설명

### 🔹 range(start, end, step)
- 특정 범위의 수열 생성
- `range(2, n+1, 2)`는 2부터 n까지 2씩 증가하는 짝수 시퀀스
- 예: `range(2, 11, 2)` → [2, 4, 6, 8, 10]

### 🔹 for 반복문
- 시퀀스 요소를 순회하며 반복 실행
- 예:
```python
for i in range(2, n+1, 2):
    answer += i
```

### 🔹 누적 덧셈 `+=`
- `answer += i`는 `answer = answer + i`의 축약 표현

---

## 🔍 예시

```python
n = 10
# 2 + 4 + 6 + 8 + 10 = 30 → return 30

n = 4
# 2 + 4 = 6 → return 6
```
