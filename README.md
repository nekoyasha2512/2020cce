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


#第02週
##進階題：大小寫轉換
```C
	#include <stdio.h>
int main()
{

	char c;
	while(scanf("%c", &c)==1)
	{
		if(c>='A' && c<='Z')
		{
			c+=32;
			printf("%c", c);
		}
		else if(c>='a' && c<='z')
		{
			c-=32;
			printf("%c", c);
		}
		else
		{
			printf("%c", c);
		}
	}
}
```
##進階題：漸增數列相加
```C
#include <stdio.h>
int main()
{

	int n, x=0;
	scanf("%d", &n);
	for(int i=n; i>=2; i--)
	{
		x=x+i*(i-1);
	}
	printf("%d\n", x);

}
```
##進階題：計算陣列的平方值 
```C
#include <stdio.h>
int main()
{

	int n, a[10];
	scanf("%d", &n);
	for(int i=1; i<=n; i++)
	{ scanf("%d", &a[i]); }
	
	for(int i=1; i<=n; i++)
	{
		printf("%d,", a[i]*a[i]);
	}
	printf("\n");
}
```
##進階題：2進位轉10進位
```C
#include <stdio.h>
int main()
{

	int n, x=0, m=1;
	scanf("%d", &n);
	for(int i=1; i<=4; i++)
	{
		x+=n%10*m;
		n/=10;
		m*=2;
	}
	printf("%d\n", x);

}
```
##基礎題：計算幾週與幾天 
```C
#include <stdio.h>
int main()
{

	int n;
	scanf("%d", &n);
	printf("%d %d\n", n/7, n%7);

}
```
##基礎題：計程車資計算 
```C
#include <stdio.h>
int main()
{

	int n, x=100;
	scanf("%d", &n);
	x+=(n-2000)/500*5;
	if(n%500!=0){ x+=5; }
	printf("%d\n", x);

}
```
##基礎題：兩數間可被5整除的整數
```C
#include <stdio.h>
int main()
{

	int a, b;
	scanf("%d%d", &a, &b);
	if(b<a){ int t=a; a=b; b=t; }
	while(a%5!=0)
	{ a+=1; }
	while(a<=b)
	{
		printf("%d\n", a);
		a+=5;
	}
	
}
```
##基礎題：整數間最大距離
```C
#include <stdio.h>
int main()
{

	int a, b, c, t;
	scanf("%d%d%d", &a, &b, &c);
	if(a>b){ t=a; a=b; b=t; }
	if(a>c){ t=a; a=c; c=t; }
	if(b>c){ t=b; b=c; c=t; }
	printf("%d\n", c-a);

}
```
