<img width="744" height="614" alt="image" src="https://github.com/user-attachments/assets/87d9501d-f939-4c62-9c49-0e660ed59277" />
```c
#include <stdio.h>
#include <string.h>
#include <math.h>
#include <stdlib.h>

int main() {
	
    int n;
    scanf("%d", &n);
    int sum =0;
    //Complete the code to calculate the sum of the five digits on n.
    for (int i=0;i<5;i++)
    {
       sum += (n%10);
        n =n/10;
    }
    printf("%d",sum);
    return 0;
}
```
