---
date : 2022-03-26
title : "[C++] 정수의 최댓값 최솟값"
comments : true
categories : 
    - C++
---

```C++
#include <iostream>
using namespace std;

int main()
{
    int testcase;
    int a;
    int tmp;
    int max = 0;
    int min = 0;

    cin >> testcase;

    for (int i = 0; i < testcase; i++)
    {
        cin >> a;
        {
            for(int j = 0; j < a; j ++)
            {
                if(j == 0)
                {
                    cin >> tmp;
                    max = tmp;
                    min = tmp;  
                }

                else
                {
                    cin >> tmp;
        
                    if(tmp > max)
                        max = tmp;

                    if(tmp < min)
                        min = tmp; 
                }
            }
            cout << max << " " << min << endl;
            max = 0;
            min = 0;
        }
    } 
    return 0;
}
```
