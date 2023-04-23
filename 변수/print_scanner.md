### 형식화된 출력 : printf()

- println()의 단점 : 출력 형식 지정 불가
    - 실수의 자리수 조절 불가 → 소수점 n자리만 출력하려면
    - 10진수로만 출력된다.
- **printf()로 출력형식 지정가능**
```java
System.out.printf(”%.2f”, 10.0/3); //소수점 둘째자리까지 출력
System.out.printf(”%d”, 0x1A); //10진수로 출력
System.out.printf(”%X”, 0x1A); //16진수로 출력
```

### 화면에서 입력 받기 : Scanner

- Scanner : 화면으로부터 데이터를 입력받는 기능을 제공하는 클래스
- Scanner을 사용하려면
```java
//import문 추가
import java.util.*;
        
//Scanner 객체의 생성
Scanner scanner = new Scanner (System.in);
        
//Scanner 객체를 사용
int num = scanner.nextInt(); // 화면에서 입력받은 정수를 num에 저장
String input = scanner.nextLing(); //화면에서 입력받은 내용(한 행)을 input에 저장
```
