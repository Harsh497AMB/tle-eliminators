## PROBLEM
https://codeforces.com/problemset/problem/1890/A

## SOLUTION

```cpp
#include<bits/stdc++.h>
using namespace std;

bool f(int n , vector<int>& v){
    unordered_map<int,int> hash;
    for(int i=0 ; i<n ; i++) hash[v[i]]++;

    if(hash.size() > 2) return false;
    if(hash.size() == 1) return true;

    vector<int> f;
    for(auto it: hash){
        f.push_back(it.second);
    }

    if(abs(f[0]-f[1])<2) return true;
    return false;
}

int main(){
    int tt; cin>>tt;
    while(tt--){
        int n; cin>>n;
        vector<int> v;
        for(int i=0 ; i<n ; i++){
            int temp; cin>>temp;
            v.push_back(temp);
        }
        if(f(n,v)) cout<<"Yes\n";
        else cout<<"No\n";
    }
}

```