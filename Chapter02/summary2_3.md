## 2.3 자바의 데이터 타입

**데이터 타입**: 자바에서 다룰 수 있는 데이터 종류

+ ### 기본 타입(basic type): 8개
+ boolean
+ char
+ byte
+ short
+ int
+ long
+ float
+ double

+ ### 레퍼런스 타입(reference type): 1개
+ 배열에 대한 레퍼런스
+ 클래스에 대한 레퍼런스
+ 인터페이스에 대한 레퍼런스

### 자바의 기본 타입

**정수**: byte, short, int, long  
**실수**: float, double  
문자 하나는 2바이트의 유니코드
char 타입은 크기가 2 byte  
**문자열**은 자바의 기본 타입x -> String 클래스 이용

    String strName="kitae";  

### 문자열

기본 타입x
JDK에 제공하는 String 클래스 이용

    String toolName="JDK";  

문자열과 기본 타입의 + 연산이 실행되면, 기본 타입의 값이 문자열로 바뀌고 새로운 문자열 생성

    toolName + 1.8 + "("+3+","+5+")"
    System.out.println(toolName + "이 출시됨");

### 변수와 선언

**변수**: 데이터를 저장하는 공간

+ ### 변수 선언

데이터 타입과 이름으로 변수 선언  
같은 타입의 변수를 여러 개 선언 시 콤마로 분리

    char c1, c2, c3;  

+ ### 변수 선언과 동시에 초기화

변수 선언과 동시에 초기값 지정 가능

    int radius = 10;
    char c1 = 'a', c2='b', c3='c';
    double weight=75.56;  

+ ### 변수 읽기와 저장

변수를 선언한 후 변수에 값을 저장하고 읽기 가능

    radius=10*5; //변수 radius에 10*5의 결과 50 저장
    c1='r';  // 변수 c1에 문자 'r' 저장
    weight=weight+5.0;  // 변수 weight의 값을 읽고 5.0을 더해 weight에 다시 저장  

### 리터럴(literal)

**리터럴**: 프로그램에 직접 표현한 값

+ ### 정수 리터럴

**정수 리터럴**은 4가지 유형이 존재하며 int 타입으로 자동 컴파일

    int n= 15; //십진수 15  
    int m=015; //015는 8진수로서 십진수 13
    int k=0x15; // 0x15는 16진수로서 십진수 21
    int b=0b0101; //0b0101은 2진수로서 십진수 5
    long g=24L; 24L은 24l과 동일  

+ ### 실수 리터럴

**실수 리터럴**은 소수점 형태나 지수 형태로 실수를 표현한 값이며 double 타입으로 자동 처리

    double d=0.1234;
    double e-1234E-4; //1234E-4= 1234*10^-4이므로 0.1234와 동일  
    float f =0.1234f; //f=0.1234로 하면 컴파일 오류  
    double w = .1234D; //.1234D dhk .1234는 동일  

+ ### 문자 리터럴

**문자 리터럴**은 당일 인용부호('')로 문자를 표현하거나 \u 다음에 문자의 유니코드 값을 사용하여 표현

+ ### 논리 리터럴과 boolean 타입

**논리 리터럴**은 true, false whswo, boolean 타입의 변수에 직접 치환하거나 조건문에 사용

    boolean a = true;
    boolean b = 10> 0; //10>0가 참이므로 b 값은 true
    boolean c=1; // 타입 불일치 오류 
    while(true) { //자바에서 무한 루프. while(1)로 하면 안됨
        ...
    } 

### 상수

**상수**는 변수 선언 시 final 키워드를 사용, 변수와 달리 실행 중에 값이 바꿀 수 없음

    public class CircleArea{
        public static void main(String args[]){ 
            final double PI=3.14; //원주율을 상수로 선언
            
            double radius = 10.0; //원의 반지름
            double circleArea = radius*radius*PI; //원의 면적 계산  

            //원의 면적을 화면에 출력한다.
            System.out.println("원의 면적 = "+circleArea);
        }
    }  

### 타입변환

**타입 변환**은 변수나 상수 혹은 리터럴의 타입을 다른 타입으로 바꾸는 것

+ ### 자동타입 변환

치환문(=)이나 수식 내에서 타입이 일치하지 않을 때, 컴파일러는 오류 대신 작은 타입을 큰 타입으로 자동 변환

    long m = 25; //리터럴 25는 int 타입. 25가 long 타입으로 자동 변환  
    double d = 3.14 * 10; /// 실수 연산을 하기 위해 10이 10.0으로 자동 변환  

+ ### 강제 타입 변환

**강제 타입 변환**은 개발자가 강제로 타입 변환을 지시하는 경우

    int n=300;
    byte b=n; //컴파일 오류. int 타입은 byte 타입으로 자동 변환 안됨  
    byte b=(byte)n; //n을 byte 타입으로 강제 변환. b=44

300에서 byte 타입(0~255) 256 범위를 초과하여 44(300%256=44)가 변수에 저장되어 데이터 손실 발생  
강제 타입 변환을 캐스팅이라고 부름