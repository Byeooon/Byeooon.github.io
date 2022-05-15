---
date : 2022-05-15
title : "[Python] Python count function"
comments : true
categories :
    - Python
---

###### 파이썬을 사용하는 중에 리스트에서 특정요소의 개수를 알아야 하는 상황이 있었습니다.
###### 찾아보니 파이썬에는 count라는 유용한 함수가 있어서 기록하게 되었습니다.
```python
list = [a,a,a,b,c,d,e]
```


###### 위와 같은 리스트가 있다고 가정했을 때


```python
value = list.count(a)
print(value)
```

###### 리스트.count(value)의 형태로 해당 리스트에 value의 값이 몇개있는지 알 수 있습니다. 위와 같은 경우에는 value에 3이 나옵니다. 
###### 오늘은 파이썬 리스트에 적용할 수 있는 count 에 대해서 알아봤습니다.
