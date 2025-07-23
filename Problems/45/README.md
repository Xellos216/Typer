## 🧠 Problem
문자열 `s`의 각 알파벳을 n만큼 민 결과를 반환하는 문제입니다. 
- 공백은 그대로 두며, 알파벳만 n칸 뒤의 알파벳으로 변경합니다.
- 알파벳은 대소문자를 유지해야 하며, z를 밀었을 경우 a로 돌아가야 합니다.

### Constraints
- `s`는 알파벳 소문자, 대문자, 공백으로만 이루어져 있습니다.
- `s`의 길이는 8000 이하입니다.
- `n`은 1 이상, 25 이하의 자연수입니다.

### Example
- Input: `"AB"`, `1`
- Output: `"BC"`
- Input: `"a B z"`, `4`
- Output: `"e F d"`

---

## 🐍 Python Reference Code

```python
def solution(s, n):
    answer = ''
    for c in s:
        if c.isupper():
            answer += chr((ord(c) - ord('A') + n) % 26 + ord('A'))
        elif c.islower():
            answer += chr((ord(c) - ord('a') + n) % 26 + ord('a'))
        else:
            answer += c
    return answer
```