# isEitherEvenAndLessThan9

# Assignment

isEitherEvenAndLessThan9 함수를 작성하세요.

- 함수의 인자로 숫자 두개가 주어졌을때 함수는 2가지 조건을 검사
- 우선 두 숫자 중 적어도 하나가 짝수인지 확인
- 그리고 두 숫자 모두 9보다 작은지를 확인
- 두 조건을 모두 만족하는 경우만 true를 반환

```
function isEitherEvenAndLessThan9(num1, num2) {
  if ((num1 %2 === 0 || num2 %2 === 0) && (num1 < 9) && (num2 < 9)) {
       return true
  } else {
    return false
  }
}
console.log(isEitherEvenAndLessThan9(4,12))
```
