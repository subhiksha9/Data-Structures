#include<stdio.h>
#include<stdlib.h>
struct circularlist
{
    int data;
    struct circularlist *next;
};
typedef struct circularlist node;
node *create(node *first)
{
    node *new,*prev;
    int x;
    printf("enter a value(enter -1 to stop)\n");
    scanf("%d",&x);
    while(x!=-1)
    {
        new=(node *)malloc(sizeof(node));
        new->data=x;
        new->next=NULL;
        if(first==NULL)
        {
            first=new;
            prev=new;
        }
        else
        {
            prev->next=new;
            prev=new;
        }
        printf("enter a value(enter -1 to stop)\n");
        scanf("%d",&x);
        prev->next=first;
    }
    return first;
}
void display (node *first)
{
    node *temp=first;
    node *k=first;
    if(first==NULL)
    {
        printf("No list is found\n");
    }
    else
    {
        printf("%d->",temp->data);
        while (temp->next!=k)
        {
            temp=temp->next;
            printf("%d->",temp->data);
        }
    }
}
int count(node *first)
{
    int c=0;
    node *temp=first;
    node *k=first;
    while(temp->next!=k)
    {
        c++;
        temp=temp->next;
    }
    return c+1;
}
void search(node *first,int f)
{
    node *temp=first;
    node *k=first;
    int flag=0;
    while(temp->next!=k)
    {
        if(temp->data==f)
        {
            flag=1;
            break;
        }
        temp=temp->next;
    }
    if(flag==1)
        printf("%d Element is found\n",f);
    else
        printf("%d Element is not found\n",f);
}
node *insert_at_begin(node *first,int x)
{
    node *new,*k,*temp;
    temp=first;
    k=first;
    new=(node *)malloc(sizeof(node));
    new->data=x;
    new->next=NULL;
    if(first==NULL)
    {
        first=new;
    }
    else
    {
        while(temp->next!=k)
        {
           temp=temp->next; 
        }
        temp->next=new;
        new->next=first;
        first=new;
    }
    return first;
}
node *insert_at_end(node *first,int x)
{
    node *temp=first,*new;
    node *k=first;
    new=(node *)malloc(sizeof(node));
    new->data=x;
    new->next=NULL;
    if(first==NULL)
    {
        first=new;
    }
    else
    {
        while(temp->next!=k)
        {
            temp=temp->next;
        }
        temp->next=new;
        new->next=first;
    }
    return first;
}
node *insert_at_pos(node *first,int x,int pos)
{
    node *new,*temp=first;
    new=(node *)malloc(sizeof(node));
    new->data=x;
    new->next=NULL;
    for(int i=1;i<pos-1;i++)
    {
        temp=temp->next;
    }
    new->next=temp->next;
    temp->next=new;
    return first;
}
node *begin_delete(node *first)
{
    node *temp,*k;
    temp=first;
    k=first;
    while (temp->next!=k)
    {
        temp=temp->next;
    }
    temp->next=first->next;
    first=k->next;
    return first;
}
node *random_delete(node *first,int pos)
{
    int i;
    node *temp=first;
    node *k,*l;
    for (i=0;i<pos-1;i++)
    {
        k=temp;
        temp=temp->next;
        l=temp->next;
    }
    k->next=l;
    free(temp);
    return first;
}
void main()
{
    node *head=NULL;
    int ch,pos,c;
    int x,f;
    printf("Menu Driven\n1.Create\n2.Display\n3.Count\n4.Search\n5.insert at beginning\n6.insert at ending\n7.insert at postion\n8.Delete\n9.Random Delete\n10.Exit\n");
    while(1)
    {
        printf("Enter your choice\n");
        scanf("%d",&ch);
        switch(ch)
        {
            case 1:head=create(head);
                   break;
            case 2:display(head);
                   break;
            case 3:c=count(head);
                   printf("number of nodes is %d\n",c);
                   break;
            case 4:printf("enter f: ");
                   scanf("%d",&f);
                   search(head,f);
                   break;
            case 5:printf("enter x: ");
                   scanf("%d",&x);
                   head=insert_at_begin(head,x);
                   break;
            case 6:printf("enter x: ");
                   scanf("%d",&x);
                   head=insert_at_end(head,x);
                   break;
            case 7:printf("enter x,pos: ");
                   scanf("%d%d",&x,&pos);
                   head=insert_at_pos(head,x,pos);
                   break;
            case 8:head=begin_delete(head);
                   break;
            case 9:printf("enter the postion: ");
                   scanf("%d",&pos);
                   head=random_delete(head,pos);
                   break;
            case 10:exit(0);
                   
        }
    }
}
