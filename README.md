# The-length-of-the-longest-strictly-increasing-subsequence.
The length of the longest strictly increasing subsequence.
#include <iostream>
#include <vector>
using namespace std;
int listending(vector<int>&a,int idx){
if(idx==0)
 {return 1;}
 int mx=1;
 for(int pre=0;pre<idx;pre++)
 if(a[pre]<a[idx])
 
    mx=max(mx,listending(a,pre)+1);
 
     return mx;
}
   int list(vector<int>&a) {
    int n=a.size();
    int res=1;
    for(int i=1;i<n;i++)
    res= max (res, listending(a,i));
    return res;
}
int main()
{
 vector<int>a={10,2,55,7,44,90};
 cout<<list(a);
 return 0;

}
