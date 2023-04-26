### 반올림, 나머지 연산자

- **반올림 : Math.round()**
    - 실수를 **소수점 첫째자리**에서 반올림한 정수를 반환한다.
    - ex) Math.round(pi * 1000) /1000.0 → 3142 / 1000.0 → 3.142

### 임의의 정수 만들기

- Math.random() : 0.0 ~ 1.0 사이의 임의의 double값을 반환
- 원하는 값 : 1~3까지의 정수
    - 각 변에 3을 곱한다. → 0.0 * 3 ≤ Math.random() * 3 < 1.0 * 3
    - 각 변을 int형으로 변환한다.  → (int) 0.0 ≤ (int) (Math.random() * 3) < (int) 3.0
    - 각 변에 1을 더한다. → 0+1 ≤ (int) (Math.random() * 3) + 1 < 3+1

### 문자열의 비교

- == 대신 equals()를 사용해야 한다.
```java
String str1 = "abc";
String str2 = "abc"

System.out.println(str1 == str2); //true
System.out.println(str1.equals(str2)); //true

String str1 = new String("abc");
String str2 = new String("abc");

System.out.println(str1 == str2); //false
System.out.println(str1.equals(str2)); //true
```
