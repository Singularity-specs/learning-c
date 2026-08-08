#include <stdio.h>

int add(int a, int b);
int subtract(int a, int b);
int multiply(int a, int b);
int divide(int a, int b);
int calculate(int a, int b, char operation);

int main() {
    
    int a, b;
    char operation;
    scanf("%d %d %c", &a, &b, &operation);
    
    if (operation == '/' && b == 0) {
        printf("Invalid input\n");
    } else {
        int result = calculate(a, b  operation);
    printf("%d\n", result);
    return 0;
    }
}


int add(int a, int b) {
    return a + b;
}

int subtract(int a, int b) {
    return a - b;
}

int multiply(int a, int b) {
    return a * b;
}

int divide(int a, int b) {
    if (b != 0) {
        return a / b;
    }
    return 0;
}

int calculate(int a, int b, char operation) {
    if (operation == '+') {
        return add(a, b);
    } else if (operation == '-') {
        return subtract(a, b);
    } else if (operation == '*') {
        return multiply(a, b);
    } else if (operation == '/') {
        return divide(a, b);
    }
    return 0;
}
