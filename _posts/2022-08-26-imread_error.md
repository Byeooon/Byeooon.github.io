---
date : 2022-08-26
title : "[Computer Vision] error: (-215:Assertion failed) size.width>0 && size.height>0 in function 'imshow' 해결방법"
comments : true
categories : 
    - Computer Vision
---

###### 아래의 에러 발생시 해결할 수 있는 방법에 대해 설명하도록 하겠습니다.

```python
error: (-215:Assertion failed) size.width>0 && size.height>0 in function 'imshow'
```

###### 위 에러는 보통 아래의 3가지 경우에 해당하며 저의 경우에는 파일의 이름대신 파일의 절대경로를 입력해주었을 때 해결할 수 있었습니다.

* 파일 존재X
* 파일 자체의 문제
* 파일의 경로문제

