# 파이썬 리스트로 ndarray 만들기
 
```python
import numpy as np
np.array(3) #scholar
np.array([1,2]) #vector
np.array([[1,2,4],[3,4,6],[6,7,8]]) # matrix
np.array([
    [[1,2,3],[2,3,5]],
    [[5,8,6],[3,5,0]]
    ])# 3rd order tensor
```

shape notation

```python
import numpy as np
np.array(3).shape #()
np.array([1,2]).shape #(2,)
np.array([[1,2,4],[3,4,6],[6,7,8]]).shape # (1, 3)
np.array([
    [[1,2,3],[2,3,5]],
    [[5,8,6],[3,5,0]]
    ]).shape # (1,2,2)
```

