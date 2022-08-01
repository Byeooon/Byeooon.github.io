---
date : 2022-04-09
title : "[Algorithm] 달팽이 배열 응용"
comments : true
categories : 
    - Algorithm
---

###### 일반적인 형태의 배열을 달팽이 배열의 순서로 탐색하면서 입력받은 정수 a번째부터 b번째까지 존재하는 숫자들을 출력하는 문제입니다.

```c++
#include <iostream>
#define SIZE 1000
using namespace std;

int arr[SIZE];
int result[SIZE][SIZE];


int num; //배열 크기
int seed_num = 1; //배열의 시작값
int x = 0; //배열 위치
int y = -1; //배열 위치 //y부터 증가되기 때문에 -1로 초기값을 설정한다
int cnt; //전역변수로 선언한 num을 대체하여 출력에 사용될 임시변수

int tmp = 1;
int sum = 0;
int element;

int a; //시작 인덱스
int b; //끝 인덱스

int main()
{
    cout << "달팽이 배열의 크기를 입력하시오 : ";
    cin >> num;
    cout << "시작값 : ";
    cin >> a;
    cout << "끝값 : ";
    cin >> b;

    cnt = num;

    for(int i = 0; i < num ; i++)
    {
        for(int j = 0; j < num; j++)
        {
            result[i][j] = tmp++;
            cout << result[i][j] << " ";
        }
        cout << endl;   //일반 배열 선언
    }
    
    //=====================================//
    
    while(num > 0)
    {
        for(int i = 0; i < num; i++)
        {
            element = result[x][++y];
            arr[sum++] = element;
        }

        num--;

        for(int i = 0; i < num; i++)
        {
            element = result[++x][y];
            arr[sum++] = element;
        }

        num--;

        for(int i = 0; i < num + 1; i++)
        {
            element = result[x][--y];
            arr[sum++] = element;
        }

        for(int i = 0; i < num; i++)
        {
            element = result[--x][y];
            arr[sum++] = element;
        }
    }

    for(int i = a; i < b+1; i++)
    {
        cout << "Result : ";
        cout << arr[i] << " " << endl;
    }

    return 0;
}

```