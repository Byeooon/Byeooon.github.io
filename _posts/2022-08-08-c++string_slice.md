---
date : 2022-08-08
title : "[C++] C++ String Slicing"
comments : true
categories :
    - C++
---

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