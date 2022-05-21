---
date : 2022-05-21
title : "[Python] Python Binary formatting"
comments : true
categories :
    - Python
---

###### 10진수를 2진수로 변환하는 것은 python에서 bin()함수를 이용하여 간단하게 할 수 있습니다.
###### 하지만 2진수를 변환할 때 bin()을 이용하면 가공하기 쉽지않은 형태로 이진수가 출력되게 됩니다.

```python
a = 3
print(bin(a))
```

###### 위와 같은 형태의 경우 출력값이 0b11의 형태로 나오게 됩니다.
###### 따라서 2진수를 변환할 때 원하는 자릿수 만큼 제가 가공하기 편한 형태로 출력할 수 있는
###### 방법이 필요했고 아래와 같은 형태로 원하는 자릿수의 2진수를 변환 및 출력할 수 있었습니다.

```python
num = 3
num_2 = 5

tmp = "{0:0" + str(num) + "b}"
tmp_2 = "{0:0" + str(num_2) + "b}"
print("formatting by 3bit : ", tmp.format(3))
print("formatting by 5bit : ", tmp_2.format(5)) 
```

###### 위와 같은 형태의 python코드를 이용하면 

##### formatting by 3bit :  011
##### formatting by 5bit :  00101
###### 위와 같은 출력값을 얻을 수 있습니다.

