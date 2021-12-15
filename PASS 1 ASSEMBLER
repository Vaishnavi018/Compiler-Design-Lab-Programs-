#include<stdio.h>
#include<conio.h>
#include<stdlib.h>
void main()
{
FILE *f1,*f2;
char ch,str[30],str1[10],str2[30],cstr[15];
int i,j,num,q,r;

printf("Enter your assembly instructions\n");
f1=fopen("asin","w");
while(1)
{ ch=getchar();
if(ch=='*')
break;
fputc(ch,f1);
}
fclose(f1);
f1=fopen("asin","r");
f2=fopen("asout","w");
while(1)
{
fgets(str,25,f1);
strncpy(str1,str,3);
str1[3]='\0';
j=0;
for(i=3;i<strlen(str);i++)
{
str2[j]=str[i];
j++;
}

str2[j]='\0';
if((strcmp(str1,"lda"))==0)
{
fputs("3a\t",f2);
fputs(str2,f2);
} else if((strcmp(str1,"mov"))==0)
{
fputs("47\n",f2);
} else if((strcmp(str1,"add"))==0)
{
fputs("80\n",f2);
} else if((strcmp(str1,"sub"))==0)
{
fputs("90\n",f2);
} else if((strcmp(str1,"hlt"))==0)
{
fputs("76\n",f2);
break;
} else if((strcmp(str1,"sta"))==0)
{
fputs("32\t",f2);
num=atoi(str2);
q=num/100;
r=num%100;
if(r==0)
fputs("00\t",f2);
else
fputs(itoa(r,cstr,10),f2);
fputs("\t",f2);
fputs(itoa(q,cstr,10),f2);
fputs("\n",f2);
} else
{
fputs("error\n",f2);
}}
fclose(f1);
fclose(f2);
f2=fopen("asout","r");
printf("\nTHE OBJECT CODE CONTENTS\n");
ch=fgetc(f2);
while(ch!=EOF)
{
putchar(ch);
ch=fgetc(f2);
}
fclose(f2);
getch();

}
