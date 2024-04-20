## 2.6 조건문

### 단순 if문

if문의 조건식은 비교 연산이나 논리 연산이 혼합된 식으로 구성되며 조건식의 결과 값은 boolean값
조건식이 true이면 if 내부의 '실행문장'이 실행되고, false이면 if문을 벗어남

    if(n%2==0){
        System.out.println(n+"은 짝수입니다");
    }

### if-else문

if의 조건식이 참인 경우와 거짓인 경우에 각각 실행할 문장을 지시

    if(n%2==0){
        System.out.println(n+"은 짝수입니다");
    }else{
        System.out.println(n+"은 홀수입니다");
    }

### 다중 if-else문

if-else가 연속된 것으로 '조건식'이 차일 경우 해당하는 '실행문장'을 실행 후 다중 if-else문을 벗어남

### switch문

'식'을 계산 후 그 결과 값과 일치하는 case 문으로 분기 후 '실행문자'을 실행 후 break를 만나면 switch문을 벗어남
case 문으로 분기하지 못한 경우 default문으로 분기하여 실행문장을 실행
