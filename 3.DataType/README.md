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

그 이유는 아래 링크 참조!

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

## 문자열

> 파이썬의 문자열 타입을 알아보자

## 리스트, 튜플

> 파이썬의 리스트, 튜플의 정의와 차이점을 알아보자

## 딕셔너리

> 파이썬의 딕셔너리 그리고 해시 테이블을 알아보자

## 집합

> 파이썬의 집합을 알아보자

## 불

> 파이썬의 불 자료형을 알아보자
