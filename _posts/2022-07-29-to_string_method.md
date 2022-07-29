---
date : 2022-07-29
title : "[C++] to_string 메소드"
comments : true
categories : 
    - C++
---

###### C++ <string> headerfile에 존재하는 to_string 사용법입니다.
###### 위의 method를 사용하면 string의 형태로 변환가능합니다.

```c++
// to_string example
#include <iostream>   // std::cout
#include <string>     // std::string, std::to_string

int main ()
{
  std::string pi = "pi is " + std::to_string(3.1415926);
  std::string perfect = std::to_string(1+2+4+7+14) + " is a perfect number";
  std::cout << pi << '\n';
  std::cout << perfect << '\n';
  return 0;
}
```

* 출처 : [cplusplusreference](https://cplusplus.com/reference/string/to_string/)