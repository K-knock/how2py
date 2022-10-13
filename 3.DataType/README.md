## ☝️ 들어가며

> 데이터 타입을 왜 공부할까?

<br >
프로그램의 값 처리 방식에 따라 보내주는 값의 데이터 타입을 맞춰줘야 합니다.

만약

<br >

데이터 타입을 구하기 위해선 `type()` 함수를 사용합니다.

문자열 연산 등에서 `type` 관련 에러가 많이 나기 때문에 `type()` 함수는 꼭꼭 외워두는게 좋습니다.

```python
print(type(1), type("Hello"))

> <class 'int'> <class 'str'>
```

## Numeric Type

> 파이썬의 숫자 타입을 알아보자

**`Int`**

기본적인 정수형입니다.

```python
print(type(32), type(-32), type(123123131311312312312))

> <class 'int'> <class 'int'> <class 'int'>
```

Q) 파이썬의 정수형 범위는 얼마일까요?

정답은 **무제한**입니다.

<br >
그 이유는 아래 링크 참조!

<br >

[python의 Int 자료형은 어떻게 범위가 무제한일까?](https://velog.io/@toezilla/1D1Q-001.-Python%EC%9D%98-int-%EC%9E%90%EB%A3%8C%ED%98%95%EC%9D%80-%EC%96%B4%EB%96%BB%EA%B2%8C-%EB%B2%94%EC%9C%84%EA%B0%80-%EB%AC%B4%EC%A0%9C%ED%95%9C%EC%9D%BC%EA%B9%8C)

그렇기 때문에 `integer overflow`도 나지 않고, 정수형도 `int` 하나만 존재한답니다. (python3 기준)

<br >

**`Float`**

기본적인 실수형입니다.

```python
print(type(3.14), type(3.0), type(-3.14))

> <class 'float'> <class 'float'> <class 'float'>
```

E-notation도 사용 가능합니다. (지수표기법)

```python
# e 왼쪽 숫자를 e 다음 숫자의 거듭제곱으로 10 곱셈
# 1e5 = 1x10^5
print(type(1e5), 1e5)

> <class 'float'> 100000.0
```

<br >

**`Complex`**

복소수입니다.

실수부와 허수부로 나누고, 허수부 앞에 `j` 혹은 `J`를 표기합니다.

```python
print(type(1+5j))

> <class 'complex'>
```

<br >

**`Type Conversion`**

파이썬은 한 `type`에서 다른 `type`으로 변환할 수 있습니다.

물론, `complex type`은 다른 `type`으로 변환이 불가능합니다.

```python
# Int to Float
print(type(float(1)), float(1))

> <class 'float'> 1.0

print(type(int(1.4)), int(1.4))

> <class 'int'> 1
```

## Text Type

> 파이썬의 문자열 타입을 알아보자

**`str`**

기본적인 문자열 타입으로, 작은 따옴표 혹은 큰 따옴표로 묶어줍니다.

```python
print(type("Hello"), 'Hello')

> <class 'str'> Hello
```

Q) 여러 줄을 입력하려면 어떻게 해야 할까요?

파이썬은 **들여쓰기**로 코드의 흐름을 판별한다는 것 기억하시나요?

따라서 아래 코드는 오류를 출력합니다.

```python
print("Hello
World!")

> SyntaxError: EOL while scanning string literal
```

방법은 2가지가 있습니다.

(1) line feed '\n'

```python
print("Hello\nWorld!")

> Hello
World!
```

(2) multiline Strings """ """

```python
print("""Hello
World!""")

> Hello
World!
```

두 번째 방식은 주석으로도 사용합니다. (변수에 할당하지 않으면 그냥 코드에 있는 문자열 그 자체이기 때문이죠)

```python
"""
print("이건 주석이랍니다!")
"""
print("Hello World!")

> Hello World!
```

## Sequence Types

> 파이썬의 리스트, 튜플의 정의와 차이점을 알아보자

**`List`**

C언어의 배열과 비슷합니다. `[]`로 감싸거나 `list()` 함수를 사용해서 만들 수 있습니다.

```python
fruit = ["apple", "banana", "cherry"]

print(type(fruit), fruit)

> <class 'list'> ['apple', 'banana', 'cherry']
```

```python
fruit = list(("apple", "banana", "cherry"))

print(type(fruit), fruit)

> <class 'list'> ['apple', 'banana', 'cherry']
```

<br >

list 내부에 값을 가져오기 위해선 `list_name[index]`를 사용합니다. (index는 0부터 입니다!)

```python
fruit = ["apple", "banana", "cherry"]

print(fruit[1])

> banana
```

<br >

list 안에는 **여러** `datatype`이 **혼합**해서 들어갈 수 있습니다.

```python
student = [202111445, "Younghun Kwon", True]

print(type(student[0]), type(student[1]))

> <class 'int'> <class 'str'>
```

<br >

`len()`함수로 list의 길이를 구할 수 있습니다.

```python
fruit = ["apple", "banana", "cherry"]

print(len(fruit))

> 3
```

## 딕셔너리

> 파이썬의 딕셔너리 그리고 해시 테이블을 알아보자

## 집합

> 파이썬의 집합을 알아보자

## 불

> 파이썬의 불 자료형을 알아보자

```

```

```

```
