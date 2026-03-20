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


 "the code doesn't work without the scanf("\n")s", and that's partly true. After reading a string with %s, there's a \n still on the input stream. So the next %[^\n] is prematurely satisfied by that stray \n. So your call to scanf("\n") is one way to strip it. (But you didn't need to call scanf("\n") between the %c and the %s.)

As an aside, rather than calling scanf("\n"), I believe it would have been cleaner to just add a leading space to the following %[…] specifier: scanf(" %[^\n]%*c", sen);.

(Also you don't necessarily need that %*c out at the end. I know what it's for, but I'd say you don't or shouldn't need it. More on this below.)

