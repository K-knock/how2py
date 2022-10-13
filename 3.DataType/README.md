## ☝️ 들어가며

> 데이터 타입을 왜 공부할까?

프로그램의 값 처리 방식에 따라 보내주는 값의 데이터 타입을 맞춰줘야 합니다.

<br >

데이터 타입을 구하기 위해선 `type()` 함수를 사용합니다.

문자열 연산 등에서 `type` 관련 에러가 많이 나기 때문에 `type()` 함수는 꼭꼭 외워두는게 좋습니다.

```python
print(type(1), type("Hello"))

> <class 'int'> <class 'str'>
```

```python
# 서로 다른 타입을 + 할 경우 오류가 납니다.
print(1+"Hello")

> TypeError: unsupported operand type(s) for +: 'int' and 'str'
```

## Numeric Type

> 파이썬의 숫자 타입을 알아보자

### Int

기본적인 정수형입니다.

```python
print(type(32), type(-32), type(123123131311312312312))

> <class 'int'> <class 'int'> <class 'int'>
```

_Q) 파이썬의 정수형 범위는 얼마일까요?_

정답은 **무제한**입니다.

<br >
그 이유는 아래 링크 참조!

<br >

[python의 Int 자료형은 어떻게 범위가 무제한일까?](https://velog.io/@toezilla/1D1Q-001.-Python%EC%9D%98-int-%EC%9E%90%EB%A3%8C%ED%98%95%EC%9D%80-%EC%96%B4%EB%96%BB%EA%B2%8C-%EB%B2%94%EC%9C%84%EA%B0%80-%EB%AC%B4%EC%A0%9C%ED%95%9C%EC%9D%BC%EA%B9%8C)

그렇기 때문에 `integer overflow`도 나지 않고, 정수형도 `int` 하나만 존재한답니다. (python3 기준)

### Float

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

### Complex

복소수입니다.

실수부와 허수부로 나누고, 허수부 앞에 `j` 혹은 `J`를 표기합니다.

```python
print(type(1+5j))

> <class 'complex'>
```

### Type Conversion

파이썬은 한 `type`에서 다른 `type`으로 변환할 수 있습니다.

물론, `complex type`은 다른 `type`으로 변환이 불가능합니다.

```python
# Int to Float
print(type(float(1)), float(1))

> <class 'float'> 1.0

# Float to Int
print(type(int(1.4)), int(1.4))

> <class 'int'> 1
```

## Text Type

> 파이썬의 문자열 타입을 알아보자

### Str

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

<br >

방법은 2가지가 있습니다.

(1) line feed `\n`

```python
print("Hello\nWorld!")

> Hello
World!
```

(2) multiline Strings `""" """`

```python
print("""Hello
World!""")

> Hello
World!
```

<br >

두 번째 방식은 주석으로도 사용합니다. (변수에 할당하지 않으면 그냥 **코드에 있는 문자열 그 자체** 이기 때문이죠)

```python
"""
print("이건 주석이랍니다!")
"""
print("Hello World!")

> Hello World!
```

## Sequence Type

> 파이썬의 리스트, 튜플의 정의와 차이점을 알아보자

### List

C언어의 배열과 비슷합니다. **`list`는 python의 핵심 기능 중 하나라고 해도 과언이 아닐만큼 많이 사용**되기 때문에 꼭 숙지하시는 것을 추천드립니다.

`[]`로 감싸거나 `list()` 함수를 사용해서 만들 수 있습니다.

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

`list` 내부 값을 가져오기 위해선 `list_name[index]`를 사용합니다. (index는 0부터 입니다!)

```python
fruit = ["apple", "banana", "cherry"]

print(fruit[1])

> banana
```

<br >

`list` 안에는 **여러** `datatype`이 **혼합**해서 들어갈 수 있습니다.

```python
student = [202111445, "Younghun Kwon", True]

print(type(student[0]), type(student[1]))

> <class 'int'> <class 'str'>
```

<br >

`len()` 함수로 `list`의 길이를 구할 수 있습니다.

```python
fruit = ["apple", "banana", "cherry"]

print(len(fruit))

> 3
```

<br >

`append()` 메서드로 `list`에 값을 추가할 수 있습니다.

```python
fruit = ["apple", "banana", "cherry"]
fruit.append("melon")

print(fruit)

> ['apple', 'banana', 'cherry', 'melon']
```

<br >

`remove()` 메서드로 `list` 안의 값을 제거할 수 있습니다.

```python
fruit = ["apple", "banana", "cherry"]
fruit.remove("banana")

print(fruit)

> ['apple', 'cherry']
```

<br >

`sort()` 메소드로 `list` 안의 내용을 정렬할 수 있습니다.

**_syntax_**

```python
list.sort(key=..., reverse=...)
```

**_parameter_**

| Parameter | Description                                                    | Default |
| --------- | -------------------------------------------------------------- | ------- |
| _key_     | _정렬을 목적으로 하는 함수를 값으로 넣으며, key 기준으로 정렬_ |         |
| _reverse_ | _False일 경우 오름차순 정렬_                                   | _False_ |

<br >

```python
number = [9, 123, 32, 15, 36, 42]
number.sort()

print(number)

> [9, 15, 32, 36, 42, 123]
```

```python
number = [9, 123, 32, 15, 36, 42]
number.sort(reverse=True)

print(number)

> [123, 42, 36, 32, 15, 9]
```

<br>

`copy()` 메서드로 `list`를 복사할 수 있습니다.

```python
number = [1, 2, 3]
numberCopy = number.copy()

print(numberCopy)

> [1, 2, 3]
```

_Q) 그냥 대입 연산자(=)를 사용하면 안되나요?_

<br >

대입 연산자와 `copy()` 메서드는 작동 방식이 다릅니다.

아래 코드를 참고해보세요.

```python
number = [1, 2, 3]

# 대입
numberEqual = number

# copy()
numberCopy = number.copy()

# 원본 list인 number를 수정한다면?
number.append(4)

print(numberEqual, numberCopy)

> [1, 2, 3, 4] [1, 2, 3]
```

차이점을 찾으셨나요?

<br >

대입 연산자는 **원본 list를 변경하면 같이 변경**되는 반면

`copy()` 메서드는 **바뀌지 않습니다**.

### Tuple

`list`와 매우 유사하지만, `tuple` 내의 값은 **수정 불가능**하다는 특징이 있습니다.

`()`로 감싸거나 `tuple()` 함수를 사용해서 만들 수 있습니다.

```python
fruit = ("apple", "banana", "cherry")

print(type(fruit), fruit)

> <class 'tuple'> ('apple', 'banana', 'cherry')
```

```python
fruit = tuple(("apple", "banana", "cherry"))

print(type(fruit), fruit)

> <class 'tuple'> ('apple', 'banana', 'cherry')
```

<br >

`tuple` 내부 값을 가져오기 위해선 `tuple_name[index]`를 사용합니다. (index는 마찬가지로 0부터 입니다!)

```python
fruit = ("apple", "banana", "cherry")

print(fruit[1])

> banana
```

<br >

`tuple` 안에는 여러 `datatype`이 **혼합**해서 들어갈 수 있습니다.

```python
student = (202111445, "Younghun Kwon", True)

print(type(student[0]), type(student[1]))

> <class 'int'> <class 'str'>
```

<br >

`len()` 함수로 `tuple`의 길이를 구할 수 있습니다.

```python
fruit = ("apple", "banana", "cherry")

print(len(fruit))

> 3
```

## Mapping Type

> 파이썬의 딕셔너리를 알아보자

### Dictionary

파이썬의 `dictionary`는 `키:값` 형식으로 데이터를 저장합니다.

`{}` 안에 `키:값` 형식으로 저장하며, 각 값은 `,`로 구분합니다.

```python
student = {"number":202111445, "name":"Younghun Kwon"}

print(type(student), student)

> <class 'dict'> {'number': 202111445, 'name': 'Younghun Kwon'}
```

<br >

혹은 `dict(key=vaule)` 함수를 사용해서 만들 수 있습니다.

```python
student = dict(number=202111445, name="Younghun Kwon")

print(type(student), student)

> <class 'dict'> {'number': 202111445, 'name': 'Younghun Kwon'}
```

이 때는 key 값을 따옴표로 묶지 않아야 합니다. (자동으로 문자열로 변경됩니다.)

```python
# key를 따옴표로 묶을 경우 오류가 발생합니다.
student = dict("number"=202111445, "name"="Younghun Kwon")

> SyntaxError: expression cannot contain assignment
```

<br >

`key`와 `value`는 둘 다 `datatype`을 **혼합**해서 사용할 수 있습니다.

`key`의 경우 `list`와 `dictionary`를 사용할 수 없으며, `value`는 모든 `datatype`을 사용할 수 있습니다.

```python
information = {10: "ten", True: [1, 2, 3]}

print(information)

> {10: 'ten', True: [1, 2, 3]}
```

<br >

`dictionary` 내부 값을 가져오기 위해선 `dict_name[key]`를 사용합니다.

```python
student = {"number":202111445, "name":"Younghun Kwon"}


print(student["number"])

> 202111445
```

<br >

`key`에 `value`를 할당할 수 있습니다. 만약 `key`가 존재하지 않았다면, 해당 `key`를 추가하고 `value`를 할당합니다.

```python
student = {"number":202111445, "name":"Younghun Kwon"}

# 존재하는 key에 할당
student["number"] = 222222222

# 존재하지 않는 key에 할당
student["height"] = 187

print(student)

> {'number': 222222222, 'name': 'Younghun Kwon', 'height': 187}
```

<br >

_Q) `key` 이름이 중복되면 어떻게 될까요?_

아래처럼 오류가 발생하게 됩니다.

`key`는 **중복이 안된다**는 것!

```python
student = dict(number=202111445, number=222222222)

> keyword argument repeated: number
```

```python
# 만약 아래 방식을 사용한다면, 오류 대신 마지막 할당 값이 적용됩니다.
student = {"number":202111445, "number":222222222}

print(student["number"])

> 222222222
```

<br >

`len()` 함수를 사용해 `dictionary`의 길이를 구할 수 있습니다.

```python
student = dict("number"=202111445, "name"="Younghun Kwon")

print(len(student))

> 2
```

## Set Type

> 파이썬의 집합을 알아보자

### Set

수학의 집합과 비슷하며, 순서가 없고 집합 안에서는 중복 값이 없습니다.

`set`은 `{}` 를 사용해 생성합니다.

```python
# 단, {} 자체는 dict과 겹치므로 주의해서 사용해야 합니다.
# dict는 키:값인 반면 set은 값만 존재하는 차이점이 있습니다.
number = {1, 2, 3, 4, 5}

print(type(number), number)

> <class 'set'> {1, 2, 3, 4, 5}
```

```python
# 그냥 중괄호만 선언할 경우 dict으로 인식합니다.
number = {}

print(type(number))

> <class 'dict'>
```

혹은 `set()` 함수를 사용해 생성할 수도 있습니다.

```python
number = set([1, 2, 3, 4, 5])

print(type(number), number)

> <class 'set'> {1, 2, 3, 4, 5}
```

<br >

**중복된 값을 제거한다는 성질**을 이용해 값을 정리하기도 합니다.

```python
number = [1, 2, 3, 3, 5, 5, 6]

print(set(number))

> {1, 2, 3, 5, 6}
```

<br >

`add()` 메소드로 값을 추가할 수 있습니다.

```python
number = {1, 2, 3, 4}
number.add(5)

print(number)

> {1, 2, 3, 4, 5}
```

<br >

`remove()` 메소드로 값을 제거할 수 있습니다.

만약 해당하는 값이 없다면 오류를 출력합니다.

```python
number = {1, 2, 3, 4, 5}
number.remove(5)

print(number)

> {1, 2, 3, 4}
```

```python
number = {1, 2, 3, 4, 5}
number.remove(6)

> KeyError: 6
```

<br >

`discard()` 메소드를 통해서도 값을 제거할 수 있습니다.

이 메소드의 경우 해당하는 값이 없어도 오류가 나지 않습니다.

```python
number = {1, 2, 3, 4, 5}
number.discard(6)

print(number)

> {1, 2, 3, 4, 5}
```

<br >

추가적으로 **집합의 연산**도 가능하지만, 일단 넘어가겠습니다.

궁금하다면 아래 링크에서 공부해보는 것도 도움될 것 같습니다.

[python-set(집합)](https://wikidocs.net/16044)

## Boolean Type

> 파이썬의 불 자료형을 알아보자

## Binary Type

> 파이썬의 바이너리 타입을 알아보자

**`bytes`**

1바이트 단위의 값을 연속적으로 저장하는 자료형

```

```

```

```
