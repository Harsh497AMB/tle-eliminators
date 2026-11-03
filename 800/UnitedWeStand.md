## PROBLEM
https://codeforces.com/problemset/problem/1859/A

## SOLUTION

```cpp
#include<bits/stdc++.h>
using namespace std;

int main(){
    int tt; cin>>tt;
    while(tt--){
        int n; cin>>n;
        vector<int> v;
        unordered_map<int,int> hash;
        int max_elem = 0;
        for(int i=0 ; i<n ; i++){
            int t; cin>>t;
            max_elem = max(max_elem , t);
            hash[t]++;
            v.push_back(t);
        }
        if(hash.size()==1) cout<<-1<<"\n";
        else{
            vector<int> b,c;
            //b%c != 0
            //c should have largest element
            for(int i=0 ; i<hash[max_elem] ; i++){
                c.push_back(max_elem);
            }
            for(int i=0 ; i<n ; i++){
                if(v[i] != max_elem) b.push_back(v[i]);
            }
            cout<<b.size()<<" "<<c.size()<<"\n";
            for(auto it: b) cout<<it<<" ";
            cout<<"\n";
            for(auto it: c) cout<<it<<" ";
            cout<<"\n";
        }        
    }
}
```