---
date : 2022-08-06
title : "[Computer Vision] ImportError on face_recognition Library on M1"
comments : true
categories :
    - Computer Vision
---

###### face_recognition이 정상적으로 설치된 경우에도 라이브러리를 import하는 과정에서 아래와 같은 오류가 발생할 수 있습니다.

```python
ImportError: dlopen(/Users/byeon/miniforge3/envs/byeon/lib/python3.10/site-packages/_dlib_pybind11.cpython-310-darwin.so, 0x0002): tried: '/Users/byeon/miniforge3/envs/byeon/lib/python3.10/site-packages/_dlib_pybind11.cpython-310-darwin.so' (mach-o file, but is an incompatible architecture (have 'x86_64', need 'arm64e'))
```

###### 위와 같이 오류가 발생한 경우 아래 명령어를 통해 해결할 수 있습니다.

* 먼저 원하는 가상환경으로 이동해줍니다

```python
!conda activate [가상환경]
```

```python
!conda install numpy
```

```python
!conda install pillow
```

```python
!conda install opencv
```

```python
!conda install scipy
```

```python
!conda install cmake
```

```python
!conda install -c conda-forge dlib
```

```python
!conda install -c akode face_recognition_models
```

* 위의 과정을 진행하고 재설치를 진행했을 때, ImportError가 해결되어 정상적으로 face_recognition 라이브러리를 이용할 수 있었습니다.

* 참고 : [headbreakz.tistory](https://headbreakz.tistory.com/entry/IT-python-face-recognition-설치-방법)