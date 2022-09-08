---
date : 2022-09-08
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

```python
Collecting setuptools
  Downloading setuptools-65.3.0-py3-none-any.whl (1.2 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 1.2/1.2 MB 10.6 MB/s eta 0:00:00
Installing collected packages: setuptools
  Attempting uninstall: setuptools
    Found existing installation: setuptools 3.3
    Uninstalling setuptools-3.3:
      Successfully uninstalled setuptools-3.3
ERROR: pip's dependency resolver does not currently take into account all the packages that are installed. This behaviour is the source of the following dependency conflicts.
socketio 0.2.1 requires setuptools==3.3, but you have setuptools 65.3.0 which is incompatible.
Successfully installed setuptools-65.3.0
```

###### 해당 명령어를 실행하면 위와같은 메시지와 함께 오류를 해결할 수 있습니다.