#include<stdio.h>
#define max 50
void insertion_sort(int a[],int  n);
int main()
{
    int a[max],i,n;
    printf("How many elements?");
    scanf("%d",&n);
    printf("Enter array elements:\n");
    for(i=0;i<n;i++)
    {
        scanf("%d",&a[i]);
    }
    insertion_sort(a,n);
}
void insertion_sort(int a[],int n)
{
    int i,j,temp;
    for (i=1;i<n;i++)
    {
        temp = a[ i ];    
        j = i;
        while(  j > 0  && temp < a[ j -1])
        {
            a[ j ] =a[ j-1];   
                j= j - 1;
        }
        a[j]=temp;
    }
    for(i=0;i<n;i++)
        printf("%d\t",a[i]);
}
OUTPUT:
How many elements?5
Enter array elements:
6
8
2
4
9
2	4	6	8	9	
    
