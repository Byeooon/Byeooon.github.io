---
date : 2022-03-23
title : "[C++] 하노이 탑"
comments : true
categories : 
    - C++
---
### 오늘은 재귀적 기법을 이용해 c++로 하노이 탑 알고리즘을 구현해봤다.<br>

```c++
#include <iostream>
using namespace std;

void Hanoi(int n, char from, char tmp, char to)
{
	if (n == 1)
		cout << "Disk" << n << " move from " << from << " to " << to << endl;
	else
	{
		Hanoi(n - 1, from, to, tmp); // from에서 to로 이동
		cout << "Disk" << n << " move from " << from << " to " << to << endl;
		Hanoi(n - 1, tmp, from, to); // tmp에서 to로 이동
	}
}

int main()
{
    int n;
    cout << "원반의 수를 입력하시오 : ";
    cin >> n;
	Hanoi(n, 'A', 'B', 'C');
}
```