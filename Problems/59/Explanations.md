## 🔹 while loop + 범위 탐색
```python
while i < len(section):
    start = section[i]
    end = start + m - 1
    ...
```
- 시작 지점에서 `m`만큼 커버할 수 있는 범위 `[start, end]` 계산
- 해당 범위 내에 있는 `section` 값들을 한 번에 덮음

## 🔍 핵심 로직

1. `section`을 왼쪽부터 오른쪽까지 순차 탐색
2. `현재 구역`부터 시작해 `m미터`만큼 덧칠
3. 해당 범위에 포함된 `section` 원소는 모두 덧칠된 것으로 간주 → index 건너뜀
4. 칠해야 할 새로운 구역이 나오면 다시 롤러 사용
