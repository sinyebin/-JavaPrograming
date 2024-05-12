## 3.2 continue문과 break문

### continue문

반복문을 빠져나가지 않으면서 즉시 다음 반복으로 넘어가고자 할 때 사용

    continue;

for문: '반복 후 작업'으로 분기  
while, do-while문: 조건식 검사하는 과정으로 분기

    for(초기문; 조건식; 반복 후 작업){
        ...
        continue;
    }

    while(조건식){
        ...
        continue;
    }

    do{
        ....
        continue;
    }while(조건식);

### break문

하나의 반복문을 즉시 벗어날 때 사용
중첩 반복의 경우 안쪽 반복문에서 break문이 실행되면, 안쪽 반복문만 벗어나게 되어 바깥 쪽 반복문 내에서 실행 유지

    break;

