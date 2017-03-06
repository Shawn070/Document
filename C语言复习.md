```C
/*********if*********/
#include<stdio.h>
void main(void)
{
   int x, y;
   printf("请输入x：");
   scanf("%d", &x);
   if(x >= 0)
   {
      if(x > 0)
         y = 1;
      else
         y = 0;
   }
   else
      y = -1;
   printf("y = %d\n x = %d\n",y,x);
}
```

```c
/*********switch*********/
#include<stdio.h>
void main(void)
{
   int a;
   scanf("%d",&a);
   switch(a)
   {
      case 0:
      case 1:
         printf("Monday\n");break;
      case 2:
         printf("Tuesday\n");break;
      .
      .
      .
      default:
         printf("Error\n");
   }
}
```

```c
/*********while*********/
#include<stdio.h>
void main(void)
{
   int i, sum=0;
   i = 1;
   while(i <= 100)
   {
      sum = sum + i;
      i++;
   }
   printf("1+2+3+...+100=%d\n",sum);
}
```

```c
/*********do-while*********/
{
   do{
      sum += i;
      i++;
   }while(i <= 100)
   printf("1+2+3+...+100=%d\n",sum);
}
```

```c
/*********for*********/
#include<stdio.h>
void main(void)
{
   int i, sum;
   sum = 0;
   for(i = 1; i <= 100; i++)
   {
      sum += i;
   }
   printf("1+2+3+...+100=%d\n",sum);
}
```
