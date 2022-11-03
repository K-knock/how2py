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
** &&,||,! 대신에 and, or, not 을 사용합니다.

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
|  True | False |              |
|       | NONE  | _NONE은 거짓_  |  
| 'HI'  |   ''  | _빈 문자열은 거짓_|
| 0xF1  |       |_실수 16진수,2진수 모두 참_|
|_not 0_|_not 1_|_not으로 참거짓 전환_|



## 👩‍🏭While 반복문

**Syntax**

```python
>>> while <conditional expression>:
...     <code1>
...     <code2>
...     <change expression>
``` 
**if문과 같이 들여쓰기와 ':'는 필수입니다.

<br>

**Examples**
<br>
(1) 기본적인 반복문
<br>
c언어와 매우 유사하다.

```python
>>> i = 0
>>> while i < 5:
...     print(f"Hello World, {i}")
...     i+=1
...

>Hello World, 0
>Hello World, 1
>Hello World, 2
>Hello World, 3
>Hello World, 4
```
*파이썬에는 증감연산자가 존재하지 않는다.*
<br>
(2) 참 거짓 구분은 if와 동일합니다.

```python
>>> while True:
...     print("It's True!")
...

> It's True!
> It's True!
> It's True!
/////
```

(3) break, continue<br>
c언어와 동일하게 사용 가능합니다.<br>
3.1) break

```python
>>> a = 1
>>> while True:
...     print(a)
...     a += 1
...     if a == 3:
...         break
...

> 1
> 2
```

3.2) continue

```python
>>> a = 0
>>> while a < 50:
...     a += 1
...     if a % 2 == 0:
...         continue
...     else:
...         print(a)
...

> 1
> 3
> 5
...
> 47
> 49
```

## 🕵️‍♀️For 반복문

**Syntax**

```python
>>> for <conditional expression>:
...     <code1>
...     <code2>
        
```

**Examples**
(1) 보통 range함수와 같이 쓰입니다.
```python
>>> for i in range(10): #for(i=0;i<10;i++) 과 같습니다.
...     print(i)
...

> 0
> 1
...
> 8
> 9
```

**range함수는 인자의 값만큼 사이클마다 0부터 하나씩 변수 i에 대입합니다.<br>
아래와 같이 i에 값을 대입해도 range함수에서 i에 다시 덮어 씌웁니다.
```python
>>> for i in range(10):
...     print(i, end=' ')
...     i = 5
...

> 0 1 2 3 4 5 6 7 8 9
```

(2) range 함수 응용
<br>
2.1) 원하는 범위를 지정할 수 있습니다.

```python
>>> for i in range(5,8):
... print(i, end=' ')
...

> 5 6 7
```

2.2) i의 증가폭을 설정할 수 있습니다.
```python
>>> for i in range(0,20,5):
... print(i,end=' ')
...

> 0 5 10 15 
```
감소도 가능합니다.
```python
>>> for i in range(10,0,-3):
... print(i,end=' ')
...

> 10 7 4 1
```

2.3) 리스트를 대입할 수 있습니다.
```python
>>> a = [2,3,5,7,11,13]
>>> for i in range(a):
...     print(a, end='')
...

> 2 3 5 7 11 13
```

**리스트 뿐만 아니라 튜플, 문자열 들 모든 시퀀스로 이용 가능합니다.**

2.4) break, continue 모두 사용 가능합니다.
```python
>>> for i in range(1,30):
...     if i % 3 == 0:
...         break
...     print(i, end =' ')

> 1 2
```


## 🦹Quiz
 $$ 반복문을 이용하여 다음을 출력해보세요

 ```
 *
 **
 ***
 ****
 *****

 --------------------

    *
   **
  ***
 ****
*****

---------------------

*  ************  *
**  **********  **
***  ********  ***
****  ******  ****
*****  ****  *****
******  **  ******
 ```
 <span style="color:gray">13기 김연우에게 제출하면 소정의 선물이 있다는 소문이...</span>
