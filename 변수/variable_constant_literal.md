### 변수, 상수, 리터럴
1. **변수 (varible)** : 하나의 값을 저장하기 위한 공간 → 변경 O
2. **상수 (constant)** : 한 번만 값을 저장 가능한 변수 → 변경 X ⇒ **final**을 사용한다.
3. **리터럴 (literal)** : 그 자체로 값을 의미하는 것 → 기존의 상수 

ex) int score = **100**; 에서 **100**은 리터럴을 의미한다.

```java
int score = 100;
score = 200;

final int MAX = 100;
MAX = 200; //에러

char ch = 'A';
String str = "abc"; 
```

### 리터럴의 접두사와 접미사

| 종류 | 리터럴 | 접미사 | 크기 (byte) |
| --- | --- | --- | --- |
| 논리형(boolean) | false, true | 없음 | 1byte |
| 정수형 (byte, short, int, long) | 123, 0b0101, 077, 0xFF, 100L | L (long을 의미) | byte (=1byte),short(=2byte),int (=4byte),long (=8byte) |
| 실수형 (float, double) | 3.14, 0e8, 1.4f, 0x1, 0p-1 | f, d → d가 default 값 |  |
| 문자형(char) | ‘A’, ‘1’, ‘\n’ | 없음 | 2byte |
| 문자열 | "ABC”, “123”, “A”, “true” | 없음 |  |
```java
String s1 = "AB";
String s2 = new String("AB");
//원래는 s2와 같이 새로운 클래스 객체를 생성해야 하지만
//String의 경우 많이 사용되므로 s1과 같이 사용하는 것이 좋다.
```

### 기본형과 참조형

1. **기본형 (Primitive Type)**
    1. 오직 8개 : boolean, char, byte, short, int, long, float, double
    2. 실제 값을 저장
    3. 표현범위 
        1. n비트로 표현할 수 있는 값의 개수 : 2^n개
        2. n비트로 표현할 수 있는 부호없는 정수의 범위 : 0~2^(n-1)
        3. n비트로 표현할 수 있는 부호있는 정수의 범위 : -2^(n-1) ~ 2^(n-1) - 1
    4. 정밀도 : float = 7자리, double = 15자리
2. **참조형 (Reference type)**
    1. 기본형을 제외한 나머지 : String, System, Date 등 (무한개)
    2. 메모리 주소를 저장 → 4byte, 8byte
    
 ```java
Date today; // 참조형 변수 today를 선언
today = new Date(); // today에 객체 주소를 저장
```
