## 🔹 슬라이싱
- `array[i-1:j]`는 리스트에서 i번째부터 j번째까지 자름 (파이썬 인덱스는 0부터 시작하므로 `i-1`)
- 예: `array = [1, 2, 3, 4, 5]`, `array[1:4]` → `[2, 3, 4]`

## 🔹 `sorted()` 함수
- 리스트를 정렬한 새 리스트 반환
- 예: `sorted([3, 1, 2])` → `[1, 2, 3]`

## 🔹 리스트 컴프리헨션
- `[...] for i, j, k in commands`
  → 명령마다 슬라이싱 → 정렬 → k번째 원소 추출하여 새 리스트 생성

## 🔹 for 반복문
- 명령어를 하나씩 꺼내와 처리할 때 사용
- 예:
```python
  result = []
  for command in commands:
      i, j, k = command
      sliced = array[i-1:j]
      sliced.sort()
      result.append(sliced[k-1])
```
