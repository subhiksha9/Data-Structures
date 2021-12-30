#include<stdio.h>
#include<stdlib.h>
int hash(int value)
{
    return value%10;
}
void insert(int arr[10],int value)
{   
    int key = hash(value);
    int flag=0,j;
    if(arr[key] == -1)
    {   
        arr[key] = value;
        printf("%d inserted at arr[%d]\n", value,key);
        flag=1;
    }
    else
    {   
        printf("Collision : arr[%d] has element %d already!\n",key,arr[key]);
        for(j=key+1;j<10;j++)
        {
            if(arr[j]==-1)
            {
                arr[j]=value;
                flag=1;
                break;
            }
        }
        for(j=0;j<key&&flag==0;j++)
        {
            if(arr[j]==-1)
            {
                arr[j]=value;
                flag=1;
                break;
            }
        }
    }
    if(flag==0)
    {
        printf("Unable to insert %d\n",value);
    }
}
void del(int arr[10],int value)
{
    int key = hash(value);
    int flag=0,j;
    if(arr[key] == value)
    {
        arr[key] = -1;
        flag=1;
    }
    else
    {
        for(j=key+1;j<10;j++)
        {
            if(arr[j]==value)
            {
                arr[j]=-1;
                flag=1;
                break;
            }
        }
        for(j=0;j<key&&flag==0;j++)
        {
            if(arr[j]==value)
            {
                arr[j]=-1;
                flag=1;
                break;
            }
        }
    }
    if(flag==1)
    {
        printf("Element %d Found to delete\n",value);
    }
    else
    {
     printf("Element %d not Found to delete\n",value);   
    }
}
void search(int arr[10],int value)
{
    int key =hash(value);
    int flag=0,j;
    if(arr[key] == value)
    {
        flag=1;
    }
    else
    {
        for(j=key+1;j<10;j++)
        {
            if(arr[j]==value)
            {
                flag=1;
                break;
            }
        }
        for(j=0;j<key&&flag==0;j++)
        {
            if(arr[j]==value)
            {
                flag=1;
                break;
            }
        }
    }
    if(flag==1)
    {
        printf("Element %d Found\n",value);
    }
    else
    {
     printf("Element %d not Found\n",value);   
    }
}
void display(int arr[10])
{
    int i;
    printf("displaying those elements\n");
    for(i = 0; i < 10; i++)
        printf("arr[%d] = %d\n",i,arr[i]);
}
void main()
{
    int ch,size,arr[10],value,key;
    for(key=0;key<10;key++)
    {
        arr[key]=-1;
    }
    while(1)
    {
        printf("\n1.Insert\n2.Search\n3.Delete\n4.Display\n5.Exit\n");
        printf("Enter choice\n");
        scanf("%d",&ch);
        switch(ch)
        {
            case 1:printf("Enter the element to insert:");
                   scanf("%d",&value);
                   insert(arr,value);
                   break;
            case 2:printf("Enter the element to search: ");
                   scanf("%d",&value);
                   search(arr,value);
                   break;
            case 3:printf("Enter the element to delete: ");
                   scanf("%d",&value);
                   del(arr,value);
                   break;
            case 4:display(arr);
                   break;
            case 5:exit(0);
                   break;
                   
        }
    }
    
}

OUTPUT:
1.Insert
2.Search
3.Delete
4.Display
5.Exit
Enter choice
1
Enter the element to insert:1
17 inserted at arr[7]

1.Insert
2.Search
3.Delete
4.Display
5.Exit
Enter choice
1
Enter the element to insert:9
9 inserted at arr[9]

1.Insert
2.Search
3.Delete
4.Display
5.Exit
Enter choice
1
Enter the element to insert:26 3
23 inserted at arr[3]

1.Insert
2.Search
3.Delete
4.Display
5.Exit
Enter choice
1
Enter the element to insert:5
5 inserted at arr[5]

1.Insert
2.Search
3.Delete
4.Display
5.Exit
Enter choice
1
Enter the element to insert:31
31 inserted at arr[1]

1.Insert
2.Search
3.Delete
4.Display
5.Exit
Enter choice
1
Enter the element to insert:20
20 inserted at arr[0]

1.Insert
2.Search
3.Delete
4.Display
5.Exit
Enter choice
2
Enter the element to search: 9
Element 9 Found

1.Insert
2.Search
3.Delete
4.Display
5.Exit
Enter choice
4
displaying those elements
arr[0] = 20
arr[1] = 31
arr[2] = -1
arr[3] = 23
arr[4] = -1
arr[5] = 5
arr[6] = -1
arr[7] = 17
arr[8] = -1
arr[9] = 9

1.Insert
2.Search
3.Delete
4.Display
5.Exit
Enter choice
1
Enter the element to insert:7
Collision : arr[7] has element 17 already!

1.Insert
2.Search
3.Delete
4.Display
5.Exit
Enter choice
2
displaying those elements
arr[0] = 20
arr[1] = 31
arr[2] = -1
arr[3] = 23
arr[4] = -1
arr[5] = 5
arr[6] = -1
arr[7] = 17
arr[8] = 7
arr[9] = 9

1.Insert
2.Search
3.Delete
4.Display
5.Exit
Enter choice
2
Enter the element to search: 0
Element 0 not Found

1.Insert
2.Search
3.Delete
4.Display
5.Exit
Enter choice
2
Enter the element to search: 7
Element 7 Found

1.Insert
2.Search
3.Delete
4.Display
5.Exit
Enter choice
3
Enter the element to delete: 23
Element 23 Found to delete

1.Insert
2.Search
3.Delete
4.Display
5.Exit
Enter choice
3
Enter the element to delete: 1
Element 1 not Found to delete

1.Insert
2.Search
3.Delete
4.Display
5.Exit
Enter choice
5
