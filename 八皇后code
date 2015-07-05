#include<iostream>
#include<string>
using namespace std;
bool place(int *a,int k)
{
	for(int i=0;i<k;i++)
		if(((i-k)==(a[i]-a[k]))||((i-k)==(a[k]-a[i])))
			return false;
	return true;
}
void queenchild(int *a,int k,int kqueen)
{
	if(a[k]==kqueen)
	{
		for(int i=0;i<kqueen;i++)
			cout<<a[i]<<",";
		cout<<endl;
	}
	else
	{
		for(int j=k;j<kqueen;j++)
		{
			int temp=a[j];
			a[j]=a[k];
			a[k]=temp;
			if(place(a,k))
				queenchild(a,k+1,kqueen);
			temp=a[j];
			a[j]=a[k];
			a[k]=temp;
		}
	}
}
void queen(int *a,int kqueen)
{
	queenchild(a,0,kqueen);
}
void main()
{
	int k=0;
	cin>>k;
	int *a=new int[k+1];
	for(int i=0;i<=k;i++)
		a[i]=i;
	queen(a,k);
}
