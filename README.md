##瘋狂程設第一週

#進階題：分式化簡 ADVANCE_002
```C
#include <stdio.h>
int main()
{
	int a , b;
	scanf("%d%d" , &a , &b);
	for(int i=a;i>=1;i--)
	{
		if(a%i==0 && b%i==0)
		{
			printf("%d %d\n" , a/i , b/i);
			break;
		}
	}
}
```

#進階題：讀入整數反序列印 ADVANCE_003
```C
#include <stdio.h>
int a[10];
int main()
{
	int n;
	for(int i=0;i<10;i++)
	{
		scanf("%d" , &n);
		if(n==0) break;
		else a[i]=n;
	}
	for(int i=9;i>=0;i--)
	{
		if(a[i]!=0)
			printf("%d " , a[i]);
	}
	printf("\n");
}
```

#進階題：A的B次方函數 ADVANCE_005_C
```C
#include <stdio.h>
int MYPOWER(int a , int b)
{ 	
	int ans=1;
	for(int i=0;i<b;i++)
	{
		ans*=a;
	}
	return ans;
}
int main(void)
{
	int a,b;
	scanf("%d%d",&a,&b);
	printf("[%d]",MYPOWER(a,b));
	return 0;
}
```

#進階題：漸增數列相加 ADVANCE_006
```C
#include <stdio.h>
int main()
{
	int n , ans=0;
	scanf("%d" , &n);
	for(int i=1;i<n;i++)
	{
		ans+=i*(i+1);
	}
	printf("%d\n" , ans);
}
```

#基礎題：找零錢 BASE_002
```C
#include <stdio.h>
int main()
{
	int a;
	scanf("%d" , &a);
	printf("%d=50*%d+5*%d+1*%d\n" , a , a/50 , a%50/5 , a%5);
}
```

#基礎題：因數個數 BASE_005
```C
#include <stdio.h>
int main()
{
	int a , ans=2;
	scanf("%d" , &a);
	for(int i=2;i<=5000;i++)
	{
		if(a%i==0)
		{
			ans+=1;
			if(a==i)
			{
				ans-=1;
			}
		}
	}
	printf("%d\n" , ans);
}
```

#基礎題：找倍數 BASE_010
```C
#include <stdio.h>
int main()
{
	int a , ans=0;
	while(scanf("%d" , &a)==1)
	{
		if(a%3==0)
		{
			ans+=1;
		}
	}
	printf("%d\n" , ans);
}
```

#基礎題：整數轉換為等級 BASE_012
```C
#include <stdio.h>
int main()
{
	int a;
	scanf("%d" , &a);
	if(a>=90) printf("A\n");
	else if(a>=80 && a<90) printf("B\n");
	else if(a>=60 && a<80) printf("C\n");
	else printf("F\n");
}
```
