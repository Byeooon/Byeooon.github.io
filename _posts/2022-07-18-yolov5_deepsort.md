---
date : 2022-07-18
title : "[YOLO] Yolov5 + Deepsort on Colab"
comments : true
categories : 
    - YOLO
---

###### Yolov5에 Deepsort 알고리즘을 적용한 코드를 Google Colab에서 실행시킬 수 있는 코드입니다.

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
* [Github](https://github.com/AarohiSingla/Object-Tracking-Using-YOLOv5-and-DeepSORT)