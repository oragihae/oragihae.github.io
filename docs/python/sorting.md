---
layout: default
title: sorting
parent: Python
---

# Sorting

- [Sorting HOW TO](https://docs.python.org/3/howto/sorting.html)

## Key Functions

```python
student_tuples = [
    ('john', 'A', 15),
    ('jane', 'B', 12),
    ('dave', 'B', 10),
]

sorted(student_tuples, key=lambda student: student[2])   # sort by age

[('dave', 'B', 10), ('jane', 'B', 12), ('john', 'A', 15)]
```


