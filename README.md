# labtask-07

## PROBLEM:01
Take an array of 12 employee IDs. Write a program that checks if a given employee ID exists in the array or not.

```c
#include <stdio.h>
int main(void){
    int array[12];
    int i, existingID;

    for(i=0; i<12; i++){
        printf("Enter element %d: ", i+1);
        scanf("%d", &array[i]);
    }

    printf("Enter your id: ", existingID);
    scanf("%d", &existingID);

    for(i=0; i<12; i++){
        if(array[i] == existingID){
            printf("ID exists in an array\n");
            break;
        }
    }
    return 0;
}
```

## PROBLEM:02
A teacher has marks of 10 students stored in an array. Write a program to calculate the average marks.(Take input from user as an array).

```c
#include <stdio.h>
int main(void){
    int studentMarks[10];
    int i, average, sum =0;

    for(i=0; i<10; i++){
        printf("Enter marks %d: ", i+1);
        scanf("%d", &studentMarks[i]);
        sum += studentMarks[i];
    }

    average = sum/10;
    printf("Average marks: %d\n", average);

    return 0;

}
```

## PROBLEM:03
Take an array from user that stores the ages of 8 participants. Write a program to find the youngest participant’s age.

```c
#include <stdio.h>

int main(void){
    int age[8];
    int i, min;
    for(i=0; i<8; i++){
        printf("Enter age %d: ", i+1);
        scanf("%d", &age[i]);
    }
    min = age[0];
    for(i=1; i<8; i++){
        if(age[i]<min){
            min = age[i];
        }       
    }
    printf("Youngest age is %d", min);
}
```

## PROBLEM:04
You have an array of 6 numbers. Write a program to shift all elements one position to the right, moving the last element to the first position.

```c
#include <stdio.h>
int main(void){
    int array[6];
    int i, last;

    for(i=0; i<6; i++){
        printf("Enter element %d: ",i+1);
        scanf("%d", &array[i]);
    }
    last = array[5];
    for(i=5; i>=0; i--){
        array[i+1] = array[i];
    }
    array[0] = last;

    printf("Modified array is:");
    for(i=0; i<6; i++){
        printf("%d\t", array[i]); 
    }
    return 0;
}
```

## PROBLEM:05
An array contains 12 numbers. Write a program to remove all occurrences of a given number and shift remaining elements left. For example user enters 1 , 2 , 4 , 5 , 7 ,7 , 7 ,8,9,10,10,11 as an array want to remove 7 than the output will be 1 , 2 ,4,5, 8, 9 , 10, 10,11.

```c
#include <stdio.h>
int main(void){
    int array[12];
    int i, f, index, value;
    for(i=0; i<12; i++){
        printf("Enter element %d: ", i+1);
        scanf("%d", &array[i]);
    }

    printf("What element do you want to remove?: ");
    scanf("%d", &value);
    index = 11;
    for(i=0; i<=index; i++){
        if(array[i] == value){
            for(f=i+1; f<=index; f++)
                array[f-1] = array[f];

            i--;
            index--;
        }
    }
    printf("Modified array:");
    for(i=0; i<=index; i++){
        printf("%d\t", array[i]);
    }
    return 0;
}
```

## PROBELM:06
You have an array of 10 integers representing daily profit/loss. Write a program to sum only the positive values.

```c
#include <stdio.h>
int main(void){
    int array[10];
    int sum = 0, i;

    for(i=0; i<10; i++){
        printf("Enter an integer %d: ", i+1);
        scanf("%d", &array[i]);
    }

    for(i=0; i<10; i++){
        if(array[i] > 0){
            sum += array[i];
        }
    }
    printf("Sum of positive integer is: %d", sum);
}
```

## PROBLEM:07
A user enters a text containing letters, digits, spaces, and special characters. You want to create a program that extracts only the digits from the input and stores them in an array. Then, calculate the sum of all extracted digits and display it.

```c
    int n;
    printf("Enter how many characters you want to input: ");
    scanf("%d", &n);
    char array[n];
  
    int i, sum =0, digits = 0;
    printf("Enter character: ");

    for(i=0; i<n; i++){
        scanf(" %c", &array[i]);
    }
    for(i=0; i<n; i++){ 
        if(array[i] >= '0' && array[i] <= '9'){
            digits += 1;
        }
    }
    int arr[digits]; 
    int j = 0;
    for(i=0; i<n; i++){
        if(array[i] >= 48  && array[i] <= 57){
            arr[j] = array[i] - 48;
            j++;
        }
    }    
    for(i=0; i<digits; i++){
        sum += arr[i];
}
    printf("Sum of digits is: %d", sum);
}
```

## PROBLEM:08
An array stores 10 numbers. Write a program to check whether the array is sorted in ascending order.

```c
#include <stdio.h>
int main(void){
    int array[10];
    int i;

    for(i=0; i<10; i++){
        printf("Enter element %d: ", i+1);
        scanf("%d", &array[i]);
    }
    for(i=0; i<9; i++){
        if(array[i] > array[i+1]){
            printf("Array is not sorted in ascending order\n");
            return 0;
        }
    }
    printf("Array is sorted in ascending order\n");
    
}
```























    
