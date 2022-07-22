# [조건문] 2.checkAge

# Assignment

- cheackAge 함수를 작성
- 이름(name)과 나이(age)를 입력받는 checkAge라는 함수는 나이에 따라 다른 메세지를 리턴
- 만약 나이가 21살보다 적으면, "Go home, (name)!"
- 나이가 21살이거나 더 많으면, "Nice to meet you, (name)!"을 리턴

```
function checkAge(name, age) {
  if (age < 21){
     return "Go home, " + name + "!"
  }  else if (age => 21) {
    return "Nice to meet you, "+ name + "!"
  }
}
console.log(checkAge("은지", 28))
```
