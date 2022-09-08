---
date : 2022-07-18
title : "[Error] AttributeError: module 'importlib._bootstrap' has no attribute 'SourceFileLoader' 해결방법"
comments : true
categories : 
    - Error
---

###### 해당에러가 발생했을 때, 해결할 수 있는 방법에 대해 알아보도록 하겠습니다.

* 해결방법
```python
!python3 -m pip install --upgrade setuptools
```

###### 위의 에러는 setuptools에 문제가 생겨 발생하는 오류이므로 위의 명령어로 업그레이드해 해결해줄 수 있습니다.