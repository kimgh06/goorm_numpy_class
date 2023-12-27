# dtype 바꾸기

```python
import numpy as np

M = np.array([1, 2, 3], np.int8)

N = M.astype(np.uint32)
O = M.astype(np.float32)

M = np.random.uniform(low=-10, high=10, size=(3,3))

M # float64 array
M.astype(np.int32) # int32 array

bools = np.array([True, False]) # [True False]
bools.astype(np.int) # [1 0]
bools.astype(np.float) # [1. 0.]

ints = np.array([-2, -1, 0, 1, 2]) 
ints.astype(np.bool) # [True, True, False, True, False]

0 == False # True
1 == True # True
3 == True # False
```