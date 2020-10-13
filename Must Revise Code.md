# Questions

### Q1. Rearrange an array with O(1) extra space.
  > https://practice.geeksforgeeks.org/problems/rearrange-an-array-with-o1-extra-space3142/1/?track=ppc-arrays&batchId=221
  ```
  void arrange(long long arr[], int n) {
    // Your code here
    unordered_map<int,int> mp;
    for(int i=0;i<n;i++)
    {
        arr[i]+=(arr[arr[i]]%n)*n;
    }
    for(int i=0;i<n;i++)
    {
       arr[i]=arr[i]/n;
    }
    
}
```
### Q2. Merge Without Extra Space

> https://practice.geeksforgeeks.org/problems/merge-two-sorted-arrays-1587115620/1/?track=ppc-arrays&batchId=221

```
void merge(int arr1[], int arr2[], int n, int m) 
{ 
    //Your code here
    //n is size of arr1
    //m is size of arr2
    int i=n-1,j=0;
    while(i>=0 && j<m)
        {
            if(arr1[i]>arr2[j])
            {
                swap(arr1[i], arr2[j]);
                i--;
                j++;
            }
            else
            {
                i--;
            }   
        }
        sort(arr1,arr1+n);
        sort(arr2,arr2+m);
}
```

### Q3.Rearrange Array Alternately

>https://practice.geeksforgeeks.org/problems/-rearrange-array-alternately/0/?track=md-arrays&batchId=144

```
#include <iostream>
#include<algorithm>
using namespace std;
int main() {
	//code
	int t;
	cin>>t;
	for(int i=0;i<t;i++)
	{
	    long int n;
	    cin>>n;
	    long int arr[n];
	    for(long int j=0;j<n;j++)
	    {
	        cin>>arr[j];
	    }
	    for(long int j=0;j<n/2;j++)
	    {
	        cout<<arr[n-1-j]<<" "<<arr[j]<<" ";
	    }
	    if(n%2!=0)
	    {
	        cout<<arr[n/2];
	    }
	    
	    cout<<endl;
	}
	return 0;
}

```
### Q4. 
