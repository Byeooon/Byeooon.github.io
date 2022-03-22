---
date : 2022-03-22
title : "[Conda] Conda 명령어 정리"
comments : true
categories : 
    - Conda
---

### python을 사용할 때 환경을 구분하기 위해 conda를 자주사용하는데 명령어를 계속 찾아보게 되어 오늘은 conda명령어에 대해 정리해보려고한다.<br>
아래는 conda를 다운 받을 수 있는 공식 깃허브이다.<br>
miniforge3 download link : [Url](https://github.com/conda-forge/miniforge)

<br>

![콘다](https://docs.conda.io/en/latest/_images/conda_logo.svg)

<br>

* 가상환경 목록 조회
```
% conda env list
```
<br>

* 가상환경 생성
```
% conda create -n [가상환경이름] python=[버전]
```
<br>

* 가상환경 활성화
```
% conda activate [가상환경이름]
```
<br>

* 가상환경 비활성화
```
% conda deactivate [가상환경이름]
```
<br>

* 가상환경 복제
```
% conda create --clone [복제될 가상환경이름] -n [새 가상환경이름]
```
<br>

* 가상환경 삭제
```
% conda env remove -n [가상환경이름]
```
<br>

* 콘다 버전확인
```
% conda --version
```
<br>

* 콘다 정보확인
```
% conda --info
```
<br>

* 가상환경에 설치된 패키지 조회
```
% conda list
```
<br>

* 콘다를 이용한 패키지 설치
```
% conda install [패키지 이름]
```
<br>

* 콘다를 이용한 패키지 업데이트
```
% conda update [패키지 이름]
```
<br>

* 콘다를 이용한 패키지 삭제
```
% conda remove -n [가상환경이름][패키지이름]
```



