---
date : 2022-04-03
title : "[C++] srand, command line argument dice"
comments : true
categories : 
    - C++
---

```c++
#include <iostream>
#include <cstdlib>

using namespace std;

int main(int dicec, char *dicev[])
{
  if(dicec != 2) 
  {
    cout <<"usage: ./dice1 n" << endl; //입력값 오류 체크
    return -1;
  }

  int n = atoi(dicev[1]);
  srand(n); //입력값을 seed값으로 

  for(int i=0; i<10; i++)
  {
    int dice = rand()%6 + 1; //1 to 6
    cout << dice << " ";
  }
  cout << endl;

  return 0;
}
```

<br>

##### C++에서 srand와 command line argument를 이용해서 주사위의 값을 출력하는 프로그램을 제작해봤습니다.