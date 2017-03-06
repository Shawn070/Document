### 基础语句
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

### 相关方法

```c
/*********分支与循环结构的应用-判断闰年*********/
#include<stdio.h>
void main(void)
{
   int year, leap;
   printf("Input year:");
   scanf("%d", &year);
   if(year%400 == 0 || ((year%4 == 0)&&(year%100 != 0)))
      leap = 1;
   else leap = 0;
   if(leap == 1)
      printf("%d is a leap year.\n",year);
   esle printf("%d is not a leap year.\n",year);
}
```

```c
/*********枚举法-求100~200间的素数*********/
#include<stdio.h>
#include<math.h>
void main(void)
{
   int m, k, i, n=0;
   for(m=101, m<200, m+=2)        /*循环枚举100~200之间的奇数*/
   {
      k=(int)sqrt((double)m);     /*求m的开平方→k*/
      for(i=2;i<=k;i++)           /*循环判断能否被2~k之间的所有数整除*/
      ｛
         if(m%i == 0)   break;    /*若能被整除则不是素数，跳出循环*/
      ｝
      if(i>k)                     /*若m均不能被小于k的数整除则为素数*/
      {
         printf("%5d", m);
         n++;
      }
   if(n%10 == 0)  printf("\n");   /*控制没行输出10个数*/
   }
   printf("\n");
}
```

```c
/*********迭代法-用辗转相除法求两个正整数的最大公约数*********/
#include<stdio.h>
void main(void)
{
   int m, n, q;
   printf("输入两个正整数：\n");
   scanf("%d,%d",&n,&m);
   do{                        /*开始迭代*/
      q = n%m;
      n = m;
      m = q;
   }while(q != 0);
   printf("最大公约数是：%d\n",n);
}
```

```c
/*********冒泡法*********/
#include<stdio.h>
void main(void)
{
   int a[10], i, j, temp;
   printf("输入10个数：\n");
   for(i=0; i<10; i++)
      scanf("%d", a[i]);      /*从键盘输入10个数*/
   for(i=0; i<9; i++)         /*i=0进行第一轮比较，i=1进行第二轮比较···共比较9轮*/
   {
      for(j=0; j<9-i; j++)    /*依次将相邻两数比较*/
         if(a[j] > a[j+1])    /*若大数在前，则交换两数位置*/
         {
            temp = a[j];
            a[j] = a[j+1];
            a[j+1] = temp;
         }
   }
   printf("排列后的数为：");
   for(i=0; i<10; i++)
      printf("%3d", a[i]);
   printf("\n");
}
```
