## Syntax

## 🔹 사용된 함수 및 문법 설명

### 🔹 `set()` 집합 자료형
- 중복 제거를 위한 자료 구조
- 예: `set([1, 2, 2, 3])` → `{1, 2, 3}`

### 🔹 중첩 for문
- 이중 반복을 통해 모든 쌍 탐색
```python
for i in range(len(numbers)):
    for j in range(i+1, len(numbers)):
        result.add(numbers[i] + numbers[j])
```

### 🔹 리스트 컴프리헨션 + 집합
- 집합 컴프리헨션 사용 → 중복 없이 한 줄로 표현 가능
```python
{numbers[i] + numbers[j] for i in range(len(numbers)) for j in range(i+1, len(numbers))}
```

### 🔹 `sorted()` 함수
- 리스트나 집합 등을 오름차순으로 정렬한 새 리스트 반환
- 예: `sorted({3, 1, 2})` → `[1, 2, 3]`

---

## 🔍 예시

```python
numbers = [2, 1, 3, 4, 1]

# 가능한 모든 쌍의 합:
# 2+1=3, 2+3=5, 2+4=6, 2+1=3
# 1+3=4, 1+4=5, 1+1=2
# 3+4=7, 3+1=4
# 4+1=5
# → {2,3,4,5,6,7} → 정렬 → [2,3,4,5,6,7]
```
