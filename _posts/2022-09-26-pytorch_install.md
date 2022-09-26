---
date : 2022-09-26
title : "[Pytorch] Install Pytorch on M1"
comments : true
categories :
    - Pytorch
---

###### 오늘은 M1 OS위에 Pytorch를 설치하는 방법에 대해 알아보겠습니다.

###### 먼저 Pytorch 공식홈페이지에 접속해 줍니다.

* [https://pytorch.org](https://pytorch.org)

###### PyTorch Build에서 안정적인 Stable버전이 아닌, Preview 버전을 선택줘야 합니다. 왜냐하면 M1 OS위에서 GPU가속을 사용하기 위한 기능이 Preview버전에만 포함되어있기 때문입니다.

<img width="830" alt="스크린샷 2022-09-26 오후 6 35 16" src="https://user-images.githubusercontent.com/55019557/192244582-41ac1500-75c2-48fd-8c0a-f65ab398d58f.png">

###### 위의 옵션을 선택해준 후, 아래 명령어를 통해 원하는 가상환경위에 설치해줍니다.

```python
!pip3 install --pre torch torchvision torchaudio --extra-index-url https://download.pytorch.org/whl/nightly/cpu
```

###### 위의 명령어를 실행하면 아래와 같이 정상적으로 설치된 모습을 볼 수 있습니다.

```python
Successfully installed certifi-2022.9.24 charset-normalizer-2.1.1 idna-3.4 requests-2.28.1 torch-1.13.0.dev20220926 torchaudio-0.13.0.dev20220925 torchvision-0.14.0.dev20220925 typing-extensions-4.3.0 urllib3-1.26.12
```