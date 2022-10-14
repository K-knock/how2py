
## List to Dict

> List 에서 Dict으로 변환하는 방법에는 여러가지 방법이 있습니다.

<br>
아래와 같은 리스트가 있을 때.

```python
string_list = ['A','B','C']
int_list = [1, 2, 3]
```

<br>

**1\. Dictionary Comprehesion(딕셔너리 컴프리헨션) 이용**

```python
string_list = ['A','B','C']
dictionary = {string : 0 for string in string_list}
print(dictionary)
```

```python
{'A': 0, 'B': 0, 'C': 0}
```
<br>

위의 방식을 조금 변경하면

```python
string_list = ['A','B','C']
dictionary = {string : i for i,string in enumerate(string_list)}
print(dictionary)
```

```python
{'A': 0, 'B': 1, 'C': 2}
```

이런식의 코딩도 가능합니다.

<br>

**2\. dict.fromkeys(key, value) 이용**

```python
string_list = ['A','B','C']
dictionary = dict.fromkeys(string_list,0)
print(dictionary)
```

```python
{'A': 0, 'B': 0, 'C': 0}
```
<br>
Value에 아무것도 적지 않는다면 value는 None으로 됩니다.

```python
string_list = ['A','B','C']
dictionary = dict.fromkeys(string_list)
print(dictionary)
```

```python
{'A': None, 'B': None, 'C': None}
```
<br>

**3\. list의 값을 value로 갖는 dict 만들기 (1번 방법에서 key와 value가 반대로)**

```python
string_list = ['A','B','C']
dictionary = {i : string_list[i] for i in range(len(string_list))}
print(dictionary)
```

```python
{0: 'A', 1: 'B', 2: 'C'}
```


<br>

**4\. zip 사용하여 묶기**

```python
string_list = ['A','B','C']
int_list = [1, 2, 3]
dictionary = dict(zip(string_list, int_list))
print(dictionary)
```

```python
{'A': 1, 'B': 2, 'C': 3}
```

<br>


물론 string\_list 와 int\_list의 순서를 바꾸면 key와 value도 변경됩니다.

```python
string_list = ['A','B','C']
int_list = [1, 2, 3]
dictionary = dict(zip(int_list, string_list))
print(dictionary)
```

```python
{1: 'A', 2: 'B', 3: 'C'}
```

<br>
<br>

## Tuple to Dict

```python
tuple_list = [('A',1), ('B',2), ('C',3)]
```
<br>

**1\. dict() 사용하기**

```python
tuple_list = [('A',1), ('B',2), ('C',3)]
dictionary = dict(tuple_list)
print(dictionary)
```

```python
{'A': 1, 'B': 2, 'C': 3}
```