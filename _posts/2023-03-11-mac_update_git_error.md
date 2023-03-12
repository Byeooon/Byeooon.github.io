---
date : 2023-03-11
title : "[Mac] Mac OS 업데이트시 발생하는 Git 오류 해결방법"
comments : true
categories : 
    - Mac
---

###### 오늘은 Mac OS 업데이트시 발생하는 깃 오류와 해결방법에 대해 기록해보도록 하겠습니다.

###### Mac OS 업데이트 후 깃 명령어를 터미널에 입력할 시 아래와 같은 오류가 발생하는 경우가 있습니다. 

<br>

* 에러 메시지
```
xcrun: error: invalid active developer path ...
```

<br>



###### 이 때, 아래의 명령어를 입력하고 설치과정을 진행하면 간단하게 해결할 수 있습니다.

* 설치 명령어
```
xcode-select --install
```

###### 설치를 마치고 아래의 명령어를 통해 깃 버전을 확인해보면 다시 깃이 정상적으로 동작하는 것을 확인할 수 있습니다.

* 설치 확인
```
git --version
```