## 2.2 식별자

**식별자**: 클래스, 변수, 상수 메소드 등에 붙이는 이름

+ ### 식별자 이름 규칙
+ 특수문자, 공백은 식별자로 사용할 수 없으나 '_', '$'는 예외
+ 한글 가능
+ if, while, class 등 자바 언어의 키워드는 식별자로 사용 불가
+ 식별자의 첫 번째 문자로 숫자는 불가
+ '_', '$'는 첫 글자로 사용 가능하나 잘 사용하지 않음
+ 대소문자 구별
+ 길이 제한 없음

사용가능 예시

    int name; 
    char student_ID;
    void $func(){ }  
    class Monster3{ }
    int whatsYourNameMyNameIsKitae;
    int barChart; int barchart;
    int 가격;    

사용 불가 예시

    int 3Chapter;
    class if{}
    char false;
    void null(){ } 
    class %calc{ }

+ ### 좋은 이름 붙이는 관습

1. 목적에 맞는 이름
2. 이름 길이에 연연하지 말고 충분히 긴 이름으로 붙이기
3. 이름을 붙이는 언어의 관습 따르기

+ ### 클래스 이름

첫 번째 문자는 대문자로 시작
여러 단어가 복합되면 각 단어의 첫 번째 문자를 대문자로 표시

    public class HelloWorld{}
    class AutoVendingMaching{}

+ ### 변수, 메소드 이름

첫 단어는 소문자, 이후 각 단어의 첫 번째 문자만 대문자로 표기

    int myAge;
    boolean isSingle;
    public int getAge(){return 20;}

+ ### 상수 이름

이름 전체를 대문자로 표기하도록 권장

    final double PI = 3.141592;
