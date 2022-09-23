# Numbers in Malayalam words
This fun C Programming project gives the input number in malayalam words.
Uses switch cases only for logic implementation. We can serve the same purpose with structures and pointers.

```C
#include<stdio.h>
#include<string.h>
int main()
{
    int n,n_cpy,ones,tens,hundreds;
    char ones_word[50],tens_word[50],hundreds_word[50];

    printf("Enter a number between 0-999: ");
    scanf("%d",&n);
    n_cpy = n;
    for(int i=0;i<3;i++)
    {
        int res = n%10;
        switch (i)
        {
        case 0:
            ones = res;
            break;
        case 1:
            tens = res;
            break;
        case 2:
            hundreds = res;
            break;
        }
        n = n/10;
    }
    switch (ones)
    {
    case 1:
        strcpy(ones_word,"onn");
        break;
    case 2:
        strcpy(ones_word,"rand");
        break;
    case 3:
        strcpy(ones_word,"moonnu");
        break;
    case 4:
        strcpy(ones_word,"naalu");
        break;
    case 5:
        strcpy(ones_word,"anch");
        break;
    case 6:
        strcpy(ones_word,"aar");
        break;
    case 7:
        strcpy(ones_word,"ezh");
        break;
    case 8:
        strcpy(ones_word,"ett");
        break;
    case 9:
        strcpy(ones_word,"ompath");
        break;
    }

    switch (tens)
    {
    case 1:
        strcpy(tens_word,"pathin");
        break;
    case 2:
        strcpy(tens_word,"irupathi");
        break;
    case 3:
        strcpy(tens_word,"muppathi");
        break;
    case 4:
        strcpy(tens_word,"naalppathi");
        break;
    case 5:
        strcpy(tens_word,"ampathi");
        break;
    case 6:
        strcpy(tens_word,"arupathi");
        break;
    case 7:
        strcpy(tens_word,"ezhupathi");
        break;
    case 8:
        strcpy(tens_word,"empathi");
        break;
    case 9:
        strcpy(tens_word,"thonnutti");
        break;
    }

    switch (hundreds)
    {
    case 1:
        strcpy(hundreds_word,"Nootti");
        break;
    case 2:
        strcpy(hundreds_word,"Irunnootti");
        break;
    case 3:
        strcpy(hundreds_word,"Munnutti");
        break;
    case 4:
        strcpy(hundreds_word,"Naanootti");
        break;
    case 5:
        strcpy(hundreds_word,"Anjootti");
        break;
    case 6:
        strcpy(hundreds_word,"Arunnootti");
        break;
    case 7:
        strcpy(hundreds_word,"Ezhunnootti");
        break;
    case 8:
        strcpy(hundreds_word,"Ennuutti");
        break;
    case 9:
        strcpy(hundreds_word,"Thollayirathi");
        break;
    }

    printf("Entered number: %d \nIn Malayalam words: %s %s %s",n_cpy,hundreds_word,tens_word,ones_word);
}
```
