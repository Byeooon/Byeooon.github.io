---
date : 2022-09-16
title : "[Crawaling] Google Image Downloader"
comments : true
categories : 
    - Crawling
---

###### Google Image Downloader를 이용해서 이미지를 크롤링하는 방법에 대해 알아보도록 하겠습니다.

###### 먼저 명령어를 입력해줍니다.

```python
pip install git+https://github.com/Joeclinton1/google-images-download.git
```

* 소스코드 : 

```python
from google_images_download import google_images_download

def googleImageCrawling(key, limit):
    response = google_images_download.googleimagesdownload()   #class instantiation

    arguments = {"keywords" : key, "limit" : limit, "print_urls":True,
                 "chromedriver" : "./chromedriver", "format":"jpg"}
    
    paths = response.download(arguments)   #passing the arguments to the function
    print(paths)   #printing absolute paths of the downloaded images
    
key = input("키워드 입력 (복수 선정시 ',' 로 구분) : ")
limit = input("이미지 개수 입력 : ")

googleImageCrawling(key, int(limit))
```

###### 위의 소스코드를 그대로 실행하면 오류가 뜨는 경우가 있는데 이는 라이브러리 버전때문에 생기는 오류입니다. 따라서 아래의 가이드를 따라 소스코드를 바꿔주면 해결할 수 있습니다.

###### 먼저 아래 경로로 이동해 google_images_download.py를 열어줍니다.

```
가상환경위치 -> lib -> python3.7 -> site-packages -> google_images_download -> google_images_download.py
```

###### 그리고 302번으로 이동해 아래와 같이 소스 코드를 변경해줍니다.

```python
# Bypass "Before you continue" if it appears
try:
    # browser.find_element_by_css_selector("[aria-label='Accept all']").click()
    browser.find_element(by = By.CSS_SELECTOR, value = "[aria-label='Accept all']").click() #!!!
    time.sleep(1)
except selenium.common.exceptions.NoSuchElementException:
    pass

print("Getting you a lot of images. This may take a few moments...") #!!!

element = browser.find_element(by = By.TAG_NAME, value = "body")
```

###### 위의 방법대로 소스코드를 수정하고 프로그램을 실행하면 정상적으로 크롤링이 되는것을 확인할 수 있습니다.

* 참고 : [google-images-download.readthedocs.io](https://google-images-download.readthedocs.io/en/latest/examples.html#)
