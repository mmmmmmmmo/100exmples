```c
#include<stdio.h>
#include<stdlib.h>
int main()
{
    void choose(int (*array)[],int n);
    int i,a[3];
    int (*p)[3];
    *p=a;
    for(i=0;i<3;i++)
        scanf("%d",&a[i]);
    choose(p,3);
    for(i=0;i<3;i++)
    {
        printf("%d ",a[i]);
    }
    return 0;
}
void fun_luoxuanjuzheng(int (*a)[4][4])
{

    int n=4;
    int b,i,j;
    int m=1;
    for(b=0;2*(b+1)<=n;b++)
    {
        for(j=b;j<n-b;j++)
        {
           (*a)[i][j]=m++;
        }
        for(i;i<n-b;i++)
        {
            (*a)[i][j]=m++;
        }
        for(j;j>=b;j--)
        {
            (*a)[i][j]=m++;
        }
        for(i;i>=b;i--)
        {
            (*a)[i][j]=m++;
        }
    }
}
void choose(int (*array)[],int n)
{
    int i,j,k,t;
    for(i=0;i<n-1;i++)
    {
        k=i;
        for(j=i+1;j<n;j++)
        {
            if(*array[j]<*array[k])
                k=j;
            t=*array[k];
            *array[k]=array[i;
            *array[i]=t;
        }
    }
}
