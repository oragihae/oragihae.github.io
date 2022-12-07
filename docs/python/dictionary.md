---
layout: default
title: dictionary
parent: Python
nav_order: 1
---

# 딕셔너리

- [docs: 딕셔너리](https://docs.python.org/ko/3/tutorial/datastructures.html#dictionaries)

```python
tel = {'jack': 4098, 'sape': 4139}
```

- key와 value
- 중괄호 사용

```python
{'jack': 4098, 'sape': 4139, 'guido': 4127}

tel['jack']
```

- key로 value 가져오기

```python
x = {100: 'hundred', False: 0, 3.5: [3.5, 3.5]}
```

- key, value 다양한 값 사용 가능
- 특히, list

```python
for k, v in day_dict.items():
```

- items()로 key, value for 문