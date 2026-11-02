## PROBLEM
https://codeforces.com/problemset/problem/1873/C

## SOLUTION

```cpp
#include<bits/stdc++.h>
using namespace std;

int main(){
    int tt; cin>>tt;
    while(tt--){
        int ans = 0;
        for(int i=0 ; i<10 ; i++){
            for(int j=0 ; j<10 ; j++){
                char ch; cin>>ch;
                if(ch == 'X'){
                    int a,b;
                    if(i<5) a = i+1;
                    else a = 10-i;
                    if(j<5) b = j+1;
                    else b = 10-j;
                    ans += min(a,b);
                }
            }
        }
        cout<<ans<<"\n";
    }
}
```