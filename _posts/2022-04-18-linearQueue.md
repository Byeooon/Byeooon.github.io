---
date : 2022-04-18
title : "[Data Structure] Linear Queue"
comments : true
categories : 
    - Data Structure
---

```c
#include <stdlib.h>
#include <stdio.h>
#define SIZE 100

typedef struct 
{
    int front;
    int rear;
    int data[SIZE];
}Queuetype;

void init(Queuetype *Q)
{
    Q->front = -1;
    Q->rear = -1;
}

int isFull(Queuetype *Q)
{
    if(Q->data[Q->rear] == SIZE - 1)
    {
        printf("isFull!\n");
        return 1;
    }
    else
        return 0;
}

int isEmpty(Queuetype *Q)
{
    if(Q->data[Q->front] == - 1 && Q->data[Q->rear] == - 1)
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
        printf("dqueue : %d\n",(Q->data[++Q->front]));
        return 0;
    }
}

void print(Queuetype *Q)
{
    for(int i = Q->front+1; i <= Q->rear; i++)
    {
        printf("current front : %d\n", Q->front);
        printf("%d\n", Q->data[i]);
    }
}

int main()
{
    Queuetype Q;
    init(&Q);

    enqueue(&Q, 0);
    enqueue(&Q, 5);
    enqueue(&Q, 1);
    enqueue(&Q, 9);

    dequeue(&Q);
    dequeue(&Q);

    print(&Q);

    return 0;
}

```