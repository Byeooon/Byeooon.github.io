---
date : 2022-03-16
title : "[C++] 모든자리수 반복곱하기"
comments : true
categories : 
    - C++
---

```c++
#include <iostream>
using namespace std;

int testcase;
unsigned long int num;
unsigned long int result;

int main()
{
    cin >> testcase;
    for(int i = 0; i < testcase;i++)
    {
        cin >> num;
        while(num > 9)
        {
            int result = 1;
            while (num != 0)
            {
                if(num % 10 != 0)
                {
                    result *= num % 10;
                }
                else
                {
                    result *= 1;
                }
                num = num / 10;
            } //inner while
            num = result;
        }
        cout << num << endl;
        
    }
    return 0;
}
```

###### 이 문제를 통해 c++에서 어떻게 숫자를 쪼개는지 알 수 있었다.