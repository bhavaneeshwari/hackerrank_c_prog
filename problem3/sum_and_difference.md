
## sum and difference
Print the sum and difference of both integers separated by a space on the first line, and the sum and difference of both float (scaled to  decimal place) separated by a space on the second line.
```c
#include <stdio.h>
#include <string.h>
#include <math.h>
#include <stdlib.h>

int main()
{
	int a,b;
    float c,d;
    scanf("%d %d",&a,&b);
    printf("%d %d\n",(a+b),(a-b));
    scanf("%f %f",&c,&d);
  
    printf("%.1f %.1f\n",(c+d),(c-d));
    return 0;
}

```

The tricky part here is to format the output of the floats such that the variable is rounded to one decimal place. This can be done like this: printf("%.1f", a). Here the .1 in the format specifier, specifies that the variable should be rounded down to 1 decimal place
