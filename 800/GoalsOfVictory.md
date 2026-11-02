## PROBLEM
https://codeforces.com/problemset/problem/1877/A

## SOLUTION

```cpp
#include<bits/stdc++.h>
using namespace std;

int main(){
    int tt; cin>>tt;
    while(tt--){
        int n; cin>>n;
        int sum = 0;
        for(int i=0 ; i<n-1 ; i++){
            int temp; cin>>temp;
            sum += temp;
        }
        cout<<-sum<<"\n";
    }
}
```