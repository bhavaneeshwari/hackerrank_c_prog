<img width="806" height="821" alt="image" src="https://github.com/user-attachments/assets/703c7923-3bea-463b-8e6c-7dccef51a3d6" />

```c
#include <stdio.h>
#include <string.h>
#include <math.h>
#include <stdlib.h>

int main() {

    char *s;
    s = malloc(1024 * sizeof(char));
    scanf("%[^\n]", s);
    s = realloc(s, strlen(s) + 1);
    //Write your logic to print the tokens of the sentence here.
    char *tok ;
    tok = strtok(s," ");
    while (tok != NULL)
    {
        printf("%s\n",tok);
        tok= strtok(NULL," ");
    }
    return 0;
}

```
