## PROBLRM
https://codeforces.com/problemset/problem/1866/A

## SOLUTION

```cpp
#include<bits/stdc++.h>
using namespace std;

int main(){
    int ans = INT_MAX;
    int n; cin>>n;
    for(int i=0 ; i<n ; i++){
        int t; cin>>t;
        ans = min(ans , abs(t));
    }
    cout<<ans<<"\n";
}
```