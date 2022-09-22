---
date : 2022-09-22
title : "[Computer Vision] OpenCV Image Processing"
comments : true
categories :
    - Computer Vision
---

###### OpenCV를 이용해 이미지를 처리하는 방법에 대해 알아보도록 하겠습니다.


* 밝기 조절
```python
cv2.add([src],[val])
```
###### val : 조절할 밝기 값

* 크기 조절
```python
cv2.resize([src], (30,30))
```
###### src를 30X30으로 변경
