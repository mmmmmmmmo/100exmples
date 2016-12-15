```c
#include<stdio.h>
#include<math.h>
/*18.有限5位数

个位数为6且能被3整除的五位数共有多少？*/
 void fun_18()
 {
     int a=10000,i;
     int sum=0;
     for(i=0;i<=9000;i++)
     {
         a=a+i*10+6;
         if((a/10000+a/1000+(a%100-3)/10+(a%1000-a%100)/100+(a%10000-a%1000)/1000)%3==0)
         {
             sum++;
         }
     }
     printf("%d",sum);
 }
/*19. 8 除不尽的数

一个自然数被8除余1，所得的商被8除也余1，再将第二次的商被8除后余7，最

后得到一个商为a。又知这个自然数被17除余4，所得的商被17除余15，最后得到一

个商是a的2倍。求这个自然数。*/
void fun_19()
{
    int i;
   for(i=1;i>0;i++)
    {
        if(((i*8+7)*8+1)*8+1==(34*i+15)*17+4)
        {printf("%d\n",(34*i+15)*17+4);

        break;}
    }
}

/*20.一个奇异的三位数

一个自然数的七进制表达式是一个三位数，而这个自然数的九进制表示也是一

个三位数，且这两个三位数的数码正好相反，求这个三位数。 */
void fun_20()
{


    int a=999;
    int c,k;
    int d;int m,n,l,o;
    do
    {
        c=(a/100)*pow(7,2)+((a%100)/10)*pow(7,1)+(a%10)*pow(7,0);

        m=c/pow(9,3);
        if(m>=1)
        {
              a--;
              continue;

        }
        else{
        n=c/pow(9,2);
        l=(c-pow(9,2)*n)/9;
        o=c-n*pow(9,2)-l*pow(9,1);
        k=n+l*10+o*100;

                   if(a==k)
           {
               printf("%d\n",a);
           }
           a--;}


    }while(a>=100);

}

/*21.4位反序数



设N是一个四位数，它的9倍恰好是其反序数，求N。反序数就是将整数的数字倒

过来形成的整数。例如：1234的反序数是4321。*/
void fun_21()
{
    int i;
    for(i=1000;i<10000;i++)
    {
        if(i*9==i%1000*1000+(i%100)/10*100+(i%10)/100*10+i/1000)
        {
            printf("%d\n",i);
        }

    }
}
/*22.求车速



一辆以固定速度行驶的汽车，司机在上午10点看到里程表上的读数是一个对称

数(即这个数从左向右读和从右向左读是完全一样的)，为95859。两小时后里程表上

出现了一个新的对称数。问该车的速度是多少？新的对称数是多少？*/
void fun_22()
{
    int a,b=0;
    for(a=95859;a<100000;a++)
    {
        if((a/10000==a%10000)&&(a%1000/10==a%10/1000))
            {
                printf("%d",a);
                b++;
                 break;
            }


    }
    if(b==0)
    {
        for(;a<1000000;a++)
        {
            if((a/100000==a%100000)&&(a%10000/10==a%10/10000)&&a%100/1000==a%1000/100)
            {
                printf("%d",a);
                b++;
                break;
            }
        }
    }
    printf("\n%lf",a/2.0);
}
/*23.阿姆斯特朗数



如果一个正整数等于其各个数字的立方和，则称该数为阿姆斯特朗数(亦称为自

恋性数)。



如 407=43+03+73就是一个阿姆斯特朗数。试编程求1000以内的所有阿姆斯特朗数。*/


void fun_23()
{
    int a,b,c;
    int i,sum;
    for(a=1;a<1001;a++)
    {
        i=0,sum=0;
        b=a;
        while(b>0)
        {
            b=b/10;
            i++;
        }
        for(c=a;i>=0;i--)
        {
            sum+=pow(c/pow(10,i-1),3);
            c=c-c/pow(10,i-1)*pow(10,i-1);
        }

        if(sum==a)
        {
            printf("%d\n",a);
        }
    }
}
/*24.完全数

如果一个数恰好等于它的因子之和，则称该数为“完全数”。*/
void fun_24()
{
    int sum=0;
    int a,b;
    for(a=4;a<=100;a++)
    {
        for(b=2;b<=sqrt(a);b++)
        {
            if(a%b!=0)
                break;

        else{sum+=b;}}
        if(sum==a)
        {
            printf("%d\n",a);
        }

    }


}

/*26.亲密数



如果整数A的全部因子(包括1，不包括A本身)之和等于B；且整数B的全部因子(

包括1，不包括B本身)之和等于A，则将整数A和B称为亲密数。求3000以内的全部亲

密数。*/
void fun_26()
{
    int a,b,sum,m;
    for(a=1;a<=3000;a++)
    {
        for(b=2,sum=1;b<=a/2;b++)
        {
            if(a%b==0)
            {
                sum+=b;

            }
        }

        for(b=2,m=1;b<=sum/2;b++)
        {
            if(sum%b==0)
            {
                m+=b;
            }
        }
        if(m==a)
        {
            printf("%d:%d\n",a,sum);
        }
    }
}

/*27.自守数



自守数是指一个数的平方的尾数等于该数自身的自然数：*/
void fun_27()
{
    int k,kk,mul,ll,number;
    for(number=0;number<200000;number++)

    {

    for(mul=number,k=1;(mul/=10)>0;k*=10);

        kk=k*10;
        mul=0;
        ll=10;
        while(k>0)

    {
        mul=(mul+(number%(k*10))*(number%ll-number%(ll/10)))%kk;

        k/=10;
        ll*=10;

    }

    if(number==mul)

    printf("%ld ",number);

        }
}


/*28.回文数



打印所有不超过n(取n<256) 的其平方具有对称性质的数(也称回文数)。 */
void fun_28(int n)
{
    int m1,m2,m3,m4m5;
    int  a,b,i;
    int sum;
    int j;
    for(i=1;i<=n;i++)
    {
        b=a=i*i,sum=1;
        while (a/10!=0)
        {
            a=a/10;
            sum+=1;
        }
        for(j=sum-1;j>=(sum+1)/2;j--)
        {
            m1=pow(10,j);
            m2=pow(10,sum-j-1);
            m3=pow(10,sum-j);

            if(((b/m1)%10)!=((b%m3)/m2))
            break;
            else if(j==(sum+1)/2)
            {
                printf("%d:%d:%d\n",sum,i,i*i);
            }
        }
    }

}


//13.该存多少钱
/*假设银行一年整存零取的月息为0.63%。现在某人手中有一笔钱，
他打算在今后的五年中的年底取出1000元，到第五年时刚好取完，请算出他存钱时应存入多少。*/
int fun_13()
{
    int i;

    float total=0;

    for(i=0;i<5;i++)

    total=(total+1000)/(1+0.0063*12);

    return total;
}

void main()
{
    fun_28(256);
}


