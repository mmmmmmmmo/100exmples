#include<stdio.h>
#include<math.h>
#include<stdlib.h>
void fun_mofang()
{
    int a[15][15],i,j,p,k,n;
    p=1;
    while(p==1)
    {
        scanf("%d",&n);
        if(((n%2)!=0)&&(n>0&&n<=15))
            p=0;
    }for(i=1;i<=n;i++)
    {
        for(j=1;j<=n;j++)
            a[i][j]=0;
    }
    j=n/2+1;
    a[1][j]=1;
    for(k=2;k<=n*n;k++)
    {
        i=i-1;
        j=j+1;
        if((i<1)&&(j>n))
        {
            i=i+2;
            j=j-1;
        }
        else{if(i<1)
            i=n;
            if(j>n)
                j=1;
        }
        if(a[i][j]=0)
            a[i][j]=k;
        else
        {
            i=i+2;
            j=j-1;
            a[j][j]=k;
        }
    }
    for(i=1;j<=n;j++)
    {
        printf("%3d",a[i][j]);
        printf("\n");
    }
    printf("\n");}
void fun_qiqushu()
{
	int n;
	for(n=1001;n<2000;n+=2)
	{
		printf("((%d*%d)-1)%8 = %d\n",n,n,(n*n-1)%8);
	}
}
void fun_yuanyin(char a[],char*b[])//复制元音字母
{
    int k,j=0;
    for(k=1;a[k]!=0;k++)
    {
        if(a[k]=='a'||a[k]=='A'||a[k]=='e'||a[k]=='E'||a[k]=='i'||a[k]=='I'||a[k]=='o'||a[k]=='O'||a[k]=='u'||a[k]=='U')
        {
            *b[j]=a[k];
            j++;
        }
        *b[j]='\n';
    }
}
void fun_lingxing(int m)
{
    int i,j;
    for(i=1;i<=2*m-1;i++)
    {
        for(j=1;j<=2*m-1;j++)
        {
            if(j==m-((m-fabs(m-i))-1)||j==m+((m-fabs(m-i))-1))
                printf("*");
            else{printf(" ");}
        }
        printf("\n");
    }
}
void fun_maopao(int *a[])//冒泡排序
{
    int i,j,k,t;
    int b=sizeof(a);
    for(i=0;i<b;i++)
    {
        for(j=0;j<b-1-i;j++){
        if(*a[j]<*a[j+1])
        {
            t=*a[j];
            *a[j]<*a[j+1];
            *a[j+1]=t;
        }}
    }
        for(i=0;i<=9;i++)
            printf("%d",a[i]);

}
