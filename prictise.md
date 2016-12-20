```c
void fun_84(int a)
{
	int b,c,d;
	b=a*a*a;
	for(d=0,c=0;c<a;c++)
	{
		d+=a*a-a+1+c*2;
		printf(c?"+%d":"%d",a*a-a+1+c*2);
	}
	if(d==b)
	printf("Y\n");
	else printf("N\n");
}
void fun_xioamingmaishu()
{ 
    int d[6],m,i,j; 
    long b[63],flag; 
    float c[6],min,x; 
    printf("Please enter the prices of 6 books:");
    for(i=0;i<6;i++) scanf("%f",&c[i]); 
    for(i=0,min=-1,d[0]=0;d[0]<2;d[0]++) 
    for(d[1]=0;d[1]<2;d[1]++) 
    {
        for(d[2]=0;d[2]<2;d[2]++)
        { 
            for(d[3]=0;d[3]<2;d[3]++)
            {  
                for(d[4]=0;d[4]<2;d[4]++) 
                {

                    for(d[5]=0;d[5]<2;d[5]++) 
                    { 
                        for(flag=0,x=0,j=5;j>=0;j--)
                        { 
                            x+=c[j]*d[j]; flag=flag*10+d[j];
 
                        }
                    }
                }
            }
        ] 
    x=((x-10>0)? x-10:10-x); 
    if(min<0) 
    { 
        min=x; 
        b[i++]=flag; 
    } 
    else if(min-x>1.e-6) 
    { 
        min=x; b[0]=
        flag; i=1; 
    } 
    else if(fabs((double)x-min)<1.e-6) 
        b[i++]=flag; 
    } 
    for(m=0;m<i;m++) 
    {    
        printf("10(+ -)%.2f=",min); 
        for(flag=b[m],j=0;flag>0;j++,flag/=10)
        {

        if(flag%10)  
        if(flag>1) 
        printf("%.2f+",c[j]); 
        }
    else printf("%.2f\n",c[j]); 

    }

