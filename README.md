#include <stdio.h>
#define MAX_SIZE 10

int stack[MAX_SIZE];
int top = -1;

void push(int value) {
    if (top == MAX_SIZE - 1) {
        printf("Stack Overflow - Cannot push element, stack is full.\n");
    } else {
        top++;
        stack[top] = value;
        printf("Pushed %d onto the stack.\n", value);
    }
}

void pop() {
    if (top == -1) {
        printf("Stack Underflow - Cannot pop element, stack is empty.\n");
    } else {
        printf("Popped %d from the stack.\n", stack[top]);
        top--;
    }
}

int main() {
    push(5);
    push(10);
    push(15);

    pop();
    pop();
    pop();
    pop(); // Trying to pop from an empty stack

    return 0;
}

