---
date : 2022-08-31
title : "[Python] strftime() format Code"
comments : true
categories : 
    - Python
---

###### 파이썬의 strftime()메소 포맷 코드를 모아놓은 표입니다.

* 사용예시 :

```python
import datetime

time = datetime.datetime.now()
print(time.strftime('%Y년 %m월%d일 %H시%M분%S초\n'))
```

* strftime() 포맷 코드표 : 

<img width="724" alt="스크린샷 2022-09-01 오후 5 16 45" src="https://user-images.githubusercontent.com/55019557/187866833-dcb6f7be-4c75-4bdc-843a-714b5311f944.png">
<img width="725" alt="스크린샷 2022-09-01 오후 5 16 59" src="https://user-images.githubusercontent.com/55019557/187866828-3ecbf926-8bfa-43d6-89a5-daf9cdde16f0.png">
<img width="726" alt="스크린샷 2022-09-01 오후 5 17 13" src="https://user-images.githubusercontent.com/55019557/187866803-1b55cfce-486c-4f0d-8f9d-5369b9314272.png">

* 출처 : [docs.python.org](https://docs.python.org/ko/3/library/datetime.html#strftime-and-strptime-format-codes)
