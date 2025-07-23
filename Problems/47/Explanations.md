## Syntax

## 🔹 사용된 함수 및 문법 설명

### 🔹 `sorted()` 함수
- 리스트 등을 정렬하여 새로운 리스트 반환
- `key` 매개변수를 사용해 사용자 정의 기준으로 정렬 가능
  예: `sorted(["cat", "apple"], key=len)` → `["cat", "apple"]` (길이 기준)

### 🔹 `lambda` 표현식
- 익명 함수를 생성하는 키워드
- `lambda x: (x[n], x)`는 매개변수 `x`를 받아 `(x[n], x)` 형태의 튜플 반환
- 정렬 시 여러 기준을 동시에 설정 가능

### 🔹 튜플 정렬
- `sorted(strings, key=lambda x: (x[n], x))`는  
  1. 첫 번째 기준: `x[n]` (n번째 문자)
  2. 두 번째 기준: `x` (문자열 전체)  
  두 기준을 순차적으로 비교해 정렬

---

## 🔍 예시

```python
strings = ["sun", "bed", "car"]
n = 1

# lambda x: (x[1], x)
# 정렬 기준: ("u", "sun"), ("e", "bed"), ("a", "car")
# 정렬 결과: ("a", "car") < ("e", "bed") < ("u", "sun")
# → ["car", "bed", "sun"]
```
