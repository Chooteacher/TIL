# 05. Finding a Remainder

자바스크립트 산술연산자에는 기본적인 덧셈(+), 뺄셈(-), 곱셈(\*), 나눗셈(/) 이외에 (%) 연산자가 있음

# Assignment

1. findRemainder 함수를 작성

- 함수 내부에 임의의 숫자 두 개를 넣어 리턴값이 1이 나와야 함
- % 연산자를 이용하면 짝수/홀수를 쉽게 구별 가능

```
function findRemainder(){
  let num = 7 /6
  return num
}
findRemainder();
```

2. 짝수인지 홀수인지 알 수 있게하는 함수 oddOrEven()를 작성

- oddOrEven() 함수는 한 개의 인자를 받음
- if 문과 % 연산자를 사용

```
function oddOrEven(num){

  if (num % 2 === 1 ){
    return "Odd"
  } else {
    return "Even"
  }
}
oddOrEven(50)
```
