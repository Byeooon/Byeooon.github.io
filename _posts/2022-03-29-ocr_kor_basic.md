---
date : 2022-03-29
title : "[OCR] OCR 한글적용 및 전처리"
comments : true
categories : 
    - OCR
---
##### 오늘은 영어가 아닌 한글을 ocr을 이용해서 추출해보도록 하겠습니다.<br> 기본적인 설정은 같지만 조금 더 편하게 코랩환경을 구축하기 위해 구글 드라이브를 마운트하겠습니다.

* ##### 아래의 한글 가사 사진을 텍스트로 추출해보도록 하겠습니다.<br>
![smokingdreams](https://user-images.githubusercontent.com/55019557/160626221-6528cccc-9aee-44dd-8c56-cd084644746c.jpeg)


* ##### 먼저 구글 드라이브를 마운트합니다.

```python
from google.colab import drive
drive.mount("/content/gdrive") #gdrive는 원하는대로 설정 가능
```

<br>

* ##### 마운트한 구글 드라이브 아래의 폴더에 한글 학습데이터를 넣어줍니다. 학습데이터는 tesseract-ocr 공식 깃허브에서 다운 받을 수 있습니다.
* ##### tesseract-ocr 공식 깃허브 한글 데이터 주소("https://github.com/tesseract-ocr/tessdata/blob/main/kor.traineddata")
```python
!cp -r /content/gdrive/MyDrive/OCR/kor.traineddata /usr/share/tesseract-ocr/4.00/tessdata
```
<br>

* ##### 기본적인 코드는 저번과 동일하고 인식하는 부분에서 저번에 넣었던 기본적인 전처리 코드 외에도 몇가지 코드를 더 추가해서 인식률을 높아보았습니다.
```python
image_name = "/content/smokingdreams.jpeg"
min_conf = 0

image = cv2.imread(image_name)
gray = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY) #grayscale로 변환
height, width = gray.shape
gray_larger = cv2.resize(gray, (2*width, 2*height), interpolation= cv2.INTER_LINEAR) #이미지 확대
denoised = cv2.fastNlMeansDenoising(gray_larger, h=10, searchWindowSize=21, templateWindowSize=7) #노이즈 제거

result = pytesseract.image_to_string(denoised, lang="kor")

print(result)
```

<br>

* ##### 이미지 확대나 노이즈를 제거하기 전의 결과물입니다.
<img width="300" alt="스크린샷 2022-03-29 오후 10 30 38" src="https://user-images.githubusercontent.com/55019557/160623077-664c7bd8-ae09-4234-b890-85060a5ab134.png">

<br>

* ##### 이미지 확대나 노이즈제거를 추가하고 난 뒤의 결과물입니다. 전처리를 하기 전보다 결과가 좋아진 모습입니다. 하지만 아직까지 완벽한 출력이 되고있는 것은 아니기 때문에 다음번에는 추가적인 전처리나 모델학습을 통해 ocr을 더욱 강화해보는 것에 도전해보도록 하겠습니다.
<img width="300" alt="스크린샷 2022-03-29 오후 10 31 23" src="https://user-images.githubusercontent.com/55019557/160623084-401daf7b-b95e-4d5a-a392-5ea70c019771.png">
