# ndarray 의 flattening

평평히 ndarray를 1차원으로 바꾸는 것

flatten은 reshape의 역 연산이다.

깊은 복사.

```python
import numpy as np

M = np.arange(9)
# 0 ~ 8
N = M.reshape((3,3))
# [[0 1 2] [3 4 5] [6 7 8]]
O = N.flatten()
# 0 ~ 8

M = np.arange(27)
# 0 ~ 26
N = M.reshape((3, 3, 3))
# [
#  [[0 1 2] [3 4 5] [6 7 8]]
#  [[9 10 11] [12 13 14] [15 16 17]]
# [[18 19 20] [21 22 23] [24 25 26]]
# ]
O = N.flatten()
# 0 ~ 26
```

ravel

얕은 복사

```python
import numpy as np

M = np.arange(9)
# 0 ~ 8
N = M.reshape((3, 3))
# [[0 1 2] [3 4 5] [6 7 8]]
O = N.ravel()
# 0 ~ 8
```