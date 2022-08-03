---
date : 2022-08-03
title : "[C++] Descending order Sort"
comments : true
categories :
    - C++
---

* 기본적인 Sort 사용법 ( ex : vector )
```c++
#include <algorithm>
sort(vec.begin(), vec.end())
```
###### (ascending order)

* 내림차순으로 정렬해야 할 경우( ex : vector )
```c++
#include <algorithm>
sort(vec.begin(), vec.end(), greater<>())
```
###### (descending order)