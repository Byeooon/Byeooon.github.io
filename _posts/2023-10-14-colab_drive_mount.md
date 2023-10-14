---
date : 2023-10-14
title : "[Google Colab] Google drive Mount on Colab"
comments : true
categories : 
    - Google Colab
---

### 코랩에 구글 드라이브를 마운트 할 수 있는 방법을 기록해보도록 하겠습니다.


```python
from google.colab import drive
drive.mount('/content/drive')
```


### 위의 코드를 코랩에서 실행시키면 구글 드라이브가 마운트되고, 사용할 파일의 경로를 적절히 설정하여 사용하면 됩니다.