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
cv2.add(src,[val])
# val : 조절할 밝기 값
```


* 크기 조절
```python
cv2.resize(src, (30,30))
# src를 30X30으로 변경
```

* Blur 처리
```python
cv2.blur(src, (5,5))
# 5*5 평균값으로 이미지를 흐리게 함
# 커널의 크기가 커질수록 이미지가 더욱 흐려진다.
```






