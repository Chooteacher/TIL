# 02. whichGrade

# Assignment

whichGrade 함수를 작성

- 점수가 주어졌을때 주어진 점수에 따라 서로 다른 등급을 문자열로 반환
- (100 이하 ~ 90 이상) --> 'A'
- (89 이하 ~ 80 이상) --> 'B'
- (79 이하 ~ 70 이상) --> 'C'
- (69 이하 ~ 60 이상) --> 'D'
- (59 이하 ~ 0 이상) --> 'F'
- 점수가 100을 초과하거나 0 미만인 경우 --> 'INVALID SCORE'

```
function whichGrade(score) {
  if (score >= 90 && score <= 100) {
    return 'A'
  } else if ( score >= 80 && score <= 89) {
    return 'B'
    } else if ( score >= 70 && score <= 79) {
    return 'C'
    } else if ( score >= 60 && score <= 69) {
    return 'D'
    } else if ( score >= 0 && score <= 59) {
    return 'F'
    } else if ( score >= 100 || score <= 0) {
    return 'INVALID SCORE'
    }
  }

```
