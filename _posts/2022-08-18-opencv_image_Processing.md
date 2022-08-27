---
date : 2022-08-18
title : "[Computer Vision] OpenCV를 이용한 이미지 출력과 저장"
comments : true
categories : 
    - Computer Vision
---

![opencv_logo_icon_170888](https://user-images.githubusercontent.com/55019557/185362228-b6584610-b972-43e4-a724-0fcb9e5ba529.png)


###### OpenCV에서 이미지를 읽고 출력하고 저장하는 방법에 대해 알아보도록 하겠습니다.

```python
import cv2

img = cv2.imread("whiteDog.jpg",cv2.IMREAD_GRAYSCALE)

cv2.imshow("whiteDog.jpg", img)

cv2.imwrite("images", img) 

cv2.waitKey() # 키보드 입력 대기
cv2.destroyAllWindows() # 모든 윈도우 제거
```

###### 이미지 읽기

* imread(filename : "이미지 경로", flag : "원하는 플래그 선택") :

###### flag에는 다양한 옵션을 줄 수 있음. 위와 같이 cv2.IMREAD_GRAYSCALE을 주면 흑백의 이미지가 나옴.

* 참고링크 : [docs.opencv.org](https://docs.opencv.org/3.4/d8/d6a/group__imgcodecs__flags.html)


###### 이미지 출력

* imshow(title : 윈도우의 제목, image : cv2.imread의 리턴값)

###### 이미지 저장

* imwrite(filename : 이미지를 저장할 경로, image : cv2.imread의 리턴값)

###### 위의 코드를 실행하면 아래의 whiteDog이미지가
![whiteDog](https://user-images.githubusercontent.com/55019557/185360454-2ceff5f8-4749-44bd-9de8-0604e19c9220.jpg)
###### grayDog로 변환되어 images에 저장되는 것을 확인할 수 있습니다.
![grayDog](https://user-images.githubusercontent.com/55019557/185360471-7a87e91e-1702-4ba2-923d-c4ccd58f5bb1.jpg)

* 참고 : [iagreebut.tistory](https://iagreebut.tistory.com/70)

