---
date : 2023-11-30
title : "[Python] Input with sys.stdin.readline"
comments : true
categories : 
    - Python
---

###### python에서 sys.stdin.readline를 이용해서 입력을 받는 방법에 대해 기록해보도록 하겠습니다.
###### 기본적인 input() 방법은 입력 횟수가 증가할 경우 속도저하의 원인이 되기 때문에 아래의 방법을 사용하는 것이 효율적입니다.

```python
import sys

a = int(sys.stdin.readline())
```

* int()를 사용하는 이유는 입력을 string 형태로 받기 때문에 형변환과 개행 문자를 제거하기 위해서 입니다.
