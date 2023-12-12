---
date : 2023-12-12
title : "[Google Colab] Image input on Colab"
comments : true
categories : 
    - Google Colab
---

###### 오늘은 구글 코랩에 이미지를 삽입하는 방법에 대해 기록해보도록 하겠습니다.

###### 방법 1. 코랩 자체 기능

![img](https://github.com/Byeooon/Byeooon/assets/55019557/31ff93a0-9958-4d7b-8c88-b7e971b53754)

* 코랩에서 텍스트를 추가하고 위의 메뉴들 중 사진액자 모양의 버튼을 클릭하면 원하는 이미지를 입력할 수 있습니다.

* 하지만 이 기능을 실제로 사용해보면 여러 이미지를 넣었을 때 갑자기 이미지가 사라지는 등의 문제가 발생합니다. 그래서 저는 아래의 방법을 추천합니다.

###### 방법 2. 구글 드라이브 이용

* 먼저 구글 드라이브에 원하는 사진을 업로드

* 아래 사진과 같이 링크 생성 후 링크 복사
![스크린샷 2023-12-29 오후 4 43 16](https://github.com/Byeooon/Byeooon/assets/55019557/c6bfd797-aae6-485a-9772-5136cfcbe259)

* 포맷에 맞춰 변경
https://drive.google.com/file/d/'''사진 고유 아이디'''/view?usp=share_link

# 사진 고유 아이디 가져오기
https://drive.google.com/uc?id='''사진 고유 아이디'''

* HTML 태그 사용

```html
<img src = "https://drive.google.com/uc?id='''사진 고유 아이디'''" height = 100 width = 100>
```

###### 위의 과정을 따르면 코랩에 사진을 입력할 수 있습니다. 감사합니다.

