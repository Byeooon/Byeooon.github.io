---
date : 2022-04-21
title : "[Algorithm] 끝자리 숫자 계산하기"
comments : true
categories : 
    - Algorithm
---

```c++
#include <iostream>
#include <algorithm>
using namespace std;

int main()
{
    int testcase;
    cin >> testcase;

    while(testcase--)
    {
       int count;
       int tmp;
       int result = 1;
       cin >> count;
       for(int i = 0; i < count; i++)
       {   
           cin >> tmp;
           tmp %= 10;
           result *= tmp;
           result %= 10;
       }
       cout << result << endl;
    }
    return 0;
}


```