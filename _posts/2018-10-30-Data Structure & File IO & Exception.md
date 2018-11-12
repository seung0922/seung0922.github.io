---
layout: post
title:  "Data Structure & File IO & Exception"
date:   2018-10-30 10:01:13
categories: Data_science
---

# Data Structure & File IO & Exception.md

## 재귀함수
```
def factorial(a):
  if a == 1:
    return 1
  else:
    return a * factorial(a-1)
print factorial(3)
```
## Data structure
### List
- 순서대로 정리된 비정적 mutable 자료구조
- 초기화 할 때 [] 사용
```
shoplist = ['apple', 'mango', 'carrot', 'banana']
print 'I have', len(shoplist), 'items to purchase.'
```

### Tuple
- 여러 개의 객체를 모아 담는 정적 mutable 자료구조, 순서가 있음
- 초기화 할 때 () 사용
```
zoo = ('Python', 'elephant', 'penguin')
print 'Number of animals of in the zoo is, len(zoo)
```

### Dictionary
- 초기화에 {} 사용, key:value의 쌍으로 이루어짐

```
ab = {  'Swaroop'   : 'swaroop@swaroopch.com',
        'Larry'     : 'larry@wall.org',
        'Matsumoto' : 'matz@ruby-lang.org',
        'Spammer'   : 'spammer@hotmail.com',
    }

print "Swaroop's address is", ab['Swaroop']
```

### Stack
- 스택은 데이타 입/출력이 한쪽으로만 접근 할 수 있는 자료 구조이다. 
- 스택에서 가장 나중에 들어간 데이타가 제일 먼저 나오게 된다
- 그래서 스택을 LIFO(Last In First Out) 구조라고 한다.

<img src = 'http://cfs3.tistory.com/upload_control/download.blog?fhandle=YmxvZzEyNDIxQGZzMy50aXN0b3J5LmNvbTovYXR0YWNoLzAvOS5wbmc%3D'>

```
def main():
    stack = []            # stack create
    stack.append(1)  # same PUSH
    stack.append(2)
    stack.append(3)
    stack.append(4)
    print stack

    while stack:
       print "POP >", stack.pop()

if __name__ == '__main__':
    main()
```

### Queue
- 큐는 먼저 넣은 데이타가 먼저 나오는 FIFO(First-In-First-Out) 구조로 저장하는 자료구조 이다.
- 즉, 큐는 LIFO 구조인 스택과 반대되는 개념의 자료 구조이다. 
- 스택은 데이타가 입/출력하는 부분이 한 부분밖에 없다고 한다면, 큐는 양쪽 모두 뚤려있다.
<img src = 'http://cfs2.tistory.com/upload_control/download.blog?fhandle=YmxvZzEyNDIxQGZzMi50aXN0b3J5LmNvbTovYXR0YWNoLzAvMTcucG5n'>

```
def Main():
    queue = []           # queue create
    queue.append(1) # same PUT
    queue.append(2)
    queue.append(3)
    queue.append(4)
    print queue

    while queue:
        print "GET > ",queue.pop(0) # same GET

Main()
```

## 예외처리
### 예외(exception)란?
- 예외는 일반적으로 런타임 오류와 관련된 것으로서, 예방하기가 어렵거나 불가능한 것들이다. 더 이상 존재하지 않는 데이터베이스에 연결하려고 한다거나, 손상된 파일을 열려고 하거나, 오프라인 상태인 머신에 접속하려고 하는 경우 예외가 발생할 수 있다. 프로그래머나 사용자는 이러한 '예외적인' 경우에 대처하기가 어렵다.

### 오류 일부러 발생시키기
```
class NotAllowedUserName(Exception):
    def __str__(self):
        return "허용되지 않은 계정명입니다."

def register_nick(nick):
    # 비속어 닉네임
    if nick == '바보':
        raise NotAllowedUserName()
    # 음란한 닉네임
    elif nick == '19금':
        raise NotAllowedUserName()
    # 운영자 사칭
    elif nick == '운영자':
        raise NotAllowedUserName()
    else:
        print '계정이 생성되었습니다. 계정명은 {} 입니다.'.format(nick)

try:
#    register_nick('바보')
    register_nick('새로운 유저')
#    register_nick('19금')
except NotAllowedUserName as e:
    print e
```
