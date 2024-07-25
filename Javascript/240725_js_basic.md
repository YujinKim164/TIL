## 자바스크립트 소스 작성하고 실행하기

1. HTML 문서 안에 자바스크립트 소스 작성하기<br>

   - \<script> 태그는 HTML 문서 **어디에든** 사용 가능<br>
   - \<script> 태그는 한 문서 안에서 **여러 개** 사용 가능<br>
   - \<script> 태그가 **삽입된 위치**에서 소스 실행<br>

   보통 \<script> 태그는 주로 HTML 문서 내용이 끝나는 \</body> 태그 앞에 삽입한다.

2. 외부 스크립트 파일 연결하기<br>

   1. 같은 디렉토리 내에서 html 파일에서 \<script> 태그에 들어있던 코드를 js 파일에 작성한다.
   2. html 문서의 \</body> 태그 바로 앞에 아래와 같이 src 속성을 작성함으로써 외부 자바스크립트 파일을 연결한다.

   ```html
   <script src="js/change.js"></script>
   ```

## 자바스크립트 프로그램의 실행 프로세스

웹 브라우저에는 **HTML 분석기(HTML Parser)**, **CSS 분석기(CSS Parser)**, **자바스크립트 해석기(Javascript Interpreter)**가 포함되어 있다.

```html
<!DOCTYPE html>
<html lang="ko">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <title>Welcome</title>
    <style>
      ...;
    </style>
  </head>
  <body>
    <h1>어서오세요</h1>
    <script>
      ...
    </script>
  </body>
</html>
```

- \<!DOCTYPE html>은 HTML 문서의 시작을 알리는 HTML 태그. 크롬 브라우저는 이 태그를 보고 작성한 소스가 HTML문서라는 사실을 알게 된다. 따라서 \<html> 태그 사이의 내용을 HTML 분석기로 HTML5 표준에 맞춰 해석하기 시작

- HTML 분석기는 주로 HTML 태그의 순서와 포함 관계를 확인한다. 즉 HTML 분석기를 통해 크롬 브라우저의 \<head> 태그 안에는 3개의 \<meta> 태그와 \<title>, \<style> 태그가 있고 \<body> 태그 안에는 \<h1>, \<script> 태그가 있다는 것을 알게 된다.

- CSS 분석기는 HTML 분석기가 태그 분석을 끝낸 다음 \<style> 태그 사이의 스타일 정보를 분석한다.

- 마지막으로, 자바스크립트 해석기가 \<script> 태그 사이의 자바스크립트 소스를 해석한다.

## 자바스크립트의 입력과 출력

#### 사용자 입력값 받기 - prompt( ) 함수

- 사용자가 값을 입력할 수 있도록 작은 창을 만들어 준다.
- 소괄호 안에 큰따옴표나 작은따옴표로 원하는 문장을 감싸 넣으면 프롬프트 창에 문장 표시 가능
- 아래와 같이 입력하면 프롬프트 창의 텍스트 필드 안에 기본 값(KYJ)을 표시할 수 있다.

  ```javascript
  prompt("이름을 입력하세요", "KYJ");
  ```

#### 알림 창으로 출력하기 - aleart( )함수

- 소괄호 안에 원하는 내용을 큰따옴표나 작은따옴표로 감싸 준다.

  ```javascript
  alert("환영합니다!");
  ```

#### 웹 브라우저 화면에 출력하기 - document.write( )함수

- 괄호 안의 내용을 크롬 브라우저 화면에 출력하는 용도로 사용한다.

  ```javascript
  var name = prompt("이름을 입력하세요.");
  document.write(name + "님, 어서오세요!");
  ```

#### 콘솔에 출력하기 - console.log( ) 함수

- 괄호 안의ㅣ 내용을 콘솔 창에 출력한다.
  ```javascript
  var name = prompt("이름을 입력하세요.");
  console.log(name + "님, 어서오세요!");
  ```

## 자바스크립트 소스 작성 시 규칙

1. 대소문자 구별하기
2. 읽기 쉽게 들여 쓰기
3. 세미콜론으로 문장 구분하기
4. 주석
   1. 한 줄 주석 **//**
   ```javascript
   var today = new Date(); // 날짜를 가져온다.
   var h = today.getHours(); // 시를 추출한다.
   ```
   2. 여러 줄 주석 **/\* ... \*/**
   ```javascript
   /*
    현재 날짜를 가져와
    시와 분, 초로 추출하고
    화면에 표시하는 스크립트
    */
    function startTime(){...}
   ```
5. 식별자는 정해진 규칙을 지켜 작성하기

   1. 영문자로 시작
   2. 밑줄(\_)로 시작
   3. 두 단어로 만들 경우 camelCase 사용

6. 예약어는 식별자로 사용 불가능

[출처] Do it! 웹 프로그래밍을 자바스크립트 기본편
