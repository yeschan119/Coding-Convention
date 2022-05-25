# Coding-Convention

## purpose
  + record the coding convention for clean code
## C language
  + 줄 길이
    + 코드의 각 줄은 120문자를 넘지 않게 한다.
  + 문자 형식
    + 문자는 되도록 ASCII 문자를 사용하고, ASCII가 아닌 문자를 사용할 경우에는 UTF-8 형식을 사용한다.
  + 들여쓰기
    + 단계 당 2개의 스페이스로 들어쓰기 하고 탭은 사용하지 않는다.
  + 중괄호
    + 중괄호로 묶이는 모든 코드 블럭에서, 각 중활호 {}는 구문에 따라 같은 줄에 작성하거나 줄바꿈하여 작성한다.
    ```
    // 함수 내용을 여는 중괄호와 닫는 중괄호는 모두 새로운 줄에 작성한다.
    int Function(int a)
    {
    };
    
    //구조체 내용을 여는 중괄호와 닫는 중괄호는 모두 새로운 줄에 작성한다.
    struct Structure
    {
    };
    
    //enum ecode
    {
    };
    
    //조건문 내용을 묶는 중괄호는 같은 줄에 작성하고, 닫는 중괄호는 새로운 줄에 작성한다.
    //단, 가독성이 현저하게 낮은 경우 가독성 향상을 위해 묶는 중괄호를 새로운 줄에 작성할 수 있다.
    if (condition) {
      Do Something();
    }
    
    //switch 문을 묶는 중괄호는 같은 줄에 작성하고, 닫는 중괄호는 새로운 줄에 작성한다.
    //단, 가독성이 현저하게 낮은 경우 가독성 향상을 위해 묶는 중괄호를 새로운 줄에 작성할 수 있다.
    switch (var) {
      case 0:
        ...
     }
    ```
  + 모든 조건문(if, switch)과 반복문(for, while)에서 중괄호를 반드시 사용한다. 본문이 한 줄인 경우에도 중괄호를 사용한다.
    ```
    if (condition) {
      DoSomething();
    }
    
    while (condition) {
      DoSomething();
    }
    ```
  + 강제 줄 바꿈
    + 모든 조건문(if, switch), 반복문(for, while)의 표현식이 정해진 가로 줄 길이를 초과할 경우, 가독성 좋게 정렬하여 줄바꿈 한다.
      + 일관성 있게 줄바꿈한다.
      + 각 줄의 시작지점을 통일한다.
      + 보통 연산자 뒤에서 줄바꿈한다.
    ```
    if ((this_one_thing > this_other_thing) &&
        (a_third_thing == a_fourth_thing) &&
        yet_another &&
        last_one) {
       ...
    }
    ```
  + 함수 선언과 정의
    + 기본적으로 리턴 타
