//Dynamic-memory-allocation

#include <stdio.h>
#include <stdlib.h>
 
int main()
{
    int* ptr;
    int i, n;
    printf("Enter the number of input\n");
    scanf("%d", &n);
    ptr = (int*) malloc(n*sizeof(int));
 
    if(ptr == NULL)
    {
        printf("Memory is not allocated because it is full");
    }
    else{
        for(i=0;i<n;i++)
        {
            printf("Enter input-%d\n", i+1);
            scanf("%d", &ptr[i]);
        }
    }
    for(i=0;i<n;i++)
    {
        printf("Output-%d:\t%d\n", i+1, ptr[i]);
    }
 
    return 0;
}
