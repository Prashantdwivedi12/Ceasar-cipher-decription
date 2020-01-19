# Ceasar-cipher-decription
SOurce code:

#include <stdio.h>
#include <stdlib.h>
#include <ctype.h>
int main()
{
   int i , k;
   int len;
   char result[100]="";
   char str[100];
   printf("enter the cipher text:=");
   gets(str);

   printf("enter the key:=");
   scanf("%d",&k);
   len=strlen(str);
       for(i=0;i<len;i++)
       {
           if(isupper(str[i]))
           result[i]+=((((int)str[i]-k+26)-65)%26)+65;

           else
            result[i]+=(((((int)str[i]-k)+26)-97)%26)+97;
       }


   printf("\plain text is %s",result);
   return 0;
}
