# HTML의 부모태그와 자식태그

## 태그의 포함 관계, 부모 태그와 자식 태그

```
<parent>
	<child></child>
	<child></child>
</parent>
```

- `<parent>`와 `<child>` 라는 두 개의 태그가 있다고 가정
- 포함하고 있는 태그를 **부모 태그**, 포함된 태그 **자식 태그** 라고 함
- 참고! 탭(Tab) 키를 누르면 들여쓰기가 됨, 또는 스페이스(Space Bar)를 두 번 눌러도 됨

<br>

## 목차 구성하기

```
<ul>
	<li>Monday</li>
	<li>Tuesday</li>
	<li>Wednesday</li>
	<li>Thursday</li>
</ul>

<ol>
	<li>Friday</li>
	<li>Saturday</li>
	<li>Sunday</li>
</ol>
```

- `<ol>` : Ordered List
- `<ul>` : Unordered List
- `<li>` : List
  - `<li>` 태그는 어디서부터 어디까지가 연관된 항목일지 구분하기 위한 부모태그가 필요
  - `<li>` 태그는 반드시 부모 태그를 갖고있고, 부모 태그인 `<ul>` , `<ol>` 태그는 반드시 자식 태그를 갖고 있음
- 이처럼 복잡한 웹 페이지도 부모-자식 관계의 태그를 통해 구조화 시킬 수 있음

<br>

## 표(table) 구성하기

```
<table>
	<tr>
		<th>Name</th>
		<td>Yeri Kim</td>
	<tr/>
	<tr>
		<th>Position</th>
		<td>Frontend</td>
	</tr>
</table>
```

- 서로 포함 관계에 있는 태그

  - `<table>` : 테이블의 시작과 끝을 알리는 부모 태그
  - `<tr>` : 하나의 행(row)의 시작과 끝을 알리는 부모 태그
  - `<th>` : 헤더를 의미하는 자식 태그
  - `<td>` : 값을 표현할 때 사용하는 자식 태그

- 부모 태그, 자식 태그를 활용하여 웹 페이지의 구성을 쉽게 파악하고 코드의 가독성을 높일 수 있음
