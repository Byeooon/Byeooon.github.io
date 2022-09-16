---
date : 2022-09-16
title : "[Crawaling] Google Image Downloader"
comments : true
categories : 
    - Crawling
---

```python
# pip install git+https://github.com/Joeclinton1/google-images-download.git

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

```
가상환경위치 -> lib -> python3.7 -> site-packages -> google_images_download -> google_images_download.py
```

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
