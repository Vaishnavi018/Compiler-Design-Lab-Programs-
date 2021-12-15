#include<stdio.h>
#include<conio.h>
#include<stdlib.h>
#include<string.h>
struct table
{
char var[10];
int value;
};
struct table tbl[20];
int i,j,n;
void create();
void modify();
int search(char variable[],int n);
void insert();
void display();
int main()
{
int ch,result=0;
char v[10];

do
{
printf("Enter ur choice:\n1.Create\n2.Insert\n3.Modify\n4.Search\n5.Display\n6.Exit");
scanf("%d",&ch);
switch(ch)
{
case 1:
create();
break;
case 2:
insert();
break;
case 3:
modify();
break;
case 4:
printf("Enter the variabe to be searched\n");
scanf("%s",&v);
result=search(v,n);
if(result==0)
printf("The variable does not belong to the table\n");
else
printf("The location of variable is %d. The value of %s is %d",
result,tbl[result].var,tbl[result].value);
break;
case 5:
display();
break;
case 6:
exit(1);
}
}
while(ch!=6);
getch();
return 0;
}
void create()
{
printf("Enter the number of entries\n");
scanf("%d",&n);
printf("Enter the variable and the value:\n");
for(i=1;i<=n;i++)
{
scanf("%s%d",tbl[i].var,&tbl[i].value);
check:
if(tbl[i].var[0]>='0' && tbl[i].var[0]<='9')
{
printf("The variable should start with an alphabet\nEnter the correct variable name\n");
scanf("%s%d",tbl[i].var,&tbl[i].value);
goto check;
}
check1:
for(j=1;j<1;j++)
{
if(strcmp(tbl[i].var,tbl[j].var)==0)
{
printf("The variable already exists.\nEnter another variable\n");
scanf("%s%d",tbl[i].var,&tbl[i].value);
goto check1;
}
}
}
printf("The table after creation is\n");
display();
}
void insert()
{
if(i>=20)
printf("Cannotinsert. Table is full");
else
{
n++;
printf("Enter the variable and value\n");
scanf("%s%d",tbl[n].var,&tbl[n].value);
check:
if(tbl[i].var[0]>='0' && tbl[i].var[0]<='9')
{
printf("The variable should start with alphabet\nEnter the correct variable name\n");
scanf("%s%d",tbl[i].var,&tbl[i].value);
goto check;
}
check1:
for(j=1;j<n;j++)
{
if(strcmp(tbl[j].var,tbl[i].var)==0)
{
printf("The variable already exist\nEnter another variable\n");
scanf("%s%d",tbl[i].var,&tbl[i].value);
goto check1;
}
}
printf("The table after insertion is\n");
display();
}
}
void modify()
{
char variable[10];
int result=0;
printf("Enter the variable to be modified\n");
scanf("%s",&variable);
result=search(variable,n);
if(result==0)
printf("%sdoes not belong to the table",variable);
else
{
printf("The current value of the variable%s is %d, Enter the new variable and its value",tbl[result].var,tbl[result].value);
scanf("%s%d",tbl[result].var,&tbl[result].value);
check:
if(tbl[i].var[0]>='0' && tbl[i].var[0] <= '9')
{
printf("The variable should start with alphabet\n Enter the correct variable name\n");
scanf("%s%d",tbl[i].var,&tbl[i].value);
goto check;
}
}
printf("The table after modification is\n");
display();
} int search(char variable[],int n)
{
int flag;
for(i=1;i<=n;i++)
{
if(strcmp(tbl[i].var,variable)==0)
{
flag=1;
break;
}
}
if(flag==1)
return i;
else
return 0;
}
void display()
{
printf("Variable\t value\n");
for(i=1;i<=n;i++)
printf("%s\t\t%d\n",tbl[i].var,tbl[i].value);

}
