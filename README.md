#include<stdio.h>
int min(int x,int y)
{
return x<y?x:y;
}
int max(int x,int y)
{
return x>y?x:y;
}
int maxSubarrayproduct(int arr[], int n)
{
int min_ending_here=1;
int max_ending_here=1;
int flag_so_far=0
int flag=0
for(int i=0;i<n;i++)
{
if(arr[i]>0)
{
max_ending_here=max_ending_here*arr[i];
min_ending_here=min(min_ending_here*arr[i],1)
flag=1;
}
elseif(arr[i]==0)
{
max_ending_here=1;
min_ending_here=1;
}
else
{
int temp = max_ending_here;
 max_ending_here= max(min_ending_here * arr[i], 1);
 min_ending_here = temp * arr[i];
 }
if (max_so_far < max_ending_here)
 max_so_far = max_ending_here;
}
if (flag == 0 && max_so_far == 0)
 return 0;
 return max_so_far;
 return max_so_far;
}
int main()
{
int arr[];
int n = size of arr[1]/arr[0];
printf("Maximum Sub array product is %d",maxSubarrayProduct(arr, n));
return 0;
}
