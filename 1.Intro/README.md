## ☝️ 들어가며

> 학습 난이도, 그리고 응용 측면에서 한국어와 매우 유사합니다.

파이썬(Python)은 1990년 암스테르담의 귀도 반 로섬(Guido Van Rossum)이 개발한 **인터프리터 언어**입니다.<br>

쉽고 간결한 문법구조에 힘입어 많은 사용자층을 만들어냈고, 이로 인해 방대한 양의 데이터가 구축되어있어 매우매우 유용합니다.

## 인터프리터 언어

> 소스코드를 한 줄 한 줄 읽어가며 명령을 처리하는 프로그램

- 컴파일 언어가 프로그램을 전부 컴파일 하고 실행하는 데 비해 인터프리터 언어는 한 번에 한 줄씩 **바로바로** 실행이 가능합니다.
- 한 줄씩 실행을 시킬 수 있어서 **프로그램 수정이 간편**합니다.
- 단, 한 줄씩 명령을 내리다보니 **명령 자체의 처리 속도**는 느립니다.

<img src="https://github.com/x-xnocx/python/blob/main/1.Intro/img/jupyter.png">

_Jupyter Notebook으로 한 줄만 실행하는 모습_

## 특징

> Life is too short, You need python

- 파이썬은 문법이 쉽습니다.
- 파이썬은 간결합니다.
- 파이썬은 개발 속도가 빠릅니다.

## 기본 문법

> 파이썬은 일반적인 언어들과 다른 몇 특성들이 있습니다.

**`세미콜론';'`**

파이썬은 구문이 끝날 때 세미콜론을 **안 붙여도** 됩니다.

```python
print("Hello World!")

> Hello World!
```

<br >

단, 붙여도 오류가 나지는 않고, 오히려 **한 줄에 여러 구문**을 쓸 때는 사용합니다.

```python
# 세미콜론으로 구문 구별
print("Hello"); print("World!")

> Hello
World!
```

```python
# 안 붙이면 오류 발생
print("Hello") print("World!")

> SyntaxError: invalid syntax
```

**`들여쓰기`**

파이썬은 `{}` 가 들어갈 대부분의 자리에 `들여쓰기`를 사용합니다.

즉, **같은 칸 수의 들여쓰기**가 되어있는 곳은 **같은 코드 블록**이라는 의미입니다.

```C
// C에선 중괄호!
if (a == 100) {
    printf("100!");
}
```

```python
# 파이썬에선 들여쓰기!
if a == 100:
    print("100!")
```

<br >

_Q) 만약 들여쓰기가 제대로 되지 않았다면?_

```python
# 들여쓰기 실패
if a == 100:
print("100!")

> IndentationError: expected an indented block
```

<br >

들여쓰기의 방법은 여러 개지만, **공백 4칸**을 정석으로 규정하고 있습니다.

<br >

## 설치 그리고 실습 준비

- [windows python 설치](https://wikidocs.net/8)
- [실습 준비](https://wikidocs.net/9)
- [IDLE 사용하기](https://wikidocs.net/17684)

## Reference

- [파이썬이란?](https://wikidocs.net/4307)
- [인터프리터 언어(Interpreter Language) vs 컴파일 언어(Compiled Language)](https://eunjinii.tistory.com/4)
- [Windows 10 텐서플로우 환경에서 jupyter notebook 실행하기](https://blog.ggaman.com/1001)

```

```
