## 🔹 약수 개수 구하기
```python
for i in range(1, int(n**0.5) + 1):
    if n % i == 0:
        count += 1
        if i != n // i:
            count += 1
```
- 약수는 `√n`까지만 확인해도 충분
- `i`와 `n // i` 두 쌍이 약수 관계 (단, `i == n // i`인 경우 중복 제외)

## 🔍 주요 로직 흐름

1. `1`부터 `number`까지 모든 기사 번호에 대해 순회
2. 각 번호에 대해 약수 개수(공격력)를 구함
3. 공격력이 `limit`보다 크면 → `power`로 대체
4. 각 기사의 무기 공격력을 모두 합산
5. 무기 공격력 = 철의 무게(1kg당 1 공격력) → 총합을 그대로 리턴
