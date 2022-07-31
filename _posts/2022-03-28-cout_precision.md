---
date : 2022-03-28
title : "[Algorithm] A/B"
comments : true
categories : 
    - Algorithm
---
### 문제 : 두 정수 A와 B를 입력받은 다음, A/B를 출력하는 프로그램을 작성하시오.<br>

```c++
#include <iostream>
using namespace std;

long double A;
long double B;


int main()
{
    cin >> A >> B;
    
    cout.precision(10); //소수점의 자리수를 조절. 기억해두면 유용할 함수이다.

    cout << A/B << endl;

    return 0;
}
```