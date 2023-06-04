# C-p89-
C语言学习笔记 p89 分支与循环
#include<stdio,h>
#include<math.h>
//大小顺序排列
int main()
{
    int a=0;
    int b=0;
    int c=0;
    scanf("%d %d %d",&a&b&c);
    //算法实现
    //a放最大值，b次之，c放最小值
    if(a<b)
    {
        int tmp=a;
        a=b;
        b=tmp;
    }
    if(a<c)
    {
        int tmp=a;
        a=c;
        c=tmp;
    }
    if(b<c)
    {
        int tmp=b;
        b=c;
        c=tmp;
    }
    printf("%d %d %d\n",a,b,c);
    return 0;
}


//判断一个数是否是3的倍数
int main()
{
    int i=0;
    for(i=1;i<=100;i++)
    {
        if(i%3==0)
            printf("%d",i);
    }
    return 0;
}


//给两个数，求最大公约数
int main()
{
    int m=24;
    int n=18;
    scanf("%d %d",&m,&n);
    while(r=m%n)
    {
        m=n;
        n=r;
    }
    printf("%d\n",n);
    return 0;
}


//打印闰年
int main()
{
    int year=0;
    int count=0;
    for(year=1000;year<=2000;year++)
    {
        //判断year是否为闰年
        //能被4整除并且不能被100整除是闰年
        //能被400整除是闰年
        if(year%4==0&&year%100!=0)
        {
            printf("%d",year);
            count++;
        }
        else if(year%400==0)
        {
            printf("%d",year);
            count++;
        }
    }
    printf("count=%d\n",count);
    return 0;
}

//方法2
int main()
{
    int year=0;
    int count=0;
    for(year=1000;year<=2000;year++)
    {
      if(((year%4==0)&&(year%100!=0))||(year%400==0)
      {
          printf("%d",year);
      }
    }
    printf("count=%d\n",count);
    return 0;
}


//打印素数
int main()
{
    int i=0;
    int count=0;
    for(i=100;i<=200;i++)
    {
        //判断i是否为素数
        //素数判断规则
        //试除法
        //产生2-i-1的数字
        int j=0;
        for(j=2;j<i;j++)
        {
            if(i%j==0)
            {
                break;
            }
        }
        if(j==i)
        {
            printf("%d",i);
        }
    }
    printf("count=%d\n",count);
    return 0;
}

//素数求解2
int main()
{
    int i=0;
    int count=0;
    for(i=100;i<=200;i++)
    {
        int j=0;
        for(j=2;j<=sqrt(i);j++)
        {
            if(i%j==0)
            {
                break;
            }
        }
        if(j>sqrt(i))
        {
            count++;
            printf("%d",i);
        }
    }
    printf("count=%d\n",count);
    return 0;
}


int main()
{
    int i=0;
    int count=0;
    for(i=1;i<=100;i++)
    {
        if(i%10==9)
            count++;
        if(i/10==9)
            count++;
    }
    printf("count=%d\n",count);
    return 0;
}


//分数求和
int main()
{
    int i=0;
    double sum=0;
    int flag=1;
    for(i=1;i<=100;i++)
    {
        sum+=flag*1.0/i;
        flag=-flag;
    }
    printf("%lf\n",sum);
    return 0;
}


//求10个数的最大值
int main()
{
    int arr[10]={1,2,3,4,5,6,7,8,9,10};
    int max=arr[0];
    int i=0;
    int sz=sizeof(arr)/sizeof(arr[0]);
    for(i=1;i<sz;i++)
    {
        if(arr[i]>max)
        {
            max=arr[i];
        }
    }
    printf("max=%d\n",max);
    return 0;
}


//在屏幕上输出9*9乘法口诀表
int main()
{
    int i=0;
    for(i=1;i<=9;i++)
    {
        //打印一行
        int j=1;
        for(j=1;j<=i;j++)
        {
            printf("%d*%d=%2d",i,j,i*j);
        }
    }
    return 0;
}


//二分查找
int main()
{
    int arr[10]={1,2,3,4,5,6,7,8,9,10};
    int k=0;
    int left=0;
    int right=sizeof(arr)/sizeof(arr[0])-1;
    scanf(%d",&k);
    while(left<=right)
    {
        int mid=left+(right-left)/2;
        if(k<arr[mid])
        {
            right=mid-1;
        }
        else if(x>arr[mid])
        {
            left=mid+1;
        }
        else
        {
            printf("找到了，下标是%d\n",mid);
            break;
        
        }
    }
    if(right<left)
    {
        printf("没找到");
    }
    return 0;
}










