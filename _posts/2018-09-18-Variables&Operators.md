---
layout: post
title:  "Variables & Operators"
date:   2018-09-18 10:01:13
categories: Data_science
---

# Variables & Operators.md

## Format string
<img src = 'https://t1.daumcdn.net/cfile/tistory/2522014854BFBC0125'></img>
* raw_input()
* 문자열 포맷 코드
	* 숫자 바로 대입
	```
	"I eat %d apples." % 3
	```

	* 문자열 바로 대입
	```
	print "I eat %s apples." % "five"
	```

	* 숫자값을 나타내는 변수로 대입
	```
	number = 3
	print "I eat %d apples." % number
	```

	* 2개 이상의 값 넣기
	```
	number = 3
	day = "three"
	print "I eat %d apples. So I was sick for %s days." % (number, day)
	```

## 변수 타입
* 정수형 - 말 그대로 정수 뜻하는 자료형
```
a = 120
b = 4
```

* 실수형 - 소수점이 포함된 숫자
```
a = 1.2
b = 4.24E10
```

## Type Casting
* C의 ++, --연산을 원하신다면 python에서는 +=1, -=1으로 고쳐 써야함

* Operator의 종류 
 	* **, -, +, *, /, %, //, +=, >>, <<, &, ^, |, <=, <, >, >=, !=, ==
