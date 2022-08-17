---
date : 2022-07-18
title : "[Data Labeling] labelImg default label 설정하기"
comments : true
categories : 
    - Data Labeling
---

###### 데이터 라벨링 과정에서 각각의 사진마다 매번 라벨을 지정하지 않고 자동으로 라벨을 설정해주기 위한 방법에 대해 설명하도록 하겠습니다.

* 먼저 설치된 labelImg 폴더에 들어갑니다.

* labelImg에 있는 data 폴더에 들어갑니다.

###### data폴더에 들어가면 predefined_classes.txt 파일이 존재하는데 기본적으로 설정되어있는 값들을 지우고 학습시키고자 하는 모델에 맞추어 다시 설정해주면 default label을 변경할 수 있습니다.
