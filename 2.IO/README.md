## ✍️ 출력 함수

> python의 출력함수를 알아보자

<br >

**Syntax**

```python
print(object(s), sep=..., end=..., file=..., flush=...)
```

<br >

**Parameter**

| Parameter         | Optional | Description                           | Default |
| ----------------- | -------- | ------------------------------------- | ------- |
| _Object(s)_       |          | _넣은 object 출력 (개수 상관 x)_      |
| _sep='separator'_ | O        | _object를 여러 개 넣었을 때의 구분자_ | ' '     |
| _end='end'_       | O        | _마지막에 출력할 값_                  | _'\n'_  |

<br >

**Examples**

(1) 여러 Object들을 출력할 수 있습니다.

```python
print("Hello World!")

> Hello World!
```

```python
a = "Hello World!"
print(a)

> Hello World!
```

```python
a = "Hello"
print(a, "World!")

> Hello World!
```

<br >
(2) object를 여러 개 넣었을 때 구분자를 지정할 수 있습니다.

```python
# 기본 값 (" "), a와 World! 문자열 사이에 공백
a = "Hello"
print(a, "World!")

> Hello World!
```

```python
# ("+"), a와 World! 문자열 사이에 "+"
a = "Hello"
print(a, "World!", sep="+")

> Hello+World!
```

<br >
(3) 마지막에 출력할 값을 지정할 수 있습니다.

```python
# 기본 값 ("\n"), Hello 출력이 끝난 후 줄바꿈 출력
print("Hello")
print("World!")

> Hello
World!
```

```python
# (" "), Hello 출력이 끝난 후 공백 출력
print("Hello", end=' ')
print("World!")

> Hello World!
```

<br >

**String formatting**

python도 C처럼 문자열과 변수 값을 적절히 섞어서 출력할 수 있습니다. <br >
속도 그리고 가독성면에서 **f-string**이 젤 좋습니다:)

<br >
(1) , (comma)

```python
a = "Hello"
print(a, "World!")

> Hello World!
```

<br >

(2) % operator

```python
a = "World!"
b = 1234

# C의 printf와 익숙한 방식
print("Hello %s" % a)

> Hello World!

# 타입 지정 필수, integer는 i로
print("Hello %i" % b)

> Hello 1234

# 만약 타입이 틀렸다면? 에러 발생
print("Hello %i" % a)

> TypeError: %i format: a number is required, not str

# 여러 개 한다면?
print("Hello %s %i" % (a,b))
```

<br >

(3) str.format (python3)

```python
a = "Hello"
b = "World!"

# {} 사용
print("{} {}".format(a, b))

> Hello World!

# {이름} 사용
print("{name1} {name2}".format(name1=a, name2=b))

> Hello World!

# {번호} 사용
print("{1} {0}".format(b, a))

> World! Hello
```

<br >

(4) f-string

```python
a = "World!"

# 앞에 f를 붙여주면 {} 안의 값을 변수로 인식합니다.
print(f"Hello {a}")

> Hello World!

# '{' 를 출력
print(f"{{")

> {
```

<br >

위 내용 중 첫 번쨰를 제외한 모든 방법은 print 밖에서도 사용할 수 있습니다.

```python
# print 밖에서, 즉 변수 할당 같을 때도 사용 가능하다!
# 사실 밖에서 되는 것이 원래 맞고, print 안에서는 이 연산을 하는 것
a = "Hello %s" % "World!"
print(a)

> Hello World!
```

<br >

## 📖 입력 함수

> python의 입력 함수를 알아보자

<br >

**syntax**

```python
input(prompt)
```

<br >

**Parameter**

| Parameter | Description                             |
| --------- | --------------------------------------- |
| _prompt_  | _String, input 받기 전에 출력할 메시지_ |

<br >

**Example**

(1) 입력 값을 받아올 수 있습니다.

```python
x = input()
print(x)

Hello?
> Hello?
```

<br>

(2) 입력받을 때 설명할 메시지를 지정할 수 있습니다.

```python
x = input("숫자를 입력해주세요 ")
print(x)

숫자를 입력해주세요 33
> 33


```

<br >

(3) 한 번에 여러 개의 변수를 입력받을 수 있습니다.

```python
#spilt()의 이용
a,b = input("두개의 숫자를 입력해주세요 ").split()
print(a)
print(b)

두개의 숫자를 입력해주세요 12 13
> 12
> 13
```

```python
#split()의 기본값은 공백으로 받지만 '구분자'를 기준으로 나누어 받을 수 있습니다.
#seq='(구분자)' 로 이용합니다.
a,b = input("숫자, 숫자 형식으로 값을 입력해주세요 ").split(sep=',')
print(f"{a} {b}")

숫자, 숫자 형식으로 값을 입력해주세요 13, 14
> 13 14
```


