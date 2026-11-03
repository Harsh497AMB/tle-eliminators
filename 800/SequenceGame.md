## PROBLEM
https://codeforces.com/problemset/problem/1862/B

## SOLUTION

```cpp
#include<bits/stdc++.h>
using namespace std;

int main(){
    int tt; cin>>tt;
    while(tt--){
        int n; cin>>n;
        vector<int> v;
        for(int i=0 ; i<n ; i++){
            int t; cin>>t;
            v.push_back(t);
        }

        vector<int> ans;
        ans.push_back(v[0]);
        for(int i=1 ; i<n ; i++){
            if(v[i] >= v[i-1]){
                ans.push_back(v[i]);
            }else{
                ans.push_back(1);
                ans.push_back(v[i]);
            }
        }
        cout<<ans.size()<<"\n";
        for(auto it:ans) cout<<it<<" ";
        cout<<"\n";
    }
}
```