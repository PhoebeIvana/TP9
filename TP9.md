# Tugas Pendahuluan 9
```bash
Nama    : [Kaera Yukio || CHANGE ME]
NPM     : [2306839344 || CHANGE ME]
```
---
## Soal Teori
1. Apa yang dimaksud dengan Queue dan Stack dalam konteks Programming? Apa fungsinya? dan Jelaskan cara kerja dari Stack dan Queue!
2. Operasi apa sajakah yang dapat dilakukan oleh Queue dan Stack? Sebutkan dan jelaskan!
3. Berikanlah contoh real-world case dari penggunaan Stack dan Queue dan berikan juga visualisasi dari kedua contoh tersebut
4. Buatlah program untuk kedua contoh diatas! 

## Soal Lanjutan
## 5. Reverse String 
Diberikan sebuah string, kalian diminta membuat program menggunakan stack untuk membalikkan urutan string tersebut. Jelaskan perbedaan antara algoritma kalian dengan jawaban dari AI. Apa saja yang membuat satu solusi lebih efisien daripada yang lain?

## 6. Balancing Parentheses
Diberikan expression: ((a+b)*(c-d)). Sekarang, tugas kalian adalah menuliskan program untuk memeriksa apakah tanda kurung dalam expression tsb. seimbang/tidak dengan menggunakan stack. Kemudian, bandingkan algoritma kalian dengan jawaban dari AI. Yang mana yang lebih cepat? yang mana yang lebih efisien? Jelaskan perbedaan logika di antara keduanya!

## 7. Infix to Postfix Conversion 
Kalian diminta untuk membuat program yang mengubah ekspresi infix menjadi postfix dengan menggunakan stack. Pastikan program yang dibentuk sudah benar, kemudian bandingkan cara handling operator dan operand yang kalian lakukan dengan yang dilakukan oleh AI. Apakah handling operator dengan prioritas tinggi (i.e. *, /) untuk kedua program (kalian + AI) sudah sesuai dengan yang seharusnya? Jelaskan!

## 8. Case Study
Pada soal ini, program menggunakan array untuk mengimplementasikan Stack dan Queue. Kalian diminta untuk melengkapi beberapa function agar dapat melakukan operasi dasar pada Stack dan Queue, i.e. Push + Pop untuk Stack, dan Enqueue + Dequeue untuk Queue.
```c
#include <stdio.h>
#include <stdlib.h>
#define MAX_SIZE 100

typedef struct {
    int data[MAX_SIZE];
    int top;
} Stack;

typedef struct {
    int data[MAX_SIZE];
    int front;
    int rear;
} Queue;

// Prototype
void initStack(Stack *s);
int isStackFull(Stack *s);
int isStackEmpty(Stack *s);
void push(Stack *s, int value); 
int pop(Stack *s);              
void initQueue(Queue *q);
int isQueueFull(Queue *q);
int isQueueEmpty(Queue *q);
void enqueue(Queue *q, int value); 
int dequeue(Queue *q);             
void printStack(Stack *s);
void printQueue(Queue *q);


void push(Stack *s, int value) {
    // TODO 1: Lengkapin functionnya ya
}

int pop(Stack *s) {
    // TODO 2: Lengkapin functionnya ya
    return -1;
}

void enqueue(Queue *q, int value) {
    // TODO 3: Lengkapin functionnya ya
}

int dequeue(Queue *q) {
    // TODO 4: Lengkapin functionnya ya
    return -1;
}

void initStack(Stack *s) {
    s->top = -1;
}

int isStackFull(Stack *s) {
    return s->top == MAX_SIZE - 1;
}

int isStackEmpty(Stack *s) {
    return s->top == -1;
}

void initQueue(Queue *q) {
    q->front = 0;
    q->rear = -1;
}

int isQueueFull(Queue *q) {
    return q->rear == MAX_SIZE - 1;
}

int isQueueEmpty(Queue *q) {
    return q->rear < q->front;
}

void printStack(Stack *s) {
    if (isStackEmpty(s)) {
        printf("Stack is empty.\n");
        return;
    }
    for (int i = 0; i <= s->top; i++) {
        printf("%d ", s->data[i]);
    }
    printf("\n");
}

void printQueue(Queue *q) {
    if (isQueueEmpty(q)) {
        printf("Queue is empty.\n");
        return;
    }
    for (int i = q->front; i <= q->rear; i++) {
        printf("%d ", q->data[i]);
    }
    printf("\n");
}

int main() {
    Stack stack;
    Queue queue;

    initStack(&stack);
    initQueue(&queue);

    push(&stack, 10); 
    push(&stack, 20);
    printf("Stack after pushing 10 and 20:\n");
    printStack(&stack);

    int poppedValue = pop(&stack); 
    printf("Popped value: %d\n", poppedValue);
    printStack(&stack);

    enqueue(&queue, 30); 
    enqueue(&queue, 40);
    printf("Queue after enqueuing 30 and 40:\n");
    printQueue(&queue);

    int dequeuedValue = dequeue(&queue); 
    printf("Dequeued value: %d\n", dequeuedValue);
    printQueue(&queue);

    return 0;
}
```
Silakan jelaskan logika kalian untuk membuat masing-masing function di atas. Tanyakan juga kepada AI apakah logika kalian benar? Silakan jelaskan.

