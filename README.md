
# 100exmples
job asked by Mr Jin

```c
#include<stdio.h>
void fun()
{
  int i,j,k;
  printf("\n");
  for(i=1;i<5;i++)
    {
      for(j=1;j<5;j++)
        {
            for(k=1;k<5;k++)
              {
                if(i!=k&&i!=j&&j!=k)
                printf("%d%d%d\n"i,j,k);
                }
          }
      }
}
计算利率提成
double CarculateInterest(double a)
{
    double b=a,m;
    char c;
    double sum=0;
    if(a>100)
        c='5';
    else if(a>60&&a<=100)
        c='4';
    else if(a>40&&a<=60)
        c='3';
    else if(a>20&&a<=40)
        c='2';
    else if(a<=20&&a>10)
        c='1';
    else if(a<=10)
        c='0';
    switch (c)//计算利息
    {
        case'5':m=0.01*(b-100);b=100;sum+=m;
        case'4':m=0.015*(b-60);b=60;sum+=m;
        case'3':m=0.03*(b-40);b=40;sum+=m;
        case'2':m=0.05*(b-20);b=20;sum+=m;
        case'1':m=0.075*(b-10);b=10;sum+=m;
        case'0':m=0.1*b;sum+=m;
    }
    return (sum);
}
```
