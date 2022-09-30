---
date : 2022-09-29
title : "[Computer Vision] cv2.resize() function in Detail"
comments : true
categories :
    - Computer Vision
---

###### OpenCV의 cv2.resize()함수에 대해 자세히 알아보도록 하겠습니다.
---
* 인자 설명

```python
cv2.resize(src, dsize, dst=None, fx=None, fy=None, interpolation=None)
```
|인자|설명|비고|
|-----|-----|-----|
|src|가공할 이미지나 영상||
|dsize|결과 영상 크기|(0,0) 인 경우 fx, fy인자를 이용하여 결정|
|fx,fy|x와 y방향 스케일 비율|dsize인자가 (0,0)인 경우에 유효|
|interpolation|보간법 선택|Default : cv2.INTER_LINEAR|
