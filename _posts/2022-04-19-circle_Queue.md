---
date : 2022-04-19
title : "[Data Structure] Circle Queue"
comments : true
categories : 
    - Data Structure
---


```c++
#include <stdlib.h>
#include <stdio.h>
#define SIZE 6

typedef struct 
{
    int front;
    int rear;
    int data[SIZE];
}Queuetype;

void init(Queuetype *Q)
{
    Q->front = 0;
    Q->rear = 0;
}

int isFull(Queuetype *Q)
{
    if(Q->front == (Q->rear+1)%SIZE)
    {
        printf("isFull!\n");
        return 1;
    }
    else
        return 0;
}

int isEmpty(Queuetype *Q)
{
    if(Q->front == Q->rear)
    {
        printf("isEmpty!\n");
        return 1;
    }
    else
        return 0;
}

int enqueue(Queuetype *Q, int e)
{
    if(isFull(Q))
        return -1;
    else
        {
            Q->data[++Q->rear] = e;
            return 0;
        }
}

int dequeue(Queuetype *Q)
{
    if(isEmpty(Q))
        return -1;
    else
    {
        printf("dequeue : %d\n",Q->data[++Q->front]);
        return 0;
    }
}

void print(Queuetype *Q)
{
    for(int i = Q->front; i <= Q->rear; i++)
    {
        printf("%d\n", Q->data[i]);
    }
}

int main()
{
    Queuetype Q;
    init(&Q);

    enqueue(&Q, 0);
    enqueue(&Q, 1);
    enqueue(&Q, 2);
    enqueue(&Q, 3);
    enqueue(&Q, 4);
    enqueue(&Q, 5);
    
    dequeue(&Q);
    dequeue(&Q);

    enqueue(&Q, 6);
    

    print(&Q);

}
```