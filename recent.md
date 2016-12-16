```c
void main()
{
    fun_45(8,11);
}
void fun_43(int a,int m,int b,int n)
{
    printf("%d/%d\n",a*n>b*m?b:a,a*n>b*m?n:m);
}
void printb(int x,int n)
{
    if(n>0)
    {
        printf("%d",(unsigned)(x&(1<<(n-1)))>>(n-1));
        printb(x,n-1);
    }
}
int fun_42(int a,int b)
{
    int max=a>b?a:b;
    int min=a+b-max;
    int p;
    if(!max%min)
    {
        return min;
    }
    else{return (fun_42(min,max%min));}
}
void fun_45(int a,int b)
{
    int i;
    double m=a/b;
    while (m){
    i=2;
    while (m-1.0/i<=0)
    {
        i++;
    }
    printf("1/%d\t",i);
    m-=1.0/i;}
}
//抓交通肇事犯

voidfun_18()
{
    int x,y,c;
    double b,d,e;
    for(x=7;x<10;y++)
    {
        b=x*1000+x+y*10+y;
        c=sqrt(b);
        e=c;
        d=sqrt(b);
        if(y!=x&&e==d)
        {
            c=b;
            printf("%d\t",c);

        }
    }
}
//打鱼还是晒网\

void fun_9(int nian,int yue,int ri)
{
    int day[12]={31,30,31,30,31,30,31,31,30,31,30,31};
    int sum=0,a=1990,b=0,i,m;
    while(a<=nian)
    {
        sum+=b;
        if((nian%4==0&&nian%100!=0)||nian%400==0)
            nian=366;
        else nian=365;
        a++;
    }
    for(i=0;i<yue-1;i++)
    {
        sum=sum+day[i];
    }
    if(yue>2&&b==366)
    {
        sum+=1;
    }
    sum+=ri;
    m=sum%5;
    if(m>=4||m==0)
    {
        printf("晒网\n");
    }
    else{printf("打鱼\n");}
}
//杨辉三角
void fun_10()
{
    int a[6][6];
    int m=6;
    int i,j;
    for(i=0;j<m;j++)
    {
        for(j=0;j<i;j++)
        {
            a[i][j]=a[i-1][j-1]+a[i][j-1];
        }
    }
    for(i=0;i<m;i++)
    {
        printf("%d\t",a[i][j]);
    }
    printf("\n");
}
void fun_m()
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
                    printf("%d\t%d\t%d\n",i,j,k);
            }
        }
    }
}
```
