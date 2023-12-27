# 메모리 최적화

데이터 과학에서 인공지능은 굉장히 용량이 크다.

따라서 이를 다양한 분야에서 거대한 용량을 처리하기 위해 메모리 최적화는 필수다.

쓸데 없는 복사를 없애서 메모리 최적화를 하자.

복사는 독립적으로 사용함.
뷰는 메모리를 최적화하기 좋음. 독립적이지 않아 잘 못 건들면 다른 값이 수정되는 결과를 가져옴

```python
import numpy as np

a = np.arange(5)
b = a.view()
# a와 b는 같은 메모리 주소를 가짐. (포인터)

b = a[0:3]
# a와 b는 같은 메모리 주소를 가짐. (포인터)

b = a.copy()
# a에 영향을 끼치지 않음. (깊은 복사)
c = a.view()
d = a[0:3]

b.base is a # False 영향을 끼치지 않음
c.base is a # True 영향을 끼침
d.base is a # True 영향을 끼침

np.reshape() # 메모리 참조로 값을 바꿈
np.reshape().copy() # 깊은 복사후 값을 전달함
np.resize() # 깊은 복사후 값을 전달함


flatten() # 깊은 복사
ravel() # 메모리 참조
```