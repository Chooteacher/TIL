# 01.isOkayToDrive

# Assignment

isOkayToDrive 함수를 작성

- 함수의 인자 who 가 "son"이면 "Nope!" 리턴
- 함수의 인자 who 가 "dad" 이면 "Good!" 리턴
- 함수의 인자 who 가 "grand father" 이면 "Be careful!" 리턴
- 나머지의 경우 "Who are you?" 리턴

```
function isOkayToDrive(who) {
  // 함수의 인자가 SON -> NOPE
  if (who == "son"){
    return "Nope!"
  // 함수의 인자가 DAD -> GOOD
  }  else if (who == "dad") {
    return "Good!"
  // 함수의 인자가 GRAND FATEHR -> BE CARFUL
  } else if (who == "grand father") {
    return "Be careful!"
  // who are you
  } else {
    return "Who are you?"
  }
}
isOkayToDrive("grand father");
```
