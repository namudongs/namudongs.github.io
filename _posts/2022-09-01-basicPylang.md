---
title:  "파이썬 기초"
excerpt: "파이썬 & 프로그래밍 소개"

categories:
  - python
tags:
  - [python]

toc: true
toc_sticky: true
share: false
related: false
 
date: 2022-09-01
last_modified_at: 2022-09-01

---

## :pushpin:프로그래밍 기초 

### 프로그래밍이란 ?
프로그래밍 언어 : C, C++, Java, Python, VB, Pascal, Ruby ...
영문 (인간) -> 컴파일러 -> 기계어 -> CPU -> 실행 -> 결과물

### 코딩 공부 하는 법
1. 디버깅 -> `내 의도`에 맞게 프로그램 실행 확인
2. 알고리즘, 자료구조 -> `코딩테스트` 필수
3. 다른 사람의 소스코드 참조 -> `Github` -> 오픈소스
4. 주석 -> 코드의 이해 증가
5. `자기가 만들고 싶은 프로그램`을 정확하게 정의

### 좋은 프로그램이란 ?
1. 코드의 가독성
2. 코드의 길이 -> 가독성과 연관
3. 변수의 이름
4. 중복 코드 최소화

### 파이썬의 장점
간결하고 쉽다
무료, `오픈소스의 강력함`, 빠른 개발 속도 (생산성)
협업 수월

### 파이썬의 활용 분야
GUI 프로그래밍 : pyQT
웹 프로그래밍 : flask, django ...
데이터분석, 머신러닝
IOT : 라즈베리파이 (초소형 미니PC)

## :pushpin:파이썬 기초 문법

### print 문
##### '', "", ''', """, 등의 부호로 기본 출력

```python
print('Python Start!')
# = Python Start!
print("Python Start!")
# = Python Start!
print("""Python Start!""")
# = Python Start!
print('''Python Start!''')
# = Python Start!
print()
# = 줄바꿈
```

##### separator 옵션 사용

```python
print('P', 'Y', 'T', 'H','O','N', sep='')
# = PYTHON
print('010', '7777', '7777', sep='-')
# = 010-7777-7777
print('python', 'google.com', sep='@')
# = python@google.com
```

##### end 옵션 사용

```python
print('Welcome To', end=' ')
print('IT News', end=' ')
print('Web Site')
# = Welcome To IT News Web Site
```

##### file 옵션 사용

```python
import sys

print('Learn Python', file=sys.stdout)
#전자의 내용을 후자의 파일에 저장
```

##### format 옵션 사용(d, s, f)`

d (digit) : 3

s (string) : 'python'

f (float) : 3.141519 ...


#### %s
```python
print('%s %s' % ('one', 'two'))
# = one two
print('{} {}' .format('one', 'two'))
# = one two
print('{} {}' .format('one', 2)) #.format 함수가 조금 더 유연함
# = one 2
print('{1} {0}' .format('one', 'two')) #index 번호가 0부터 시작하기에 순서가 바뀌어서 출력됨
# = two one

print('%10s' % ('nice')) #10개의 자릿수 중 문자열이 자리 차지
# =       nice
print('{:>10}' .format('nice')) #인위적으로 10자리의 문자열 확보
# =       nice

print('%-10s' % ('nice'))
# = nice
print('{:10}' .format('nice')) #반대의 경우로 10자리 확보하여 앞에서부터 출력
# = nice

print('{:_>10}' .format('nice')) #앞에 언더바 출력, 총 자릿수는 10개
# = ______nice
print('{:^10}' .format('nice')) #중앙 정렬
# = |   nice   |

print('%.5s' %('nice'))
# = nice
print('%.5s' %('pythonstudy')) #자릿수를 초과하면 지정 자릿수까지의 문자열만 출력
# = pytho
print('{:10.5}' %('pythonstudy')) #다른 방법
# = pytho
`````

#### %d
```python
print('%d %d' % (1,2))
# = 1 2
print('{} {}' .format(1,2))
# = 1 2

print('%4d' % (42))
# =  42
print('{:4d}' .format(42))
# =  42
`````

#### %f
```python
print('%f' % (3.1415192930230))
# = 3.141519
print('%06.2f' % (3.141592653589793)) #xx.yy x:정수부 자릿수 y=소수부 자릿수
# = 003.14 #총 6개의 자릿수 중에 정수부는 1개이기 때문에 0으로 채우고, 나머지 소수부 출력
print('{:06.2f}' .format(3.141592653589793))
# = 003.14 #동일하게 출력
```

문자열을 제외한 %d 정수, %f 소수는 신경써야 함
%f 소수의 경우 정수부, 소수부의 자릿수에 유의