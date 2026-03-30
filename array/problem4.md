<img width="910" height="709" alt="image" src="https://github.com/user-attachments/assets/ef183916-e154-43e8-bd74-1dc60cb25fe1" />

```c
#include <stdio.h>
#include <string.h>
#include <math.h>
#include <stdlib.h>

int main() {

    /* Enter your code here. Read input from STDIN. Print output to STDOUT */    
  int freq[10]= {0}; 
  char s[1000];
  scanf("%s",s);
  for (int i =0; i<strlen(s); i++)
  {
    if(s[i]>=48 && s[i]<=57)
    freq[s[i]-48] ++;
    
  }
   for (int i =0;i<10;i++)
   {
    printf("%d ",freq[i]);
   }
    return 0;
}

```
