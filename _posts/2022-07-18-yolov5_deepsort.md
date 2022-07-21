---
date : 2022-07-18
title : "[YOLO] Yolov5 + Deepsort on Colab"
comments : true
categories : 
    - YOLO
---

###### Yolov5와 Deepsort를 Colab에서 실행시킬 수 있는 코드입니다.

```python
!git clone --recurse-submodules https://github.com/mikel-brostrom/Yolov5_DeepSort_Pytorch.git
```

```python
cd Yolov5_DeepSort_Pytorch
```

```python
!pip install -r requirements.txt
```

```python
pip install torch==1.8.1+cu111 torchvision==0.9.1+cu111 torchaudio==0.8.1 -f https://download.pytorch.org/whl/torch_stable.html
```

```python
import torch
torch.cuda.is_available() 
torch.cuda.get_device_name(0)
```

* f1.mp4 부분에 원하는 옵션을 선택하여 넣어줄 수  있습니다.

```python
# python track.py --source 0  # webcam
#                            img.jpg  # image
#                            vid.mp4  # video
#                            path/  # directory
#                            path/*.jpg  # glob
#                            'https://youtu.be/Zgi9g1ksQHc'  # YouTube
#                            'rtsp://example.com/media.mp4'  # RTSP, RTMP, HTTP stream
                        

!python track.py --source f1.mp4 --save-vid --strong-sort-weights osnet_x0_25_msmt17.pt

# by adding  --strong-sort-weights osnet_x0_25_msmt17.pt .this weight will get installed automatically in your current working directory.
# After this command, you will get run folder with the results

#!python track.py --source img.jpg
```

###### 출처 : 
* [GITHUB](https://github.com/AarohiSingla/Object-Tracking-Using-YOLOv5-and-DeepSORT)