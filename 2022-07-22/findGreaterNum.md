# 04.findGreaterNum

# Assignment

findGreaterNum 함수를 작성

- 두 숫자가 주어졌을 때 어느 숫자가 더 큰지의 여부에 따라 다른 메세지 값을 리턴
- 첫번째 숫자(num1)가 두번째 숫자(num2)보다 더 큰 경우 "First one is greater!" 리턴
- 두번째 숫자(num2)가 첫번째 숫자(num1)보다 더 큰 경우 "Second one is greater!" 리턴
- 첫번째 숫자(num1)와 두번째 숫자(num2)가 같은 경우 "Same!" 리턴

```
function findGreaterNum(num1, num2) {
  if (num1 > num2) {
    return "First one is greater!"
  } else if (num2 > num1) {
    return "Second one is greater!"
  } else if (num1 === num2) {
    return "Same!"
  }
}
findGreaterNum(4, 5)
```

> Second one is greater!
