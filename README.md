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
    + 기본적으로 리턴 타입과 함수이름, 인자를 같은 줄에 작성하지만, 정해진 가로 줄 길이를 초과할 경우 줄바꿈하여 작성할 수 있다.
    ```
    //기본 형식
    ReturnType FunctionName(Type var1, Type var2)
    {
      DoSomething();
    }
    
    // 한줄에 작성하지 못할 경우, 리턴 타입 작성 후 줄바꿈하여 작성한다.
    ReturnType
    ReallyLongFunction(Type var1, Type var2, Type var3)
    {
      DoSomething();
    }
    
    //진짜 긴 경우
    ReturnTeyp ReallyLongLongLongFunctionName(
        Type var1,
        Type var2,
        Type var3)
    {
      DoSomething();
    }
    ```
    + 주의 사항
      + 여는 괄호 "("는 항상 함수 이름과 같은 줄에 작성한다.
      + 닫는 괄호 ")"는 항상 마지막 인자에 붙여서 작성한다.
      + 함수 이름과 여는 괄호 "("사이에는 스페이스를 넣지 않는다.
      + 여는 과로 "("밑 닫는 괄호 ")"와 인자 사이에는 스페이스를 넣지 않는다.
      + 각 인자 사이는 쉼표 + 하나의 스페이스를 사용하여 구분한다.
      + 여는 중괄호 "{"는 항상 닫는 괄호 "}" 다음 줄에 작성한다.
      + 모든 인자는 이름을 가져야 하며, 선언과 구현에서 같은 이름을 가져야 한다.
      + 함수 내 기본 들여쓰기는 2개의 스페이스이다.
      + 모든 인자들을 가능한 한 정렬되어야 한다.
      + 인자들이 다음 줄로 이동할 경우 2개의 스페이스 들여쓰기를 사용한다.
      + 인자들이 다음 줄로 이동할 경우 한 줄당 하나의 인자만 작성한다.
  + 함수 호출
    + 기본적으로 한 줄로 작성하지만, 정해진 가로 줄 길이를 초과할 경우 줄바꿈하여 작성할 수 있다.
    ```
    // 기본 형식
    bool retval = FunctionName(argument1, argument2, argument3);
    
    // 같은 줄에 작성하지 못하는 경우, 첫번째 인자를 제외한 나머지 인자들을 별도의 줄에 작성한다.
    // 인자의 시작위치는 통일한다.
    bool retval = ReallyLongLongLongFunctionName(argument1,
                                                  argument2,
                                                  argument3);
    ```
    
