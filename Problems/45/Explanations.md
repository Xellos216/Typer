## 🔹 사용된 함수 설명
- `ord(char)` → 문자를 아스키 코드로 변환
- `chr(num)` → 아스키 코드 값을 문자로 변환
- `isupper()` → 대문자인지 확인
- `islower()` → 소문자인지 확인

## 🔹 사용된 문법 설명
- `(ord(c) - ord('A') + n) % 26 + ord('A')` 
  → A~Z 범위에서 n만큼 민 다음 다시 문자로 복원하는 공식
- `(ord(c) - ord('a') + n) % 26 + ord('a')` 
  → a~z 범위에서 n만큼 민 다음 다시 문자로 복원하는 공식
