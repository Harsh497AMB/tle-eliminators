## PROBLEM
https://codeforces.com/problemset/problem/1881/A

## SOLUTION

```cpp
#include<bits/stdc++.h>
using namespace std;

int f(string x, string s, int ans){
    if(x.find(s) != string::npos) return ans;
    x += x;
    if(x.find(s) != string::npos) return ans+1;

    return -1;
}

int main(){
    int tt; cin>>tt;
    while(tt--){
        int n,m; cin>>n>>m;
        string x,s; cin>>x>>s;
        int ans=0;

        while(x.size() < s.size()){
            x += x;
            ans++;
        }
        cout<<f(x,s,ans)<<"\n";
    }
}
```