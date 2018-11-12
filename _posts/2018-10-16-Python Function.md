---
layout: post
title: "Python Function"
date: 2018-10-16 4:20:00
categories: Data_science
---

# Python Function.md

## K-fold Test와 Overfitting 과적합
* Training / Test set / Validation set 을 나누어, 훈련, 테스트, 검증의 과정을 K회 진행하여 성능을 도출
  * Sample 분화: Training Set 모델 만들 때 사용 / Validating Set 모델 조정하기 위해 사용 Test Set 모델의 최종 평가 위해 사용
  * 충분한 교차검증을 거치지 않을경우, 훈련 데이터에만 최적화 되는 과적합Overfitting이 일어남 
<img src = 'http://www.cs.nthu.edu.tw/~shwu/courses/ml/labs/08_CV_Ensembling/fig-holdout.png'>

## Python Operation
* Type Casting
 * C의 ++, -- 연산을 원한다면 python에서는 +=1, -=1 으로 고쳐써야함

## Function
- 함수는 재사용 가능한 프로그램의 조각
- 특정 블록의 명령어 덩어리를 묶어 이름을 짓고, 그 이름을 프로그램 어디에서건 사용함으로써 그 블록에 포함된 명령어들을 몇 번이고 다시 실행할 수 있게 하는 것
- 이를 함수 호출이라 부른다

### 최대값 출력 함수
```
def print_max(x, y):
    """Prints the maximum of two numbers.

    The two values must be integers."""
    # convert to integers, if possible
    x = int(x)
    y = int(y)

    if x > y:
        print x, 'is maximum'
    else:
        print y, 'is maximum'

print_max(3, 5)
print_max(7, 9)
print print_max.__doc__
```

### 전역변수, 지역변수
```
x = 50

def func():
    global x

    print 'x is', x
    x = 2
    print 'Changed global x to', x

func()
print 'Value of x is', x


x = 50

def func(z=30):
    print 'x is', z
    z = z*2
    print 'Changed local x to', z

# func(x)
func(50)
func()
print 'x is still', x
```
