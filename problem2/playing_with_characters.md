## playing with characters

First, take a character,  as input.
Then take the string,  as input.
Lastly, take the sentence  as input.

```c
#include <stdio.h>
#include <string.h>
#include <math.h>
#include <stdlib.h>

int main() 
{
char ch;
char s[40];
char sen[100];
scanf("%c", &ch);
scanf("%s",s);
scanf("\n");
scanf("%[^\n]%*c", sen);
printf("%c\n", ch);
printf("%s\n",s);
printf("%s\n",sen);
return 0;

    
   
}

```
The statement: scanf("%[^\n]%*c", s); will not work because the last statement will read a newline character, \n, from the previous line. This can be handled in a variety of ways. One way is to use scanf("\n"); before the last statement.



