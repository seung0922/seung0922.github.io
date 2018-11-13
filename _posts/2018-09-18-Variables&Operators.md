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
	#### 숫자 바로 대입
	```
	"I eat %d apples." % 3
	```

	#### 문자열 바로 대입
	```
	print "I eat %s apples." % "five"
	```

	#### 숫자값을 나타내는 변수로 대입
	```
	number = 3
	print "I eat %d apples." % number
	```

	#### 2개 이상의 값 넣기
	```
	number = 3
	day = "three"
	print "I eat %d apples. So I was sick for %s days." % (number, day)
	```

## 변수 타입
#### 정수형 
- 말 그대로 정수 뜻하는 자료형
```
a = 120
b = 4
```

#### 실수형 
- 소수점이 포함된 숫자
```
a = 1.2
b = 4.24E10
```

## Type Casting
- C의 ++, --연산을 원하신다면 python에서는 +=1, -=1으로 고쳐 써야함

#### Operator의 종류 
 	* **, -, +, *, /, %, //, +=, >>, <<, &, ^, |, <=, <, >, >=, !=, ==
	

## 블로그 만들기
1. [사용자계정명].github.io로 repository 생성
2. 생성한 repository에서 setting으로 이동한 후, 스크롤을 내려서 github pages 섹션에서 활성화
3. change theme를 통해 원하는 테마 선택 후, 적용하면 적용된 화면을 볼 수 있음
4. 원하는 테마를 선택한 후, 저장소를 Fofk한 후, [github사용자명].github.com으로 이름 변경
5. 설정한 사이트로 이동하여 내용이 잘 표시되는지 확인
