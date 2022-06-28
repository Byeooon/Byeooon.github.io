---
date : 2022-05-31
title : "[Raspberry Pi] 라즈베리파이 한글깨짐 문제해결"
comments : true
categories :
    - Raspberry Pi
---

![img](https://user-images.githubusercontent.com/55019557/176106661-b4b08508-3703-4545-9db4-2bd69a5b5ac4.png)

##### 라즈베리 파이 한글깨짐 해결방법

###### 라즈베리파이에 한글이 깨져서 나올 때가 있습니다. 이런 경우, 아래와 같은 명령어로 해결할 수 있습니다.

```python
sudo apt-get install fonts-unfonts-core
```
###### 위 코드를 실행한 후

```python
reboot
```
##### reboot를 해주면 정상적으로 한글이 나오는 모습을 볼 수 있습니다.
