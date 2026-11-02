## PROBLEM
https://codeforces.com/problemset/problem/1878/A

## SOLUTION

```cpp
#include<bits/stdc++.h>
using namespace std;

int main(){
    int tt; cin>>tt;
    while(tt--){
        int n,k; cin>>n>>k;
        vector<int> v;
        for(int i=0 ; i<n ; i++){
            int temp; cin>>temp;
            v.push_back(temp);
        }
        bool exist = false;
        for(int i=0 ; i<n ; i++){
            if(v[i]==k){
                exist = true;
                break;
            }
        }
        if(exist) cout<<"YES\n";
        else cout<<"NO\n";
    }
}
```