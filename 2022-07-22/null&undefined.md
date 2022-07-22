# 05.null & nudefinde

null과 undefined 는 모두 자바스크립트의 데이터 타입임

undefinde는 선언은 됐지만 아직 value가 할당되지 않은 경우를 의미함.
null은 '빈 값(blank)'을 의미하는데 사용자가 준 value임. 그래서 undefined와 다르게 자바스크립트가자동적으로 null 이란 값을 줄 순 없음

포괄적인 의미로 '값이 없다'는 점에서 null과 undefined가 비슷한 것 같지만 둘은 엄격하게 같지 않음

```
let name; // undefined
let name = null; // null

console.log(null == undefined); // true
console.log(null === undefined); // false
```

엄격일치연산 (===)는 value뿐만 아니라 type도 같아야 true가 나옴  
null과 undefined의 type을 알아보기 위해 'typeof' 연산자를 사용해봄

```
console.log(typeof null); // object
console.log(typeof undefined); // undefined
```

null의 type이 object가 나옴.
null은 위에 설명한대로 '값이 없음(blank)' 을 의미하는 '할당된' value이기 때문
