---
date : 2022-03-27
title : "[C++] 시침과 분침 사이의 각도"
comments : true
categories : 
    - C++
---
### 시침과 분침사이의 각도를 계산하는 알고리즘을 구현하는게 핵심사항이었습니다. 그리고 자료형변환을 하면서 입력값에 손실이 생기지 않게 하는게 핵심사항이었습니다.

```c++
#include <iostream>
using namespace std;
int angleClock(int h, int m);
float angleh;
float anglem;
int result;

int main(void)
{
    int testcase;
    int h, m;

    cin >> testcase;
    for(int i=0; i<testcase; i++)
    {
        cin >> h >> m;
        angleClock( h, m );

    }
    return 0;
}

int angleClock(int h, int m)
{
    angleh = m * 0.5 + h * 30.0;
    anglem = m * 6.0;

    if (abs((angleh-anglem)) > 180)
    {
        result = 360 - abs(angleh - anglem);
        cout << result << endl;
    }
    else
    {
        result = abs(angleh - anglem);
        cout << result << endl;
    }
    return 0;
}
```