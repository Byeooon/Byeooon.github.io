---
date : 2022-12-15
title : "[YOLO] YOLOv5 Execution error on Linux"
comments : true
categories : 
    - YOLO
---

###### Linux OS상에서 갑자기 YOLOv5가 실행이 되지 않았을 때가 있었고, 해당 오류를 해결한 방법을 기록해보록 하겠습니다.

* 에러 메시지
```
importerror: /usr/lib/x86_64-linux-gnu/libstdc++.so.6: version `glibcxx_3.4.26' not found
```

* 에러 원인

###### glibcxx_3.4.26이 설치되어 있지 않았기 때문에 에러가 발생한 것이다. 

* 해결 명령어
```
sudo add-apt-repository ppa:ubuntu-toolchain-r/test
sudo apt-get update
sudo apt-get install gcc-4.9
sudo apt-get install --only-upgrade libstdc++6
```

* [Reference](https://m.blog.naver.com/dnjswns2280/222056649970)