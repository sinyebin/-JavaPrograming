## 2.4 자바에서 키 입력

### System.in

키보드 장치를 직접 제어하고 키 입력을 받는 **표준 입력 스트림** 객체  
입력된 키를 단순한 바이트 정보로 응용프로그램에 제공, 받은 바이트 정보를 문자나 숫자로 변환해야 함  
사용자가 원하는 타입으로 변환해주는 Scanner 클래스를 사용하는것이 효과적

### Scanner를 이용한 키 입력

**Scanner**는 응용프로그램이 키 입력을 쉽게 받을 수 있도록 자바 패키지에서 제공하는 클래스

+ ### Scanner 객체 생성

  Scanner scanner = new Scanner(System.in);

+ ### import문 사용

  import java.util.Scanner;

+ ### Scanner 클래스로 키 입력받기

사용자가 입력하는 키 값을 공백문자(' ', '\t', '\n')를 기준으로 분리하여 토큰 단위로 읽음

    Scanner scanner = new Scanner(System.in);
    String name = scanner.next(); //"kim"
    String city = scanner.next(); //"Seoul"  
    int age = scanner.nextInt(); //20
    double weight = scanner.nextDouble //65.1
    boolean isSingle = scanner.nextBoolean //true

+ ### nextLine()과 next()

공백이 낀 문자열을 입력받기 위해 **nextLine()** 사용  **next()** 공백이 낀 문자열 읽을 수 없음

+ ### Scanner 객체 닫기

System.in도 닫히게 되어 System.in을 사용하여 키 입력 받을 수 없음

    scanner.close();  
    scanner = new Scannel(System.in) //scanner를 닫은 후 다시 scanner로 키 입력 받을 수 없음
