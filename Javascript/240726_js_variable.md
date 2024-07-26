## 변수를 선언하는 규칙

1. 이름은 의미 있게 짓는다.
2. 여러 단어를 연결한 변수 이름은 Camel Case로 만들어 준다.
3. 선언할 수 없는 이름도 있다.
   1. 변수의 첫 글자는 반드시 문자나 밑줄(\_) 또는 달러 기호($)로 시작해야 한다.
   2. 따라서 숫자나 그 외의 다른 기호로는 시작할 수 없다.

## document.querySelector("#result").innerHTML의 의미

소스 코드를 그대로 읽으면 '문서(document)에서 선택자를 사용하여(querySelector) id 값이 result인 태그("#result")를 선택하고 HTML에 삽입한다(innerHTML)는 의미이다.

## let과 const 예약어

ES6 버전부터 변수를 선언할 때 var 예약어 외에 let와 const 예약어를 사용할 수 있다.

let -> 블록({}으로 묶은 범위)을 벗어나면 사용 X
const -> 상숫값을 선언할 때 사용

## undefined

자료형을 지정하지 않았을 때의 유형이다. <br>
예를 들어, 변수를 선언만 하고 값을 정의하지 않으면 undefined가 된다.

## typeof 연산자

변수의 자료형을 확인할 수 있다. <br>

**자료형의 종류**<br>

- number(숫자형)
- string(문자열)
- boolean(논리형)
- undefined
- null
- array(배열)
- **object(객체)**
  - 함수와 속성이 함꼐 포함된 유형
  - 여러 자료를 중괄호({ })로 묶을 수 있다.
  - 키(Key)와 값(Value)을 콜론(:)을 사용하여 한 쌍으로 짝지어야 한다.
    ```javascript
    var kim = {
      firstName: "John",
      lastName: "Kim",
      age: 35,
      address: "Seoul",
    };
    ```

#### 자바스크립트는 미리 변수의 자료형을 지정하지 않는다.

#### 변수를 지정하여 값을 할당만 하면 된다.

#### 바로 이 방식을 '느슨한 자료형 체크(Weak Data Type Check)'라고 한다.

## 할당 연산자 응용하기

- +=
  - y = y+x
- -=
  - y = y-x
- \*=
  - y = y\*x
- /=
  - y = y/x
- %=
  - y = y%x
