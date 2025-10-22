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

## PROBLEM:04
Temperature Record System A city records temperatures for 7 days in 3 different shifts (morning, afternoon, night). Store this data in a 2D array [7][3] and: Display the temperature table. Find the average temperature for each day.

```c
#include <stdio.h>
int main(void){
    int temp[7][3];
    int i,j;
    float avg;
    int sum;

    for(i=0;i<7;i++){
        for(j=0;j<3;j++){
            if(j==0){
                printf("Enter morning temperature of day %d: ", i+1);
                scanf("%d", &temp[i][j]);
            }
            else if(j==1){
                printf("Enter afternoon temperature of day %d: ", i+1);
                scanf("%d", &temp[i][j]);
            }
            else{
                printf("enter night temperature of day %d: ", i+1);
                scanf("%d", &temp[i][j]);
            }
        }
    }
    printf("\nTEMPERATURE RECORD\n");
    printf("DAY\tMORNING\tAFTERNOON\tNIGHT\n");
    for(i=0; i<7; i++){
        printf("%d\t",i+1); 
        for(j=0; j<3; j++){
            printf("%d\t", temp[i][j]);
        }
        printf("\n");
    }
    printf("\nDAILY AVERAGES:\n");
    for(i=0; i<7; i++){
        sum = temp[i][0] + temp[i][1] + temp[i][2];
        avg = sum / 3.0;
        printf("Day %d Average: %.2f\n", i+1, avg);
    }
    return 0;
}
```

## PROBELM:05
A school has 5 students and 3 subjects. marks[5][3] = { {80, 75, 90}, {60, 70, 65}, {78, 82, 88}, {92, 85, 89}, {55, 60, 58} }; Store the marks in a 2D array [5][3]. Find:  Total marks of each student.  Average marks of each subject.

```c





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


