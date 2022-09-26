---
date : 2022-09-26
title : "[Pytorch] Install Pytorch on M1"
comments : true
categories :
    - Pytorch
---

###### 오늘은 M1 OS위에 Pytorch를 설치하는 방법에 대해 알아보겠습니다.(가상환경 위에 설치하는 것을 전제.)

###### 먼저 Pytorch 공식홈페이지에 접속해 줍니다. 조금 스크롤을 내리면 아래의 화면이 나옵니다.

* [https://pytorch.org](https://pytorch.org)

###### 아래 화면의 PyTorch Build에서 안정적인 Stable버전이 아닌, Preview 버전을 선택줘야 합니다. 왜냐하면 M1 OS위에서 GPU가속을 사용하기 위한 기능이 Preview버전에만 포함되어있기 때문입니다.

<img width="819" alt="스크린샷 2022-09-26 오후 6 52 22" src="https://user-images.githubusercontent.com/55019557/192247266-d1bdbe9b-bc18-42be-8cd5-79272db115aa.png">


###### 위의 옵션을 선택해준 후, 아래 명령어를 통해 원하는 가상환경 위에 설치해줍니다.

```python
!conda install pytorch torchvision torchaudio -c pytorch-nightly
```

###### 설치확인을 위해, 간단하게 Pytorch를 이용해 텐서를 만들어 보겠습니다.

```python
import torch

x = torch.tensor([[1,2,3],[4,5,6]], dtype=torch.double)
print(x)
```

###### 위의 프로그램을 실행하면 정상적으로 아래의 결과가 나오는 것을 확인할 수 있습니다.

```python
tensor([[1., 2., 3.],
        [4., 5., 6.]], dtype=torch.float64)
```

