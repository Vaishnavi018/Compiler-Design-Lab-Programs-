#include<stdio.h>
#include<conio.h>
#include<string.h>
struct opc
{
int len;
char mnemonic[10],code[3];
}opcode;
struct opd
{
int address;
char code[10];
}op;
struct source_result
{
int address;
char label[10],instr[10],operand[10];
}res;
struct res
{
int a;
char c[10];
}s;
void main()
{
FILE *r,*o,*result,*symb;
int i,j,found=0,l;
char s1[10];
clrscr();
r=fopen("re.txt","r");
o=fopen("opcode.txt","r");
result=fopen("output.txt","w");
symb=fopen("symbol.txt","r");
while(!feof(r))
{
fscanf(r,"%d%s%s%s",&res.address,&res.label,&res.instr,&res.operand);
rewind(o);
rewind(symb);
found = 0;
while(!feof(o))
{
fscanf(o,"%d%s%s",&opcode.len,&opcode.mnemonic,&opcode.code);
if(strcmp(res.instr,opcode.mnemonic)==0)
{
op.address=res.address;
strcpy(op.code,opcode.code);
fprintf(result,"%d\t%s",op.address,op.code);
found=1;
break;
}
}
if(found==0)
continue;
while(!feof(symb))
{
fscanf(symb,"%d%s",&s.a,&s.c);
if(strcmp(res.operand,s.c)==0)
{
fprintf(result,"%d\n",s.a);
break;
}
else if(strcmp(res.operand,"NULL")==0)
{
fprintf(result,"0000");
break;
}
else if(res.operand[0]=='#')
{
strcpy(s1,res.operand);
l=strlen(s1)-1;
for(i=4;i>l;i--)
fprintf(result,"0");
for(j=1;j<=l;j++)
fprintf(result,"%c",s1[j]);
fprintf(result,"\n");
break;
}
}
}
printf("Pass 2 completed!");
fcloseall();
getch();
}
