---
date : 2022-07-05
title : "[Homebrew] Homebrew error on M1"
comments : true
categories :
    - Homebrew
---

###### 기본적으로 Homebrew는 아래와 같이 공식홈페이지에 있는 명령어를 터미널에 복사하여 실행함으로서 설치할 수 있습니다.

<img width="400" alt="스크린샷 2022-07-07 오후 7 43 21" src="https://user-images.githubusercontent.com/55019557/177755479-21fa4558-e663-41b9-b588-8af63ce8121f.png">

* Homebrew 설치 명령어 🍺
```python
$ /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

###### 하지만 설치가 완료된 후, Homebrew를 사용하려고 할 때,아래와 같이 Rosetta 2와 관련된 오류가 발생하는 경우가 있습니다.
```python
Cannot install under Rosetta 2 in ARM default prefix (/opt/homebrew)!
```

###### 이 경우에는 아래와 같은 명령어로 해결할 수 있습니다.
```python
$ arch -arm64 brew install [패키지 이름]
```

###### 하지만 매번 Homebrew를 이용할 때 마다 위와같은 추가 명령어를 입력할 순 없으니 근본적인 해결법을 다음글에서 설명하도록 하겠습니다.

