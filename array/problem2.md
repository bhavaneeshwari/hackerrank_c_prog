<img width="833" height="836" alt="image" src="https://github.com/user-attachments/assets/71580983-903a-4a23-9e2f-1f1b92532024" />

``c
#include <stdio.h>
#include <stdlib.h>

int main()
{
    int num, *arr, i;
    scanf("%d", &num);
    arr = (int*) malloc(num * sizeof(int));
    for(i = 0; i < num; i++) {
        scanf("%d", arr + i);
    }

    int start =0;
    int end = num-1;
    int temp;
    
    while (start< num/2)
    {  
        temp = arr[start];
        arr[start] = arr[end];
        arr[end]  = temp;
        start++;
        end--;
    }
    /* Write the logic to reverse the array. */

    for(i = 0; i < num; i++)
        printf("%d ", *(arr + i));
    return 0;
}


``
