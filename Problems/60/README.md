## 🧠 Problem
숫자나라 기사단의 각 기사에게는 1번부터 `number`까지 번호가 지정되어 있습니다. 기사들은 무기점에서 무기를 구매하려고 합니다.

각 기사는 자신의 기사 번호의 약수 개수에 해당하는 공격력을 가진 무기를 구매해야 합니다.  
단, 이웃나라와의 협약에 의해 공격력의 제한수치를 정하고, 제한수치보다 큰 공격력을 가진 무기를 구매해야 하는 기사는 협약에 따라 정한 공격력을 가지는 무기를 구매해야 합니다.
또한 무기를 만들 때, 공격력 1당 1kg의 철이 필요합니다. 

기사단원의 수를 나타내는 정수 number와 이웃나라와 협약으로 정해진 공격력의 제한수치를 나타내는 정수 limit와 제한수치를 초과한 기사가 사용할 무기의 공격력을 나타내는 정수 power가 주어졌을 때, 
무기점의 주인이 무기를 모두 만들기 위해 필요한 철의 무게를 return 하는 solution 함수를 완성하시오.

---

### Constraints
- 1 ≤ `number` ≤ 100,000
- 1 ≤ `limit` ≤ 100
- 1 ≤ `power` ≤ `limit`

---

### Example

- Input: `number = 5`, `limit = 3`, `power = 2`  
  Output: `10`

- Input: `number = 10`, `limit = 3`, `power = 2`  
  Output: `21`

입출력 예 설명:

- 예제 1: 1부터 5까지의 약수 개수는 `[1, 2, 2, 3, 2]`이고, 모두 `limit` 이하이므로 그대로 더해서 `10`
- 예제 2: 1부터 10까지의 약수 개수는 `[1, 2, 2, 3, 2, 4, 2, 4, 3, 4]`. 여기서 `4 > limit` 이므로 `power = 2`로 대체  
  → `[1,2,2,3,2,2,2,2,3,2]`의 합 = `21`

---

## 🐍 Python Reference Code
```python
def solution(number, limit, power):
    def count_divisors(n):
        count = 0
        for i in range(1, int(n**0.5) + 1):
            if n % i == 0:
                count += 1
                if i != n // i:
                    count += 1
        return count

    total = 0
    for i in range(1, number + 1):
        power_value = count_divisors(i)
        if power_value > limit:
            total += power
        else:
            total += power_value
    return total
```
