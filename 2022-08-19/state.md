# state
```
import './App.css'
import React, {useState} from 'react';

export default function App() {
  let count = 0
  const [count2, setCount2] = useState(0)
  const increase = () => {
    count = count +1
    console.log("count = " + count)
  }
  return (
    <main>
      <div>{count}</div>
     <button onClick={increase}>증가해용!증가해용!</button>
    </main>
  )
}

```
> 전체 코드


```
import React, {useState} from 'react';

const [count2, setCount2] = useState(0)
```

- useState라는 함수를 react에서 가져옴
- useState라는 함수는 [] 배열(Array)을 반환함
- 현재 배열엔 [count2 , setCount2]가 담겨있음
- 초기값을 담고있는 state변수(count2) 와 state의 값을 업데이트 해주는 함수(setCount2)
- useState() 에 들어가는 매개변수는 초기값임!
- state가 바뀌면 UI가 자동으로 업데이트 됨
- state는 함수가 다 끝나고 실행 , 그 후 UI 업데이트를 함 (비동기적인 함수)