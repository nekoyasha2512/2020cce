# 2020cce

#第01週
##進階題：分式化簡
```C
include <stdio.h>
int main()
{

	int a, b, c, x, y;
	scanf("%d%d",&a ,&b);
	x=a; y=b;
	while( b!=0 )
	{
		c=b;
		b=a%b;
		a=c;
	}
	x/=a;
	y/=a;
	printf("%d %d\n", x, y);

}
```
##第二題 進階題：讀入整數反序列印
```C
#include <stdio.h>
int main()
{

	int a[10]={};
	for(int i=0; i<10; i++)
	{
		scanf("%d", &a[i]);
	}
	for(int i=9; i>=0; i--)
	{
		if(a[i]!=0)
		{ printf("%d ", a[i]); }
	}
	printf("\n");

}
```
##第三題 進階題：A的B次方函數
```C
#include <stdio.h>
int MYPOWER(int a, int b, int x=1)
{

	for(int i=1; i<=b; i++)
	{
		x=x*a;
	}
	return x;

}
int main(void)
{
	int a,b;
	scanf("%d%d",&a,&b);
	printf("[%d]",MYPOWER(a,b));
	return 0;
}
```
##第四題 進階題：漸增數列相加
```C
#include <stdio.h>
int main()
{

	int n, x=0;
	scanf("%d", &n);
	for(int i=n-1; i>0; i--)
	{
		x+=n*i;
		n--;
	}
	printf("%d\n", x);
	
}
```
##第五題 基礎題：找零錢 
```C
#include <stdio.h>
int main()
{

	int n, x, y, z;
	scanf("%d", &n);
	x=n/50;
	y=n%50/5;
	z=n%5;
	printf("%d=50*%d+5*%d+1*%d\n", n, x, y, z);

}
```
##第六題 基礎題：因數個數
```C
#include <stdio.h>
int main()
{

	int n, x=0;
	scanf("%d", &n);
	for(int i=1; i<=n; i++)
	{
		if(n%i==0){ x++; }
	}
	printf("%d\n", x);

}
```
##第七題 基礎題：找倍數 
```C
#include <stdio.h>
int main()
{
	
	int a[10], x=0;
	for(int i=1; i<=10; i++)
	{ scanf("%d", &a[i]); }
	for(int i=1; i<=10; i++)
	{
		if(a[i]%3==0){ x++; }
	}
	printf("%d\n", x);
	
}
```
##第八題 基礎題：整數轉換為等級
```C
#include <stdio.h>
int main()
{

	int n;
	scanf("%d", &n);
	if(n>=90){ printf("A\n"); }
	else if(n<90&&n>=80){ printf("B\n"); }
	else if(n<80&&n>=60){ printf("C\n"); }
	else if(n<=60){ printf("F\n"); }

}
```
