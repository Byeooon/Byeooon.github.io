---
date : 2022-08-30
title : "[YOLO] AttributeError: Can't get attribute 'DetectionModel' on <module 'models.yolo' from '...'> 해결방법"
comments : true
categories : 
    - YOLO
---

###### track.py에 custom dataset을 weights파일로 적용하려고 할 때 아래와 같은 에러가 발생하는 경우가 있습니다. 
```python
AttributeError: Can't get attribute 'DetectionModel' on <module 'models.yolo' from './models/yolo.py'>
```

###### 이는 구버전의 yolo.py가 적용되어있을 때 발생하는 오류입니다.

* [GITHUB LINK](https://github.com/ultralytics/yolov5/blob/master/models/yolo.py)

###### 위의 공식 레포지토리에 접속해 최신버전으로 파일을 교체해주면 정상적으로 작동하는 것을 확인할 수 있습니다.