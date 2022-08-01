---
date : 2022-04-05
title : "[Algorithm] 2의 거듭제곱 판별"
comments : true
categories : 
    - Algorithm
---

```c++
#include <iostream>
#include <cmath>
using namespace std;

int num;
int testcase;
int flag;

int digit(int num) //자리수 출력
{
    int cnt = 0;
    while (num > 0)
    {
        num = num / 10;
        cnt++;
    }
    return cnt;
}

int main()
{
    cin >> testcase;
    for(int i = 0;i < testcase; i++)
    {
        cin >> num;
        int count = digit(num);
        while(num > 0)
        {
            int result = num%10;
            unsigned long int tmp = pow(result, count);
            tmp = tmp%10;
        

            if(tmp == 0 || tmp == 1 || tmp == 4 || tmp == 5 || tmp == 6 || tmp == 9)
                flag = 1;
            else
            {
                flag = 0;
                break;
            }
            num = num/10;
        }
        cout << flag << endl;
    }
    return 0;
}

```