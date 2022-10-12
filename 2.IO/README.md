## 👨‍💻 들어가며

>

## ✍️ 출력 함수

> print를 알아보자

<br >

**Syntax**

```python
print(object(s), sep=separator, end=end, file=file, flush=flush)
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
