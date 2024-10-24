# Ex5_Rail_Fence

## AIM:

To develop a simple C program to implement Rail Fence Cipher.

## DESIGN STEPS:

### Step 1:

Design of Rail Fence Cipher algorithnm 

### Step 2:

Implementation using C or pyhton code

### Step 3:

Testing algorithm with different key values. 
ALGORITHM DESCRIPTION:
In the rail fence cipher, the plaintext is written downwards and diagonally on successive "rails" of an imaginary fence, then moving up when we reach the bottom rail. When we reach the top rail, the message is written downwards again until the whole plaintext is written out. The message is then read off in rows.

## PROGRAM:
```C
#include<stdio.h>
#include<string.h>
void main()
{
        int i,j,k,l;
        char a[50],c[50],d[50];
        printf("\n\t\t RAIL FENCE TECHNIQUE");
        printf("\n\nEnter the input string : ");
        scanf("%[^\n]s",a);
        l=strlen(a);

        for(i=0,j=0;i<l;i++){
                if(i%2==0)
                        c[j++]=a[i];
        }
        for(i=0;i<l;i++){
                if(i%2==1)
                        c[j++]=a[i];
        }
        c[j]='\0';
        printf("\n\nCipher text after applying rail fence :");
        printf(" %s",c);

        if(l%2==0)
                k=l/2;
        else
                k=(l/2)+1;
        for(i=0,j=0;i<k;i++){
                d[j]=c[i];
                j=j+2;
        }
        for(i=k,j=1;i<l;i++){
                d[j]=c[i];
                j=j+2;
        }
        d[l]='\0';
        printf("\n\nText after decryption : ");
        printf("%s",d);
}
```
## OUTPUT:
![Railfenceoutputimage](Railfenceoutput.png)
## RESULT:
Thus the Rail Fence Encryption and Decryption successfully implemented using c program .