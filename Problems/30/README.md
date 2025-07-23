## 🧠 Problem
문자열 `s`가 주어졌을 때, **가운데 글자**를 리턴하는 함수를 작성하시오.  
- 문자열의 길이가 **홀수**이면 가운데 **한 글자**
- 문자열의 길이가 **짝수**이면 가운데 **두 글자**

### Constraints
- `s`는 길이 1 이상 100 이하인 문자열

### Example
- Input: `"abcde"`  
- Output: `"c"`

- Input: `"qwer"`  
- Output: `"we"`

---

## 🐍 Python Reference Code

```python
def solution(s):
    n = len(s)
    if n % 2 == 0:
        return s[n // 2 - 1 : n // 2 + 1]
    else:
        return s[n // 2]
```
