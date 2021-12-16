#include<stdio.h>
struct node
{
    int ele;
    struct node *next;
};
void main()
{
    struct node *A,*B,*C;
    A=(struct node*) malloc(sizeof(struct node));
    B=(struct node*) malloc(sizeof(struct node));
    C=(struct node*) malloc(sizeof(struct node));
    scanf("%d%d%d",&A->ele,&B->ele,&C->ele);
    A->next=B;
    B->next=C;
    C->next=NULL;
    printf("Value at A is %d",A->ele);
    printf("Value at B is %d",B->ele);
    printf("Value at B is %d",A->next->ele);
    printf("Value at C is %d",C->ele);
    printf("Value at C is %d",B->next->ele);
    printf("Value at C is %d",A->next->next->ele);  
    printf("Address of A=%u",A);
    printf("Address of B=%u",B);
    printf("Address of B=%u",A->next);
    printf("Address of C=%u",C);
    printf("Address of C=%u",B->next);
    printf("Address of C=%u",A->next->next);
    
}
