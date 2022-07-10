# CSS 선택자 - 조합, 그룹, 가상

## 1) CSS 선택자 고급

### 1-1) 상속 (Inheritance)

- 스타일이 상속돼 자식에게도 같은 스타일이 적용 됨

```
<body>
	<p>블락요소</p>
	<span>인라인요소</span>
</body>
```

```
body {
  color: red;
  font-size: 14px;
}
```

- `<p>`,`<span>` 태그는 아무 스타일도 갖고 있지 않지만 부모인 body 태그에 영향을 받아 빨간색과 14px로 변경 됨

```
blockquote {
  color: black;
}
```

<br>

### 1-2) 그룹 (Grouping)

- 이 요소에, 저 요소 등등 여러 요소에 한번에 같은 스타일을 적용하고 싶음!

```
.what-is-blockquote, span {
  color: green;
}
```

- 각자의 선택자에 모두 똑같은 스타일을 적을 필요 없이 쉼표(,)로 선택자를 나열해서 한번에 지정할 수 있음

```
.what-is-blockquote {
	font-size: 12px;
  color: green;
}

span {
	font-size: 14px;
  color: green;
}
```

> 기존 코드

```
.what-is-blockquote, span {
  color: green;
}

.what-is-blockquote {
	font-size: 12px;
}

span {
	font-size: 14px;
}
```

> Grouping을 적용한 코드

- CSS 상으로 코드가 늘어나 더 복잡해 보일 수 있음

- 하지만 `green`색을 `blue`로 변경하려면 `.what-is-blockquote`와 `span`에서 각각 수정하지 않고, grouping 된 selector에서 한 번에 변경할 수 있어 유지보수가 편리함

<br>

### 1-3) 조합

- 부모 - 자식간의 관계는 한 칸 띄어쓰기가 필요함

```
<div class="pre">
  <span>이건 노란색 배경이고</span>
</div>

<div class="main">
  <span>이건 아님!</span>
</div>

<span class="pre">이것도 아님</span>

<div>
  <p class="pre">
    <span>이건 적용됩니다! 노란색배경!</span>
  </p>
</div>
```

```
.pre span {
  background-color: yellow;
}
```

- 위의 selector에서 최종적으로 적용되는 selector는 `<span>` 임

  - `<span>`이긴 `<span>`인데, `.pre` 하위에 있는 `<span>` 만 적용 됨
    - selector가 서로 붙어있지 않고 스페이스로 띄워 있다는 것을 주목!

- 하나의 요소에서 태그 + 클래스 + id로 조합할 때는 띄어 쓰지 않음

```
<p>빨간색이 적용됩니다.</p>
<p class="p-tag">회색이 적용됩니다.</p>
<p id="third-line">빨간색이고 밑줄이 적용됩니다.</p>
```

```
p {
	color: red;
}

p.p-tag {
 color: gray;
}

p#third-line {
 text-decoration: underline;
}
```

- p.p-tag는 `<p>` 태그이면서 p-tag 클래스임
- p#third-line는 `<p>`태그이면서 third-line 라는 id 이름을 가짐

 <br>

- > 아래는 어떤 뜻일까?

```
.a div .b .pre span {
 background-color: yellow;
}
```

- > 정답

```
<div class="a">
  <div>
    <header class="b">
      <h1 class="pre">
        <span>제목! 노란색 배경 나옴!</span>
        <span class="title">이것도 나옴!</span>
      </h1>
      <span>이건 적용안 됨</span>
    </header>
  </div>
  <span>이건 적용안 됨</span>
</div>
```

- `<span>` 태그에 적용되는 css임

- a클래스 밑에, div밑에, b클래스 밑에, pre클래스 밑에 span태그만 적용이 됨!

<br>

## 2) CSS 적용 우선순위

```
<p>폰트 크기는?</p>
<p class="p-tag">나는 p태그, class도 있다.</p>
```

```
p {
  font-size: 30px;
}

.p-tag {
  font-size: 15px;
}
```

- 두 번째 요소는 `<p>` 태그이자 .p-tag 로서 두개의 css에 영향을 받음, 하지만 중복된 font-size가 있음!
- 브라우저에선 30px과 15px중 어떤값을 적용할까?
- selector 표현마다 우선순위가 있음 (점수 계산으로 생각하면 좀 더 쉬움)
  - inline styling: 1000점
    - ex) `<p style="font-size: 30px;">inline styling으로 CSS 적용</p>`
  - id : 100점
  - class : 10점
  - tag : 1점

```
<p class="p-tag">나는 p태그, class도 있다.</p>
```

- `<p>` 태그에 적용된 30px은 1점
- .p-tag 클래스에 적용된 15px은 10점이므로 15px이 적용 된 것
- 만약 css에 아래가 추가된다면?

```
p.p-tag {
  font-size: 100px;
}
```

- 1점(p) + 10점(.p-tag) = 11점 이기 때문에 해당 요소는 100px이 적용될 것

- 점수 기억 하고 싶지 않다면?
  - tag << class <<<< id <<<<<< inline css
