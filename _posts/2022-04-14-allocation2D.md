---
date : 2022-04-14
title : "[C++] 동적할당을 이용한 2차원 배열"
comments : true
categories : 
    - C++
---


```c++
#include <iostream>
#include <cstdlib>

using namespace std;

int **makeArray2D(int *sz);
void destroyArray2D(int **arr, int *sz);

int **makeArray2D(int *sz)
{
    int n1 = sz[0], n2 = sz[1];
    int **arr = new int *[n1];
    for(int i=0; i<n1; i++)
        arr[i] = new int[n2];
    return arr;
}

void destroyArray2D(int **arr, int *sz)
{
  int n1 = sz[0];
  for (int i=0; i < n1; i++)
    delete[] arr[i];
    delete[] arr;
}

int main(int argc, char *argv[])
{
  if(argc < 3)
  {
    cout << "usage : ./str 1d 2d 3d ... nd \n";
    return -1;
  }

  int i,dim = argc - 1;
  int *size = new int[dim];

  for(i = 1; i < argc; i ++) size[i-1] = atoi(argv[i]);

  int **arr2d = NULL;

  arr2d = makeArray2D(size);
  for(int i=0; i < size[0]; i++)
    for(int j=0; j < size[1]; j++) arr2d[i][j] = i*size[1]+j;
  for(int i=0; i < size[0]; i++)
  {
    for(int j=0; j < size[1]; j++) cout << arr2d[i][j] << ' ';
    cout << endl;
  }
  destroyArray2D(arr2d, size);
  return 0;
}
```