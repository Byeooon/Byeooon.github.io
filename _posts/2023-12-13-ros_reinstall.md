---
date : 2023-12-13
title : "[ROS] ROS remove"
comments : true
categories : 
    - ROS
---

###### 오늘은 기존 ROS를 삭제하고 재설치하는 방법에 대해 기록해보도록 하겠습니다.

###### ROS환경에서 오류가 나서 환경을 밀어야하는 경우에 사용하면 좋을 것 같습니다. 환경을 삭제하기전에 중요파일들은 모두 백업하는 것을 꼭! 잊으면 안됩니다.

###### 기존 ROS 삭제 
 
```
$ sudo apt-get purge ros-*
// 패키지, 설정파일 모두 삭제

$ sudo apt-get remove ros-*
// 패키지 삭제, 설정파일 유지
```

###### ROS 삭제 확인

```
% rosversion -d
// <unknown> : 삭제완료
// 기존 ROS가 확인될 경우 : reboot
```








