# C语言用来选择判断和循环的语句：
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
