# 인덱싱과 슬라이싱

무시하지 마세요

```python
import numpy as np

a = np.arange(10) # [0 1 2 3 4 5 6 7 8 9]

a[-1] # 9
a[-2] # 8

a[0:3]
 # inclusive: exclusive 0부터 3전 까지

a[0:-1] 
# 0 부터 마지막 인덱스 전까지

a[0:] # 0 부터 끝 까지

a[-2:] # 마지막 두 개만

a[:-3] # 마지막 3개 빼고

a[:] # 다

a[::2] # 0 부터 끝까지 2개 마다

a[-1:0:2] # 마지막 부터 처음까지 다.


```