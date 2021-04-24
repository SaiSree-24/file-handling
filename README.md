# file-handling
created by saisree

#include<stdio.h>
int main()
{
    FILE*fp;
    char ch;
    int i,pos;
    fp=fopen("input.txt","r");
    if(fp==NULL)
    {
        printf("My Captain");
    }
    fseek(fp,0,SEEK_END);
    pos=ftell(fp);
    //printf("Curren position is %d\n",pos);
    i=0;
    while(i<pos)
    {
        i++;
        fseek(fp,-i,SEEK_END);
        //printf("%c",fgetc(fp));
        ch=fgetc(fp);
        printf("%c",ch);
    }
    return 0;
}
