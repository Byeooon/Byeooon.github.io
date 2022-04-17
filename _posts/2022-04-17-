---
date : 2022-04-17
title : "[C++] 주가분석"
comments : true
categories : 
    - C++
---

```c++
#include <iostream>
using namespace std;

int main()
{
    int testcase;
    cin >> testcase;
    while (testcase)
    {
        int yesterday;
        int today;
        int days;
        int nums;
        bool flag = false;
        int high_count = 0;

        cin >> days;
        
        for(int i = 0 ; i < days; i++)
        {
            cin >> nums;
            if(i == 0) //첫째날
            {
                today = nums;
                flag = false;
            }
            else
            {
                today = nums;
                if(flag == true && yesterday > today)
                {
                    high_count++;
                    flag = false;
                }
                else if(flag == true && yesterday == today)
                {
                    continue;
                }
                else if(yesterday < today)
                flag = true;
            }

            if(flag)
            {
                yesterday = today;
                
                continue;
            }
            else
            {
                flag = false;
            }
            yesterday = today;
        }
        cout << high_count << endl;
       testcase--;
    }
    

    return 0;
}

```