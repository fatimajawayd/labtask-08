# labtask-08

## PROBLEM:01
Write a C program to find the union of two arrays.
Union means combining all unique elements from both arrays (no duplicates).
Input:
Array 1: 1 2 3 4
Array 2: 3 4 5 6
Output:
Union: 1 2 3 4 5 6

```c
#include <stdio.h>
int main(void){
    int array1[] = {1,2,3,4};
    int array2[] = {3,4,5,6};
    int i,j,k = 0;
    int array3[8];

    for(i=0; i<4; i++){
        array3[k++] = array1[i];
    }
    for(i=0; i<4; i++){
        for(j=0; j<k; j++){
            if(array2[i] == array3[j]) break;
        }
        if(j == k){
            array3[k++] = array2[i];
        }
    }
    for(i=0; i<6; i++){
        printf("%d", array3[i]);
    }
    return 0;
}
```

## PROBLEM:02
Write a C program to find the intersection of two arrays. Intersection means elements that are common in both arrays.

```c
#include <stdio.h>
int main(void){
    int array1[] = {1,2,3,4};
    int array2[] = {3,4,5,6};
    int i,j,k = 0;
    int array3[8];
    for(i=0; i<4; i++){
        for(j=0; j<4; j++){
            if(array1[i] == array2[j]){
                break;
            }
        }
        if(j != 4){
            array3[k++] = array1[i];
        }
    }
    for(i=0; i<k;i++){
        printf("%d", array3[i]);
    }
}
```

## PROBLEM:03
Write a program to count how many elements are common between two arrays.

```c
  int array1[] = {1,2,3,4};
    int array2[] = {3,4,5,6};
    int i,j,count = 0;

    for(i=0; i<4; i++){
        for(j=0; j<4; j++){
            if(array1[i] == array2[j]){
                break;
            }
        }
        if(j != 4){
            count++;
        }
    }
    printf("Number of common elements: %d", count);
}
```




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


