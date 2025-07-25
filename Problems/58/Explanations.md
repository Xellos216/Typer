## 🔹 `itertools.combinations`
- `combinations(nums, 3)` → nums 리스트에서 서로 다른 3개 조합 생성
- 결과는 튜플 리스트로 반환됨

## 🔹 3중 for문 조합
- i < j < k 조건을 만족하도록 반복문 구성
- 각 인덱스 조합으로 세 수를 선택하고 합산 후 소수 여부 검사

## 🔹 소수 판별 (is_prime)
```python
def is_prime(n):
    if n < 2: return False
    for i in range(2, int(n**0.5)+1):
        if n % i == 0:
            return False
    return True
```
- n의 제곱근까지만 나눠보면 됨 → 시간 복잡도 감소
