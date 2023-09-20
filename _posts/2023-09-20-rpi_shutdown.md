---
date : 2023-09-20
title : "[Raspberry Pi] Rasberry Pi Soft Shutdown"
comments : true
categories : 
    - Raspberry Pi
---

###### 라즈베리파이의 전원을 끌 때 안전하게 종료하는 방법을 기록해보도록 하겠습니다.

###### 라즈베리파이는 따로 전원종료 방법이 존재하지 않기 때문에 선을 뽑아 종료하게 되는 경우가 있지만, 이런 경우에 내부 손상이 발생할 수 있기 때문에 명령어를 통해 종료시켜주는 것이 안전한 방법입니다.


* 종료 명령어

```
$sudo shutdown -h now
```