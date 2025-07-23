## Syntax

## 🔹 `datetime` 방식

### `datetime.date(yyyy, mm, dd)`
- 날짜 객체 생성
- 예: `datetime.date(2016, 5, 24)`

### `.strftime('%a')`
- 요일의 3글자 문자열 반환
- 예: `'Tue'`, `'Wed'`, ...

---

## 🔹 수학 계산 방식

### 윤년 월별 날짜 수
```python
month_days = [31, 29, 31, 30, 31, 30, 31, 31, 30, 31, 30, 31]
```

### 누적 일 수 계산
```python
total_days = sum(month_days[:a - 1]) + (b - 1)
```

### 요일 리스트와 인덱싱
```python
days = ["FRI", "SAT", "SUN", "MON", "TUE", "WED", "THU"]
return days[total_days % 7]
```

→ 기준일(1월 1일)이 금요일이기 때문에 `FRI`부터 시작

---

## 🔍 예시 흐름

> 입력: a = 5, b = 24  
→ 1월~4월까지 일 수 = `sum([31,29,31,30]) = 121`  
→ 총 경과일 = `121 + (24 - 1) = 144`

→ 144 % 7 = 3  
→ days[3] = `"TUE"`  
→ 정답: `"TUE"`
