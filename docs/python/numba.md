---
layout: default
title: Numba
parent: Python
---

# Numba

- [Numba](https://numba.pydata.org/)

- 속도의 차이는 인터프리터와 컴파일러의 차이에서 기인

## [Will Numba work for my code?](https://numba.readthedocs.io/en/stable/user/5minguide.html#will-numba-work-for-my-code)

```python
from numba import jit
import numpy as np

x = np.arange(100).reshape(10, 10)

@jit(nopython=True) # Set "nopython" mode for best performance, equivalent to @njit
def go_fast(a): # Function is compiled to machine code when called the first time
    trace = 0.0
    for i in range(a.shape[0]):   # Numba likes loops
        trace += np.tanh(a[i, i]) # Numba likes NumPy functions
    return a + trace              # Numba likes NumPy broadcasting

print(go_fast(x))
```

- NumPy 사용이 많거나 루프가 많은 경우 Numba 사용하면 좋음
- 참고로 Pandas 사용한 경우는 사용 불가
