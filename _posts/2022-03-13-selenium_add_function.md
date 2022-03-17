---
date : 2022-03-13
title : "[WebCrawaling] 셀레니움 기능 추가"
comments : true
categories :
    - WebCrawling
---

*셀레니움 라이브러리를 이용하여 페이지를 스크롤링하는 기능과 확장기능을 추가하였습니다*

```python
from selenium import webdriver
from selenium.webdriver.common.keys import Keys
import time
import urllib.request
from selenium.webdriver.common.by import By

#구글페이지에 기본적인 이미지 수는 50장

keyword = input("검색어를 입력하시오 : ")
count = 1

driver = webdriver.Chrome("/Users/byeon/PycharmProjects/Kobot/Chrome_Driver/chromedriver")
driver.get("https://www.google.co.kr/imghp?hl=ko&ogbl ")

elem = driver.find_element(by = By.NAME, value = "q") #검색창 불러오기
elem.send_keys("윈터") #검색창에 검색어 입력
elem.send_keys(Keys.RETURN) #Enter입력

SCROLL_PAUSE_TIME = 3.0 #스크롤 하는 시간 / 이 시간이 짧으면 스크롤을 다 하기전에 이미지를 불러오기 시작해 오류가 발생할 수 있다.

# Get scroll height
last_height = driver.execute_script("return document.body.scrollHeight")

while True:         #stackoverflow
    # Scroll down to bottom
    driver.execute_script("window.scrollTo(0, document.body.scrollHeight);")

    # Wait to load page
    time.sleep(SCROLL_PAUSE_TIME)

    # Calculate new scroll height and compare with last scroll height
    new_height = driver.execute_script("return document.body.scrollHeight")
    if new_height == last_height:
        break
    last_height = new_height

    # if new_height == last_height: #더보기 버튼을 눌러주는 기능
    #     try : #더보기 버튼이 없는 맨 마지막에서 발생하는 오류를 잡기위한 코드
    #         driver.find_elements(by=By.CSS_SELECTOR, value=".mye4qd").click()
    #     except :
    #         break
    # last_height = new_height

images = driver.find_elements(by = By.CSS_SELECTOR, value = ".rg_i.Q4LuWd" ) #작은 이미지의 특정요소 가져오기

for image in images :
    image.click()
    time.sleep(2) #시간지연을 위한 코드, 여기선 2초마다 imgae 저장
    # imgURL = driver.find_element_by_css_selector(".n3VNCb") ###selenium 3 version###
    imgURL = driver.find_element(by=By.XPATH, value='/html/body/div[2]/c-wiz/div[3]/div[2]/div[3]/div/div/div[3]/div[2]/c-wiz/div/div[1]/div[1]/div[2]/div/a/img').get_attribute("src")
    urllib.request.urlretrieve(imgURL, keyword + str(count) + ".jpg")
    count += 1
    
```
