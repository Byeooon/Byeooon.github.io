---
date : 2022-04-08
title : "[C++] 기본 배열 출력"
comments : true
categories : 
    - C++
---

```c++
#include <iostream>
#define SIZE 10
using namespace std;

int arr[SIZE][SIZE];

int main()
{

    int num = 10;
    int cnt = 1;

    for(int i = 0; i < num; i++)
    {
        for(int j = 0; j < num; j++)
        {
            arr[i][j] = cnt++;
            cout << arr[i][j] << " ";
        }
    cout << "\n";
    }

}
```