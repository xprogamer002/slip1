Header File : doublylist.h
#include<stdio.h>
#include<stdlib.h>
struct node
{
 struct node *prev;
 int data;
 struct node *next;
};
struct node *f;
void create()
{
 int n,i;
 struct node *s;
 printf("enter number of nodes needed : ");
 scanf("%d",&n);
 f=(struct node *)malloc(sizeof(struct node));
 printf("enter data : ");
 scanf("%d",&f->data);
 f->prev=NULL;
 s=f;
 for(i=1;i<n;i++)
 {
 s->next=(struct node *)malloc(sizeof(struct node));  s=s->next;
 printf("enter data :");
 scanf("%d",&s->data);
 }
 s->next= NULL;
}
void display()
{
 struct node *s;
 for(s=f;s!=NULL;s=s->next)
 {
 printf(" %d -> ",s->data);
 }
} 

#include <stdio.h>
#include "doublylist.h"
int main()
{ int ch;
 do
 {
 printf("\n1.create\n2.display\n0.exit");
 printf("enter choice :");
 scanf("%d",&ch);
 switch (ch)
 {
 case 1: create();
 break;
 case 2: display();
 break;
 case 0: break;
 default:
 default:printf("invalid choice ");
 break;
 }
 }while(ch!=0);
} 

