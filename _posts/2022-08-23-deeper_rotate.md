---
date : 2022-08-23
title : "[Computer Vision] OpenCV cv2.getRotationMatrix2D"
comments : true
categories : 
    - Computer Vision
---

###### 2차원 이미지를 회전시킬 수 있는 cv2.getRotationMatrix2D() 사용법에 대해 알아보도록하겠습니다.

```python
import cv2
import numpy as np

img = cv2.imread("testFire.jpg", cv2.IMREAD_COLOR)

# 이미지 크기 확인, 중심을 계산.
(h, w) = img.shape[:2]
(cX, cY) = (w // 2, h // 2)
 
#45degree Rotation
rotate_45 = cv2.getRotationMatrix2D((cX, cY), 45, 1.0)
img_45 = cv2.warpAffine(img, rotate_45, (w, h))
 
#90degree Rotation
rotate_90 = cv2.getRotationMatrix2D((cX, cY), 90, 1.0)
img_90 = cv2.warpAffine(img, rotate_90, (w, h))

#135degree Rotation
rotate_135 = cv2.getRotationMatrix2D((cX, cY), 135, 1.0)
img_135 = cv2.warpAffine(img, rotate_135, (w, h))

#180degree Rotation
rotate_180 = cv2.getRotationMatrix2D((cX, cY), 180, 1.0)
img_180 = cv2.warpAffine(img, rotate_180, (w, h))

#225degree Rotation
rotate_225 = cv2.getRotationMatrix2D((cX, cY), 225, 1.0)
img_225 = cv2.warpAffine(img, rotate_225, (w, h))

#270degree Rotation
rotate_270 = cv2.getRotationMatrix2D((cX, cY), 270, 1.0)
img_270 = cv2.warpAffine(img, rotate_270, (w, h))

#315degree Rotation
rotate_315 = cv2.getRotationMatrix2D((cX, cY), 315, 1.0)
img_315 = cv2.warpAffine(img, rotate_315, (w, h))

# Show image
# cv2.imshow("rotate0", img)
# cv2.imshow("rotate45", img_45)
# cv2.imshow("rotate90", img_90)
# cv2.imshow("rotate180", img_180)
# cv2.imshow("rotate225", img_225)
# cv2.imshow("rotate270", img_270)
# cv2.imshow("rotate315", img_315)

# Save image
# cv2.imwrite("afRt/rotate.jpg", img) #원본
cv2.imwrite("fire45.jpg", img_45)
cv2.imwrite("fire90.jpg", img_90)
cv2.imwrite("fire180.jpg", img_180)
cv2.imwrite("fire225.jpg", img_225)
cv2.imwrite("fire270.jpg", img_270)
cv2.imwrite("fire315.jpg", img_315)

cv2.waitKey()
cv2.destroyAllWindows()
```