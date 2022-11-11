---
layout: default
title: OrderedDict
parent: Python
nav_order: 4
---

# OrderedDict

- [docs: OrderedDict](https://docs.python.org/ko/3/library/collections.html#collections.OrderedDict)
- [OrderedDict in Python](https://www.geeksforgeeks.org/ordereddict-in-python/)


```python
# A Python program to demonstrate working of OrderedDict
from collections import OrderedDict

print("This is a Dict:\n")
d = {}
d['a'] = 1
d['b'] = 2
d['c'] = 3
d['d'] = 4

print("\nThis is an Ordered Dict:\n")
od = OrderedDict()
od['a'] = 1
od['b'] = 2
od['c'] = 3
od['d'] = 4


This is a Dict:
a 1
c 3
b 2
d 4

This is an Ordered Dict:
a 1
b 2
c 3
d 4
```

- 그냥 dict는 순서가 보장 되지 않음
- OrderedDict 는 넣는 순서대로 나옴 (순서가 보장됨)
  - 키가 삽입되는 순서
  - value가 나중에 바껴도 순서는 그대로 (키 순서 기준)
  - 중간에 키가 하나 빠지면 그거 빼고 그대로 순서 유지
