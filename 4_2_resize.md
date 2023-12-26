# resize

reshape이랑 resize는 달라요.

shape -> ()
size -> 100 더 조심

```python
import numpy as np

a = np.arange(6)
b = np.resize(a, (2, 3))

a # [0 1 2 3 4 5]
b # [[0 1 2] [3 4 5]]
```

> If the new array larger than the original array, then the new array is filled with repeated copies of a.
> 
>새로운 배열이 기존 배열 보다 크다면, 새로운 배열은 a의 복사본을 반복해서 채워질 것입니다.

> Note that this behavior is different from a.resize(new_shape) which fills with zeros instead of repeated copies of a.
>
> 이 동작은 a의 반복해서 복사본을 채우는 대신 0으로 채우는 a.resize(new_shape)와 다름을 알고 있으세요.


```python
import numpy as np

a = np.arange(6)
b = np.reshape(a, (9, ))

# ValueError: cannot reshpae array of size 6 into shape (9, )

b = np.resize(a, (9, )) # [0 1 2 3 4 5]-> [0 1 2 3 4 5 0 1 2]

c = np.resize(a, (3, 4)) # [0 1 2 3 4 5] -> [[0 1 2 3] [4 5 0 1] [2 3 4 5]]

d = np.arange(9)
e = np.resize(d, (2, 3, 3)) # [0 1 2 3 4 5 6 7 8] -> [[[0 1 2] [3 4 5] [6 7 8]] [[0 1 2] [3 4 5] [6 7 8]]]
f = np.resize(d, (2, 2)) # [0 1 2 3 4 5 6 7 8] -> [[0 1] [2 3]]
```

reshape 은 안정적이고, resize는 더 많이 인자를 넣을 수 있음.

```python
import numpy as np

a = np.arange(9) # [0 2 3 4 5 6 7 8]
b = a.resize((2, 2)) # return None. no return, only changing origin

a # [[0 1] [2 3]]
```

np.resize, np.reshape와 ndarray.resize, ndarray.reshape는 다른 함수 입니다.

