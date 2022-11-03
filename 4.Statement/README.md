## 👨‍💻 들어가며

<br>

## 👩‍💼 IF 조건문

**Syntax**
```python
>>> if <conditional expression>:
...     <code1>
... else : 
...     <code2>
```
(1) 꼭 들여쓰기를 해야합니다.
(2) if 조건문 뒤에 ':'을 꼭 붙여야 합니다.
<br>

**Examples**

<br>

(1) 여러 논리연산자를 사용할 수 있습니다.

```python
>>> a = 10
>>> if a == 10:
...    print("a는 10 입니다.")
...

> a는 10 입니다.

```

```python
>>> a = 5
>>> if a <= 8:
...     print('a는 8보다 작습니다.')
...

> a는 8보다 작습니다.
```

```python
>>> a = 1
>>> if a != 1:
...     print('a는 1이 아닙니다.')
...

>
```

<br>

(2)중첩하여 사용할 수 있습니다.

```python
>>> a = 21
>>> if a >= 10:
...     print('a는 10보다 큽니다.')
...
...     if a >= 20:
...         print('a는 20보다 큽니다.')
...
...         if a > 30:
...             print('a는 30보다 큽니다.')

> a는 10보다 큽니다.
> a는 20보다 큽니다.
```
<br>

(3) else를 이용하여 분기를 표현할 수 있습니다.

```python
>>> a = 50
>>> if a == 40:
...     print('a는 40입니다.')
... else
...     print('a는 50입니다.')
```
<br>

(4) 변수에 값을 대입할 때 간단하게 나타낼 수 있습니다.

```python
>>> a = 5
>>> if a == 8:
...     b = a
... else 
...     b = 0
...
>>> print(b)

> 0
```

```python
>>> a = 3
>>> b = a if a == 2 else 0
>>> print(b)

> 0
```