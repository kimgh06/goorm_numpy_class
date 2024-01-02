# bool로 인덱싱

true = 뽑겠다
false = 안뽑겠다

```python
import numpy as np
a = np.arange(10)
b_i = np.array([True, False, True, False, True])
[0 2 4]

b_i = (a % 2 == 0)
# [True False ...6 elements... False True]
a[b_i] # [0 2 4 6 8]
```

```python
import numpy as np
a = np.arange(4).reshape((2, 2))
b_i = np.array([[True, False], [False, True]])
a[b_i] #[0 3]
```