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
** 꼭 들여쓰기를 해야합니다.
<br>
** if 조건문 뒤에 ':'을 꼭 붙여야 합니다.
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
>>> if 3 <= a <= 8:
...     print('a는 3보다 크고 8보다 작습니다.')
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

```python
>>> a = 1
>>> b = 2
>>> if a == 1 and b == 2:
...     print('TRUE')
...
> TRUE
```
** &&,||,! 대신에 and, or, not 을 씁니다.

<br>

(2)중첩하여 사용할 수 있습니다.

```python
>>> a = 21
>>> if 20 >a > 10:
...     print('a는 10보다 큽니다.')
...
...     if 30> a > 20:
...         print('a는 20보다 큽니다.')
...
...         if a > 30:
...             print('a는 30보다 큽니다.')

> a는 10보다 큽니다.
> a는 20보다 큽니다.
```
<br>

(3) else와 elif를 이용하여 분기를 표현할 수 있습니다.

```python
>>> a = 50
>>> if a == 40:
...     print('a는 40입니다.')
... elif a == 30:
...     print('a는 30입니다.')
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

(5) 참 거짓을 표현하는 여러가지 방법이 있습니다.
<br>

| TRUE  | FALSE |     Explain     |
|-------|-------|-----------------|
|   1   |   0   |  _0제외 모두 참_  |
|  TRUE | FALSE |              |
|       | NONE  | _NONE은 거짓_  |  
| 'HI'  |   ''  | _빈 문자열은 거짓_|
| 0xF1  |       |_실수 16진수,2진수 모두 참_|
|_not 1_|_not 0_|_not으로 참거짓 전환_|
