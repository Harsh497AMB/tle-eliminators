## PROBLEM
https://codeforces.com/problemset/problem/1900/A


##  Approach

1. if we have "..." then the answer is always 2, because you can always pickup the water from middle cell
2. if "..." not found , it means we have to fill all the buckets

##  Complexity Analysis

- **Time Complexity:** `O(n)` per test case.
- **Space Complexity:** `O(n)` for storing the array.

## Solution (C++)

```cpp
#include <bits/stdc++.h>
using namespace std;

int f(string& s) {
    int freq = 0;
    int k = 3;

    for (int i = 0; i < s.length(); i++) {
        if (s[i] == '.') {
            k--;
            freq++;
        } else {
            k = 3;
        }

        if (k == 0) return 2;
    }

    return freq;
}

int main() {
    int tt;
    cin >> tt;

    while (tt--) {
        int n;
        cin >> n;

        string s;
        cin >> s;

        cout << f(s) << "\n";
    }
}
```