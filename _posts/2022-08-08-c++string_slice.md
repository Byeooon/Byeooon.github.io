---
date : 2022-08-08
title : "[C++] C++ String Slicing"
comments : true
categories :
    - C++
---

###### C++의 substr() 메소드의 사용법에 대해 알아보도록 하겠습니다.

```c++
#include <string>
#include <iostream>
using namespace std;

int main()
{
    string a = "Hello world!";
    cout << a.substr(1) << endl;
    cout << a.substr(1,3) << endl;
}
```

###### 각각의 출력값 : 
```c++
ello world!
ell
```