---
date : 2022-09-27
title : "[Pytorch] Pytorch GPU Acceleration on M1"
comments : true
categories :
    - Pytorch
---

###### Pytorch를 사용할 때, GPU를 활성화 시키는 방법에 대해 알아보도록 하겠습니다.

* 파이토치를 사용하기 전에 아래와 같이 torch.device에 'mps'를 할당해주면 GPU를 활성화 시킬 수 있습니다.
```python
import torch

device = torch.device('mps')
print(f"device : {device}")
print(torch.backends.mps.is_available())
```

* 실행결과 아래와 같이 정상적으로 GPU가 활성화된 것을 확인할 수 있습니다.
```python
device : mps
True
```