# Learning Python
----------------


### import re <br>

[字符串匹配](https://blog.csdn.net/qq_34500270/article/details/82899057) <br>
```python
import re 

line="this hdr-biz model server" 
pattern=r"hdr-biz" 
m = re.search(pattern, line) 
```

### 处理异常<br>
[Try expect](https://www.cnblogs.com/Lival/p/6203111.html) <br>
```python
try:
  instruct
except Exception as e:
  print(str(e))
```

### Resample重采样<br>
```python
import numpy as np
from skimage import io,transform,util,exposure

mat=io.imread(filename)
#必须先resize在repeat和reshape,不然输出一维或者二维的变量
mat = transform.resize(mat,(224,224),mode = 'reflect')
mat=np.repeat(mat,3).reshape(224,224,3)
```
