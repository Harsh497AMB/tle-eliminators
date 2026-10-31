## PROBLEM
https://codeforces.com/problemset/problem/1899/A


##  Approach

1. if the number is divisible by 3 the first member could never make it divisible by 3 by +1or-1
2. if not divisible by 3 then then he can either do +1 or -1

##  Complexity Analysis

- **Time Complexity:** `O(1)` per test case.
- **Space Complexity:** `O(1)` for storing the array.

## Solution (C++)

```cpp
#include<bits/stdc++.h>
using namespace std;
 
int main(){
    int tt; cin>>tt;
    while(tt--){
        int n; cin>>n;
        if(n%3) cout<<"First\n";
        else cout<<"Second\n";
    }
}
```