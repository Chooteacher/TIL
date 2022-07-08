# HTML 의 기본문법

```<h1>Title</h1>
<h2>제목을 사용할 때 주로 hn태그를 사용합니다.</h2>
<hr />
<h3>글씨 크기가 모두 다르네요?</h3>
<ul>
  <li>HTML</li>
  <li>CSS</li>
  <li>JavaScript</li>
</ul>
```

- h1, h2, h3의 다른 점

  - h1 태그는 가장 큰 제목을 쓸 때
  - h2, h3 태그는 점점 작아짐

- ul 과 li 란?
  - ul : 순서가 필요없는 목록 만들기
  - li : ul 태그를 나열할 때 사용

<br>

- VS code에서 html 파일에 직접 입력해보고 싶다면 아래 코드를 사용

```<!DOCTYPE html>
<html lang="en">
  <head>
    <title>웹게임 만들기</title>
    <meta charset="UTF-8" />
  </head>
  <body>
		<h1>Title</h1>
		<h2>제목을 사용할 때 주로 hn태그를 사용합니다.</h2>
		<hr />
		<h3>글씨 크기가 모두 다르네요?</h3>
		<ul>
		  <li>HTML</li>
		  <li>CSS</li>
		  <li>JavaScript</li>
		</ul>
  </body>
</html>
```

- HTML 에서 DOCTYPE 이란?
- HTML 에서 Title 의 역할은?
- HTMl 에서 charset 과 UTF - 8 의 뜻?

  - `<!DOCTYPE html>` : 웹 문서의 시작을 알려주며 `<html>` 태그보다 먼저 선언,
    웹 문서가 어떤 버전의 HTML 언어로 작성 되었는지 웹 브라우저에게 전달
  - Title : 요소에 대한 조언 정보, 툴팁
  - `<meta charset="UTF-8"/>` : charset `<meta>` 태그의 charset 속성은 해당 HTML 문서의 문자 인코딩 방식을 명시
  - UTF-8 : 유니코드 전세계의 모든 문자를 표현할 수 있는 인코딩

  <br>

- 위의 코드 처럼 웹 페이지는 다양한 HTML 태그로 이루어져 있음
- HTML 기초개념(teg, content, attribute, element)의 형태
