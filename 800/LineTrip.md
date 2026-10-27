## PROBLEM
https://codeforces.com/problemset/problem/1901/A


## SOLUTION
``` cpp
#include<bits/stdc++.h>
using namespace std;

int main(){
    int tt; cin>>tt;
    while(tt--){
        int n,x; cin>>n>>x;
        vector<int> v;
        for(int i=0 ; i<n ; i++){
            int temp; cin>>temp;
            v.push_back(temp);
        } 
        int ans = max(2*(x-v[n-1]) , v[0]);
        for(int i=0 ; i<n ; i++){
            ans = max(ans , v[i]-v[i-1]);
        }
        cout<<ans<<"\n";
    }
}
```

## COMPLEXITY
- time - N
- space - N (for storing array)