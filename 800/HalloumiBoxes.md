##  Observation

- If `k > 1`, the array can be sorted using the allowed operations.
- If `k == 1`, the array cannot be rearranged freely, so it must already be sorted.

##  Approach

1. Read `n` and `k`.
2. Read all `n` elements into a vector.
3. If `k > 1` or the array is already sorted, print `YES`.
4. Otherwise, print `NO`.

##  Complexity Analysis

- **Time Complexity:** `O(n)` per test case.
- **Space Complexity:** `O(n)` for storing the array.

## Solution (C++)

```cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
    int tt;
    cin >> tt;

    while (tt--) {
        int n, k;
        cin >> n >> k;

        vector<int> v(n);

        for (int i = 0; i < n; i++) {
            cin >> v[i];
        }

        if (k > 1 || is_sorted(v.begin(), v.end())) {
            cout << "YES\n";
        } else {
            cout << "NO\n";
        }
    }

    return 0;
}
```