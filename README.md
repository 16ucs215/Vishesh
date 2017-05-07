# Vishesh
#include <bits/stdc++.h>
using namespace std;

ll pwr(ll a,ll b,ll mod=MOD) ///calculate power if
{
	ll ans=1;
	while(b){if(b&1) ans=(ans*a)%mod;a=(a*a)%mod;b/=2;}
}
ll count()  ///count the number of divisors total ...sieve gives only distinct prime factors.
{
	int curr=n/temp[n];
	while(n!=1)
	{
		n/=temp[n];
		if(curr==temp[n])
		{
			count++;
		}
		else
		{
			ans*=(count+1)
			count=1;
		}

	}
}
public boolean isPrime(int n) ///for a single number return prime or not.
{
	int m =sqrt(n);
	if(n==1)
		return 0;
	if(n==2)
		return 1;
	if(n==3)
		return 1;
	if(n%2==0)
		return 0;
	for(int i=3;i<=m;i+=2) ///increment by even numbers....
	{
		if(n%i==0)
			return 0;
	}
	return 1;
}

public boolean sieve(int n)  ///gives all the distinct prime numbers of any num entered
{
	for(int i=0;i<=n;i++) 
	{
		a[i]=i;
	}
	for(int i=2;i*i<=n;i++)
	{
		if(a[i]==i){
			v[i].pb(i); ///the number is prime so its distinct prime factor inlclude only the num
			continue;
		}
		for(int j=i*2;j<=n;j+=i)
		{
			a[j]=-1;
			v[j].pb(i);
		}
	}
}
public boolean sieve(int n)  //also check that if vector size is empty that number is itself prime
{
	for(int i=0;i<=n;i++) ///bt still only store the smallest prime factor...
	{
		a[i]=i;
	}
	for(int i=2;i*i<=n;i++)
	{
		if(a[i]==i)
			continue;
		for(int j=i*i;j<=n;j+=i)
		{
			a[j]=-1;
			v[j].pb(i);
		}
	}
}

public boolean sieve(int n)  //if to check whether prime or not....
{
	for(int i=0;i<=n;i++)
	{
		a[i]=i;
	}
	for(int i=2;i*i<=n;i++)
	{
		if(a[i]!=i)
			continue;
		for(int j=i*i;j<=n;j+=i)
		{
			a[j]=-1;
		}
	}
}
int GCD(int a,int b)
{
	if(b==0) return a;
	return(b,a%b);
}
