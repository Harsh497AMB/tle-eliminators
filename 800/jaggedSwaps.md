## PROBLEM
https://codeforces.com/problemset/problem/1896/A


##  Approach

1. idk why it worked 

##  Complexity Analysis

- **Time Complexity:** `O(1)` per test case. (but `O(N)` to stop cin error)
- **Space Complexity:** `O(1)` for storing the array.

## Solution (C++)

```cpp
#include<bits/stdc++.h>
using namespace std;

int main(){
    int tt; cin>>tt;
    while(tt--){
        int n; cin>>n;
        int i; cin>>i;
        if(i != 1) cout<<"NO\n";
        else cout<<"YES\n";
        for(int j=1 ; j<n ; j++) cin>>i;
    }
}
```