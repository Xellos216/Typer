## 🔹 set()
- Creates an **unordered collection of unique elements**.  
  Useful for fast membership checks and set operations like difference and subtraction.

## 🔹 sorted(iterable)
- Returns a **new list** containing all elements from the iterable in ascending order.  
  Guarantees deterministic neighbour search from the lowest student number upward.

## 🔹 list.remove(x)
- Removes the **first occurrence** of `x` from the list / set.  
  Here it is used on a `set`, which simply discards the element.

---

## 📌 핵심 조건 정리
1. 같은 학생 번호가 `lost`와 `reserve`에 모두 존재하면, 그 학생은 **자기 옷만 남아 대여 불가**  
2. 체육복은 **인접 학생**(`i ± 1`)에게만 빌려줄 수 있음  
3. 한 벌의 여분은 **한 번만** 빌려줄 수 있음  
4. 빌려주기 결과로 체육복을 가진 학생 수가 **최대**가 되도록 해야 함  

## 🔍 풀이 로직
1. `real_lost = set(lost) - set(reserve)`  
   `real_reserve = set(reserve) - set(lost)`  
   → 대여 가능자·필요자 확정
2. `real_reserve`를 **오름차순 순회**하며  
   `r − 1` → `r + 1` 순으로 이웃에게 대여 (그리디)  
   → 한 번 빌려주면 `real_lost`에서 제거
3. 최종적으로 체육복이 없는 인원 수 = `len(real_lost)`  
   **참여 가능 인원** = `n − len(real_lost)` 반환

### 배열 기반 대안
- 모든 학생의 옷 개수를 배열 `clothes`로 관리 (0,1,2)  
- 앞번호 → 뒷번호 순서로 순회하며 부족 시 이웃에게 차감·추가  
- 최종 `clothes[i] > 0`인 학생 수를 합산
