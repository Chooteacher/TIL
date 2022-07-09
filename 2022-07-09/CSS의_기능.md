# CSS의 기능

## 웹 페이지의 정보를 전달하는 HTML 본연의 목적을 충실히 수행할 수 있도록, 디자인에 대한 기능을 분리한 것이 CSS

- CSS를 활용하면 텍스트나 배경 화면의 크기, 색, 또는 레이아웃 배치 등 웹 페이지의 스타일을 바꿀 수 있음

<br>

# HTML에 CSS를 적용하는 법

## 1. Inline Style

- HTML 요소에 style 속성을 사용하여 같은 줄(inline)에 CSS를 작성하는 방법

```
<ul>
	<li><a href="index.html" style="color: red">Ghost Rain</a></li>
	<li><a href="shooting.html" style="color: red">Shooting Game</a></li>
</ul>
```

- > 링크(a태그)의 파란색을 빨간색으로 바꿈

- 태그의 style 속성을 활용하여 원하는 CSS 스타일을 직접 작성 가능
- style"..." 은 HTML 속성임, 값으로 반드시 CSS 효과가 들어온다고 약속 돼 있음
- HTML 태그에 바로 스타일을 작성하기 때문에 가장 직관적인 방법

## 1-2) Inline Style의 단점

- 하나의 태그에 여러 스타일을 적용할 경우 가독성이 떨어짐

```
<!-- 스타일 관련 코드가 너무 길어져 가독성이 떨어지는 코드 -->
<h1 style="color: red; font-size: 30px; background-color: yellow; font-weight: bold;">제목입니다</h1>
```

- 웹 구성요소를 설명하는 태그 정보와 스타일을 나타내는 정보가 함께 표현돼 구분하기 어려움
- 웹이 복잡해지고 코드가 많아질수록 요소의 스타일을 일일 수정하는 것은 거의 불가능

  <br>

## 2. CSS 파일 분리

- CSS 를 HTML 파일과 분리하여 .css 확장자의 파일에서 스타일 코드를 작성하는 방법

```
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8" />
    <title>Udemy - Ghost Rain</title>
  </head>
  <body>
		<h1>Ghost Rain</h1>
    <div id="bg">
      <span id="hero"></span>
    </div>
  </body>
</html>
```

- > index.html - 아직 CSS와 연결되지 않은 HTML 코드

```
h1 {
	color: red;
	background-color: yellow;
}
```

- > style.css - 준비해놓은 CSS 코드

- HTML과 CSS 코드는 각기 다른 파일에 작성되어 있음
- 아직 두 파일은 아무 관계가 없음

![s](./img/CSS_EX.png)

- > VS Code에서 각각 파일 만들기

- CSS를 적용하기 위해선 서로 관계없는 두 파일을 연결해야 함

- HTML 파일(.html) 과 CSS파일(.css) 은 `<link>` 태그를 사용해 연결 할 수 있음

```
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8" />
    <title>Udemy - Ghost Rain</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
		<h1>Ghost Rain</h1>
    <div id="bg">
      <span id="hero"></span>
    </div>
  </body>
</html>
```

- `<link>` - 웹 페이지가 어떤 파일과 연결되어 있는지 웹 브라우저에게 알림
- href - 연결하고자 하는 파일을 지정
- rel - 관계(relationship)를 뜻하며, 현재 문서와 연결한 아이템의 관계를 설명

<br>

## 2-2) 코드의 관리(유지보수) & 가독성

- CSS 관리의 발전 : Inline 스타일 -> `<style>` 태그의 활용 -> .css 파일 분리
- .css 파일을 분리하는 것은 하나의 파일이 아닌, 서로 다른 파일에 HTML과 CSS를 완벽히 분리하여 코드의 유지보수를 효율적으로 개선하며 가독성 또한 높이는 효과적인 방법

  - 웹 페이지 유지보수를 편리하게, 가독성 높게 코드를 작성하는것이 매우 중요
  - 웹 페이지가 복잡해지고 코드의 양이 많아질수록 더욱 중요

  <br>

## 3. `<style>` tag

- `<style>` 태그를 활용하여 CSS 코드를 따로 분리할 수 있음

```
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8" />
    <title>Udemy - Ghost Rain</title>

		<style>
			h1 {
				color: red;
				background-color: yellow;
			}

			a {
				color: red;
			}
		</style>
  </head>
  <body>
		<ul>
			<li><a href="index.html">Ghost Rain</a></li>
			<li><a href="shooting.html">Shooting Game</a></li>
		</ul>

		<h1>Ghost Rain</h1>
    <div id="bg">
      <span id="hero"></span>
    </div>
  </body>
</html>
```

- `<style>` 이라는 태그는 HTML의 문법이면서, 동시에 `<style>` 태그의 안쪽에 있는 내용은 CSS이므로 CSS 언어의 문법에 맞게 처리해야 한다는 의미를 지님

- Inline style 방식과 비교했을 때
  - Inline style - HTML 태그에 속성을 활용하여 HTML 문법에 맞게 그대로 스타일을 적용
  - `<style>` - CSS 라는 새로운 언어의 문법에 맞게 스타일을 적용

## 3-3) `<style>` 태그 방식의 장단점

### 장점

- HTML과 CSS의 분리
  - 디자인과 관련된 코드는 `<style>` 태그에 전부 포함시켜, 웹 페이지 정보를 전달하는 HTML과 스타일을 관리하는 CSS를 명확히 구분할 수 있음

 <br>

- 코드의 중복 제거

  - 이전에는 링크 태그의 스타일을 수정하기 위해 요소에 직접 일일이 코드를 수정해야 했음
    - 하지만 `<style>` 태그를 활용하면 a 태그 전체에 동일한 CSs 효과를 적용하여 효율적으로 코드를 관리할 수 있음
    - 즉, `<style>` 태그를 활용해 중복되는 코드를 단 하나의 코드로 만들어 '중복을 제거' 할 수 있음

    <br>

  - 웹 페이지가 커지고 복잡할수록, 코드의 중복을 제거하는것은 매우 중요
  - 코드의 중복을 제거하는 것은 웹 페이지를 유지하고 보수하는, 즉 유지보수를 편리하게 할 수 있으며, 코드의 가독성 또한 높아짐

<br>

### 단점

- 코드의 중복 제거
  - 스타일을 정의하는 코드가 길어진다면 아무리 HTML 코드와 CSS 코드가분리되어 있어도 한 눈에 파악하기 힘들어질 것임
  - 이는 코드의 유지보수를 힘들게 하며, 가독성을 떨어뜨릴 수 있음

```
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8" />
    <title>Udemy - Ghost Rain</title>

		<style>
			h1 {
				color: red;
				background-color: yellow;
			}

			a {
				color: red;
			}

			#bg {
			  position: relative;

			  width: 800px;
			  height: 500px;

			  background: url("./images/bg.png") no-repeat;
			  background-size: cover;

			  margin: 0 auto;
			}
		</style>
  </head>
  <body>
		<ul>
			<li><a href="index.html">Ghost Rain</a></li>
			<li><a href="shooting.html">Shooting Game</a></li>
		</ul>

		<h1>Ghost Rain</h1>
    <div id="bg">
      <span id="hero"></span>
    </div>
	</body>
</html>
```
