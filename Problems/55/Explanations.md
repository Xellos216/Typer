## Syntax

## 🔹 collections.deque

- `deque`는 양방향 큐
- `.popleft()` → 앞에서 제거 (O(1) 성능)
- 리스트의 `pop(0)`은 O(n)이기 때문에 비효율적

---

## 🔹 리스트 인덱스 방식

- `i`, `j` 변수를 사용해 각 cards1, cards2의 현재 위치를 추적
- 리스트 구조는 유지되고, 슬라이싱/삭제 없이 처리 가능

---

## 🔍 예시 흐름 설명

### 예: cards1 = ["i", "drink", "water"], cards2 = ["want", "to"], goal = ["i", "want", "to", "drink", "water"]

| 단계 | word  | cards1[i] | cards2[j] | 동작            |
|------|-------|-----------|-----------|------------------|
| 1    | "i"   | "i"       | "want"    | cards1에서 사용 |
| 2    | "want"| "drink"   | "want"    | cards2에서 사용 |
| 3    | "to"  | "drink"   | "to"      | cards2에서 사용 |
| 4    | "drink"| "drink"  | (없음)    | cards1에서 사용 |
| 5    | "water"| "water"  | (없음)    | cards1에서 사용 |

✅ 최종적으로 `"Yes"` 리턴됨

---

## ❗ 주의 포인트

- `"Yes"` / `"No"` → 반드시 **대소문자 정확히** 출력할 것
- `"no"`로 출력하면 테스트 실패
