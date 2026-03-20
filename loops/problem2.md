<img width="717" height="685" alt="image" src="https://github.com/user-attachments/assets/bcbb155d-31f6-4dab-b654-0bd76b2a7d2a" />
```c

#include <stdio.h>
#include <string.h>
#include <math.h>
#include <stdlib.h>

int print (int num)
{
    if(num<=9) 
    {
      if (num ==1)   printf("one\n");
      else if (num ==2)   printf("two\n");
       else if (num ==3)   printf("three\n");
        else if (num ==4)   printf("four\n");
         else if (num ==5)   printf("five\n");
          else if (num ==6)   printf("six\n");
           else if (num ==7)   printf("seven\n");
            else if (num ==8)   printf("eight\n");
             else if (num ==9)   printf("nine\n");
    }
    else if (num>9)
    {
        if(num%2 ==0) printf("even\n");
        else printf("odd\n");
    }
    return 0;
}

int main() 
{
    int a, b;
    scanf("%d\n%d", &a, &b);
  	// Complete the code.
    for(int i =a;i<=b;i++)
    {
        print(i);
    }
    return 0;
}

```
