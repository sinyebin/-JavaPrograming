## 2.1 자바 프로그램의 구조

+ ### 클래스 만들기

class 키워드로 클래스 이름을 선언하고 {} 사이에 필드와 메소드 코드를 작성

    public class Hello {

    }  

+ ### 주석문

프로그램의 실행에 영향을 미치지 않으며, 프로그램에 대한 설명이나 특이사항 등을 자유롭게 기록

    // 한 라인 주석. 행이 끝날 때까지 주석으로 처리  
    /*
        여러 라인 주석으로 /* */로 구성
    */

+ ### main() 메소드

자바 프로그램은 main() 메소드에서부터 실행을 시작

    public static void main(String[] args) {

    }

+ ### 메소드

클래스의 멤버 함수를 지칭
메소드의 이름은 개발자가 지정하며, 갯수에는 제한이 없음

    public static int sum(int n, int m){ //매개변수 n, m   
        return n+m; //n과 m의 합 리턴
    }

메소드 sum()을 호출하는 코드

    int i= 20;
    s=sum(i, 10);  

+ ### 변수 선언

변수는 프로그램 실행 동안 데이터를 저장하는 공간

    int i;
    char a;

지역변수는 메소드 내에 선언되어 사용되는 변수로 메소드 내에서만 사용되며, 실행이 끝나면 소멸

    int i=20; // 변수 i의 선언과 동시에 20으로 초기화

+ ### 문장

모든 문장은 ';' 로 끝남

    int i=20;
    s=sum(i, 20);

+ ### 화면 출력

System.out.println() 이나 System.out.print()를 이용

    System.out.println("Hello"); //"Hello" 문자열 출력
    System.out.println(3); //3 출력
    System.out.println(2*5); //10 출력  



