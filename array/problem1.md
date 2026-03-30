<img width="808" height="718" alt="image" src="https://github.com/user-attachments/assets/9890e36e-b9d2-4413-b930-ab5249e167ab" />

``c

#include <stdio.h>
#include <string.h>
#include <math.h>
#include <stdlib.h>

int main() {

    int n;
    int sum=0;
    
      scanf("%d\n",&n);
    int *arr = (int*)malloc(n*sizeof(int));
  for (int i =0; i<n;i++)
  {
    scanf ("%d ", &arr[i]);
    
  }
  
  for (int j =0;j<n;j++) 
  {
    sum += arr[j];
  } 
  printf("%d",sum);
    return 0;
}
``
