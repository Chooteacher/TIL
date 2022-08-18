# import, export

- 리액트에서 다른 폴더의 파일을 불러오는 기능
- 다른 파일을 불러올 때 import를 사용
- 반대로 파일을 내보낼 때는 export를 사용

# 프로퍼티(props)

- 상위 컴포넌트가 하위 컴포넌트에 값을 전달할 때 사용(단방향 데이터 흐름)
- 수정할 수 없다는 특징이 있음
- 문자열을 전달할 때는 큰따옴표(" ")를, 문자열 외의 ㄱ밧을 전달할 때는 중괄호 { } 를 사용

# 컴포넌트

- 리액트로 만들어진 앱을 이루는 최소한의 단위
- 데이터(props)를 입력받아 View(state)상태에 따라 DOM Node를 출력하는 함수
- 이름은 항상 대문자로 시작

<br>

## 1) 함수형 컴포넌트

```
import React from 'react';

function MyComponent(props) {
	return <div>Hello, {props.name}</div>;
}

export default MyComponent; //다른 JS파일에서 불러올 수 있도록 내보내주기
```

- 가장 간단하게 컴포넌트를 정의하는 방법은 자바스크립트 함수를 작성하는 것
- 위의 export는 작성한 MyComponent 파일을 다른 파일에서 import 할 때 MyComponent로 불러올 수 있도록 정의하는 것

<br>

## 2) 클래스형 컴포넌트

```
import React from 'react';

class MyComponent extends React.Component {
	constructor(props) { // 컴포넌트 생성자 메서드, 컴포넌트를 만들 때 처음으로 실행
		super(props);
	}

	componentDidMount() { // 컴포넌트를 만들고, 첫 렌더링을 다 마친 후 실행
	}

	render() { // 상속받은 화면 출력 함수, 클래스형 컴포넌트는 render() 필수
		return <div>Hello, {this.props.name}</div>;
	}
}

export default MyComponent; //다른 JS파일에서 불러올 수 있도록 내보내주기
```

> componentDidMount() : 이벤트 등록, setTimeout, setInterval, 네트워크 요청 같은 비동기 작업을 처리

- 컴포넌트 구성 요소, 리액트 생명주기(라이프 사이클)를 모두 포함하고 있음
- 프로퍼티, state, 생명주기 함수가 필요한 구조의 컴포넌트를 만들 때 사용
