---
date : 2022-08-19
title : "[Computer Vision] cv2.imwrite 확장자 오류"
comments : true
categories : 
    - Computer Vision
---

* 아래와 같이 파일의 확장자를 지정해주지 않으면 아래와 같은 오류가 발생한다.
```python
import cv2
cv2.imwrite("dog", img)
```
* 오류내용
```python
cv2.error: OpenCV(4.6.0) /io/opencv/modules/imgcodecs/src/loadsave.cpp:730: error: (-2:Unspecified error) could not find a writer for the specified extension in function 'imwrite_'
```

* 아래와 같이 정확하게 확장자를 명시함으로써 해당 오류를 해결할 수 있습니다.
```python
import cv2
cv2.imwrite("dog.jpg", img)
```


