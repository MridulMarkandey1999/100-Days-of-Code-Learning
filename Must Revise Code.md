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
### Q2. 
