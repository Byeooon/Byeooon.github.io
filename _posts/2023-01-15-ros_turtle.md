---
date : 2023-01-15
title : "[ROS] ROS turtlesim"
comments : true
categories : 
    - ROS
---


###### ROS를 설치하고 정상적으로 실행되는지 확인해보기 위해 터미널을 열고 아래의 명령어들을 순서대로 입력합니다.

```
roscore
```

```
rosrun turtlesim turtlesim_node
```

```
rosrun turtlesim turtle_teleop_key
```

###### 3번째 명령어를 입력한 터미널에 커서를 올리고 방향키를 이용해 거북이를 움직이면 정상적으로 동작하는 것을 확인할 수 있습니다.

![Screenshot%20from%202023-01-15%2004-23-08](https://user-images.githubusercontent.com/55019557/212544410-88629b4f-7820-44f9-a82c-65ca6490fd26.png)