# labtask-08

## PROBLEM:05
Write a C program for character pattern
A
B C
D E F
G H I J

```c
#include <stdio.h>

int main(void){
    int i,j;
    char alphabet;
    alphabet = 'A';
    for(i=1; i<=4; i++){
       
        for(j=1; j<=i; j++){
            printf(" %c", alphabet);
            alphabet++;
        }
        printf("\n");
    }
}
```
