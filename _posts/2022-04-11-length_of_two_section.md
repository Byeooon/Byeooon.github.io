---
date : 2022-04-09
title : "[Algorithm] 두 구간이 차지하는 길이"
comments : true
categories : 
    - Algorithm
---

```c++
#include <iostream>
using namespace std;

int main()
{
    int testcase;
    cin >> testcase;
    
    while(testcase--)
    {   
        int a,b,c,d;
        cin >> a >> b >> c >> d;

        if(a >= c)
        {
            int tmp1 = c;
            int tmp2 = d;
            c = a;
            d = b;
            a = tmp1;
            b = tmp2;
        }

        if(b >= c && b <= d) // 겹치는 경우
        {
            cout << b - c << " " << d - a << endl;
        }
        else if(b >= c && b >= d) //포함하는 경우
        {
            cout << d - c << " " << b - a << endl;
        }
        else //나머지
        {
            cout << 0 << " " << (b - a) + (d - c) << endl;
        }

    }
    return 0;
}
```