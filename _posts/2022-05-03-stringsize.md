---
date : 2022-05-03
title : "[C++] <string> size function"
comments : true
categories :
    - C++
---
###### size() function을 이용하면 string의 길이를 알아낼 수 있다. 알고리즘 문제를 해결할 때 유용하게 사용할 수 있는 방법중 하나인 것 같다.
```c++
#include <iostream>
#include <string>
using namespace std;

int main() {

	string value = "abc";
	cout << value.size() << endl;

	return 0;
}
```