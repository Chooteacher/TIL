# HTML과 JavaScript의 만남

## JavaScript 실행 조건

- 브라우저가 존재해야 함
- HTML 파일이 있어야 함
- HTML 코드와 JavaScript 코드를 연결시켜야 함

## JAvaScript 적용 방법

- HTML 파일 내부에서 `<script>` 태그를 사용하는 방법
- JavaScript 파일을 분리해 HTML 파일과 연결하는 방법

### 1. `<script>` tag

- `<script>` 태그 내에 Javascript 코드를 작성할 수 있음. 단 HTML 코드는 작성 불가능
- HTML 파일에 `<script> ... </script>` 안에 작성ㅅ된 코드는 브라우저가 자바스크립트 코드로 인식하게 됨

> HTML 내부 JavaScript 코드의 위치

```
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8" />
    <title>JavaScript</title>
  </head>
  <body>
    <h1>JavaScript</h1>
    <script>
      alert("Hello JavaScript!");
    </script>
  </body>
</html>
```

### 1-1) `<script>` 태그 방식의 문제점

- `<script>` 태그를 활용해 HTML과 JavaScript 코드를 명확히 분리할 수 있음. 하지만, 동적인 기능을 정의하는 JavaScript 코드가 길어진다면 아무리 HTML코드와 JavaScript 코드가 분리돼 있어도 한 눈에 파악하기 힘들어질 것
- 이는 코드의 유지보수를 힘들게 하며, 가독성을 떨어뜨림

```
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8" />
    <title>JavaScript</title>
  </head>
  <body>
    <h1>JavaScript</h1>
    <div class="login_box">
			<input id="id" type="text" placeholder="ID를 입력해주세요" />
			<input id="password" type="text" placeholder="PW를 입력해주세요" />
			<button id="button" type="button">Login</button>
		<div>
    <script>
      const loginBtn = document.getElementById('button');

      loginBtn.addEventListener('click', function() {
        const id = document.getElementById('id').value;
        const password = document.getElementById('password').value;

        if (!id) {
          alert('아이디를 입력해주세요!');
          return;
        } else if (!password) {
          alert('비밀번호를 입력해주세요!');
          return;
        } else {
          alert('로그인 성공!');
        }
      });
    </script>
  </body>
</html>
```

<br>

### 2. JavaScript 파일 분리

- JavaScript 코드를 HTML 파일과 분리해 .js 확장자의 파일에서 코드를 작성하는 방법
- HTML 파일(.html)과 JavaScript 파일(.js)은 `<script>` 태그를 사용해 연결 할 수있음
- `<script>` 태그의 src 속성을 사용해 특정 자바스크립트 파일을 연결

```
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8" />
    <title>JavaScript</title>
  </head>
  <body>
    <h1>JavaScript</h1>
    <div class="login_box">
			<input id="id" type="text" placeholder="ID를 입력해주세요" />
			<input id="password" type="text" placeholder="PW를 입력해주세요" />
			<button class="button" type="button">Login</button>
		<div>

		<script src="index.js"></script>
  </body>
</html>
```

```
const loginBtn = document.getElementsByClassName("button")[0];

loginBtn.addEventListener("click", function () {
  const id = document.getElementById("id").value;
  const password = document.getElementById("password").value;

  if (!id) {
    alert("아이디를 입력해주세요!");
    return;
  } else if (!password) {
    alert("비밀번호를 입력해주세요!");
    return;
  } else {
    alert("로그인 성공!");
  }
});
```

<br>

### 코드의 관리 (유지보수) & 가독성

- `<script>` 태그를 활용해 HTML 파일 내부에 JavaScript 코드 작성 -> .js 파일 분리
- 웹 페이지 유지보수를 편리하게, 가독성 높게 코드를 작성하는것은 중요
- 웹 페이지가 복잡해지고 코드의 양이 많아질수록 더욱 중요
- .js 파일을 분리하는 것은 하나의 파일이 아닌 서로 다른 파일에 HTML과 JavaScript를 완벽히 분리해 코드의 유지보수를 효율적으로 개선하며 가독성을 높이는 효과적인 방법임
