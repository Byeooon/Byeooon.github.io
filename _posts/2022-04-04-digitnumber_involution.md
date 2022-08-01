---
date : 2022-04-06
title : "[Algorithm] 자리수 거듭제곱 판별"
comments : true
categories : 
    - Algorithm
---

###### 전에 구현하였던 2의 제곱수와 다르게 입력되는 자리수 크기만큼의 거듭제곱수를 구하는 알고리즘입니다.

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
        int sum = 0;
        cin >> num;
        int answer = num;
        int count = digit(num);
        while(num > 0)
        {
            int result = num%10;
            unsigned long int tmp = pow(result, count);
            sum += tmp;
            num = num/10;
        }

        if(sum == answer)
            flag = 1;
        else
        {
            flag = 0;
        }
        cout << flag << endl;
    }
    return 0;
}

```
