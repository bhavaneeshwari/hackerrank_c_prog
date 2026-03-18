
##  print Hello,World! on a single line, and then print the already provided input string to stdout.
```c
#include <stdio.h>
#include <string.h>
#include <math.h>
#include <stdlib.h>

int main() 
{
   
    char s[100];
    scanf("%[^\n]%*c", s);
    printf("Hello, World!\n");
    printf("%s", s);

    return 0;
}
```
## scanf("%[^\n]%*c", s); wondering whats the format specifer of scanf is 
means that all the characters entered as the input, including the spaces, until we hit the enter button are stored in the variable, name; provided we allocate sufficient memory for the variable.
If we input something like ‘Welcome to Programming’, then we see that the output for this code would be as following:

**Hello, World!**

**Welcome to Programming**

However if we were to replace the statement

***scanf("%[^\n]%*c", s);***

with

***scanf(“%s”, &s);***

we observe that the output would be as following:

**Hello, World!**

**Welcome**

So, the input is only accepted until we hit the spacebar and is processed.

If replaced with

**scanf(“%c”, &s);**

we observe that the output would be as following:

**Hello, World!**

**W**

So, the input is accepted is only a single character and then the output gets printed.

Hope, this helps.
