<img width="918" height="742" alt="image" src="https://github.com/user-attachments/assets/1c993740-7580-4e2a-9115-8f09fb8c4ddb" />
<img width="923" height="618" alt="image" src="https://github.com/user-attachments/assets/9e6e35e6-858f-4892-a83e-c6e69989110b" />

```c
#include <stdio.h>
#include <stdlib.h>

/*
 * This stores the total number of books in each shelf.
 */
int* total_number_of_books;

/*
 * This stores the total number of pages in each book of each shelf.
 * The rows represent the shelves and the columns represent the books.
 */
int** total_number_of_pages;

int main()
{
    int total_number_of_shelves;
    scanf("%d", &total_number_of_shelves);
    
    total_number_of_books = (int*)calloc(total_number_of_shelves,sizeof(int));/*firstly its 1d array since tnb is pointer to array itself , we typecast int*, then this array holds the number of book in each shelf*/
    total_number_of_pages  = (int**)calloc(total_number_of_shelves,sizeof(int*));/*2d array here rows are shelf, which is pointer to shelf so we have int* in sizeof operator , then int** bcz of 2d array, here we didnt care about column part, which represents the book, which may be vary*/
    
    int total_number_of_queries;
    scanf("%d", &total_number_of_queries);
    
    while (total_number_of_queries--) {
        int type_of_query;
        scanf("%d", &type_of_query);
        
        if (type_of_query == 1) {
            /*
             * Process the query of first type here.
             */
            int x, y;
            scanf("%d %d", &x, &y);
            total_number_of_books[x]++; /* here book count incr as we gonna add thats our query 1 in shelf x */
            total_number_of_pages[x]= (int*)realloc(total_number_of_pages[x],total_number_of_books[x]*sizeof(int));
            /* here we update the row(shelf) size , based on no of book in book array*/
            total_number_of_pages[x][total_number_of_books[x]-1]=y; 
        } else if (type_of_query == 2) {
            int x, y;
            scanf("%d %d", &x, &y);
            printf("%d\n", *(*(total_number_of_pages + x) + y));
        } else {
            int x;
            scanf("%d", &x);
            printf("%d\n", *(total_number_of_books + x));
        }
    }

    if (total_number_of_books) {
        free(total_number_of_books);
    }
    
    for (int i = 0; i < total_number_of_shelves; i++) {
        if (*(total_number_of_pages + i)) {
            free(*(total_number_of_pages + i));
        }
    }
    
    if (total_number_of_pages) {
        free(total_number_of_pages);
    }
    
    return 0;
}

```
