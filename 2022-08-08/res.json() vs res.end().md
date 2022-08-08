# res.json() 과 res.end() 의 차이

## res.json()

```
app.get("/api/test", (req, res) => {
  res.send({ name: "Lee" });
});
```

- json이 아닌 것도 json 형식으로 바꾸어서 보내줌, 즉 content-type 헤더를 application/JSON으로 고정함
- res.json()은 내부적으로 res.send를 호출함
- res.json() 메서드는 JSON 타입의 데이터에 대해 형식을 추가적으로 설정할 수 있음

<br>

## res.end()

- 보내줄 데이터가 아무것도 없지만 response를 끝내고 싶을때 사용함

- 요청자에게 응답을 하고 나면, 세션을 종료하는 작업이 필요한데 이 역할을 하는것이 res.end()

- ex) 404를 리턴해주어야 할 때, 에러 페이지가 필요할 때

```
res.status(400).end();
```

<br>

# 결론

- res.json()을 쓰나 res.send()를 쓰나 응답을 종료해주는 역할을 하기때문에 굳이 res.end() 메서드를 명시적으로 호출할 필요가 없음

- data 처리 없이 빠르게 response를 끝낼땐 res.end(), data 처리가 필요하다면 res.json()을 사용

> response란 어떠한 작업을 요청한 곳에 무엇인가를 돌려주는 역할을 함!
