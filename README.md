# dream.github.io
![](https://cdn.luogu.com.cn/upload/usericon/346410.png)

![](https://luogu-card.vercel.app/practice?id=346410&dark_mode=true)

![](https://luogu-card.vercel.app/about?id=346410&dark_mode=true)

# "code" generater

```cpp
#include<bits/stdc++.h>
using namespace std;
long long jsl_rand(long long u,long long d)
{
	long long r=rand()%(u-d+1);
	long long ans1=u+r,ans2=abs(d-r);
	long long pd=rand()%2;
	if(pd==0)
	{
		if(ans1<=u)
			return ans1;
		return ans1-u;
	}
	if(ans2<=u)
		return ans2;
	return ans2-u;
}
int jsl2_rand(int u,int d)
{
	long long a=rand()%(u-d+1);
	long long b=rand()%(u-d+1);
	long long c=rand()%(u-d+1);
	long long ans=(a+b+c)/3;
	long long ans2=rand()%(u-d+1);
	if(ans+ans2<=u)
		return ans+ans2;
	return ans+ans2-u;
}
int main()
{
	long long s,u,d;
	cout<<"length:\n";
	cin>>s;
	cout<<"upper:\n";
	cin>>u;
	cout<"lower:\n";
	cin>>d;
	for(long long i=1;i<=s;i++)
	{
		int qwq=rand()%2;
		switch(qwq)
		{
			case 0:
			{
				cout<<(char)(jsl_rand(u,d)%256);
				break;
			}
			case 1:
			{
				cout<<(char)(jsl2_rand(u,d)%256);
				break;
			}
		}
	}
}
```
