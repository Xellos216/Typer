## 🔹 `itertools.combinations(iterable, r)`
- iterable(리스트 등)에서 **r개의 원소를 뽑는 모든 조합**을 생성
- 순서를 고려하지 않으며, 중복 없이 생성됨
- 예: `combinations([1, 2, 3], 2)` → (1,2), (1,3), (2,3)

## 🔹 `sum()`
- 시퀀스(리스트/튜플 등)의 모든 원소의 합을 반환
- 예: `sum((1, -2, 1))` → `0`

## 🔹 조합 필터링
```python
for comb in combinations(number, 3):
    if sum(comb) == 0:
        count += 1
```
- 3개씩 조합을 만들고, 그 합이 0이면 카운트 증가
