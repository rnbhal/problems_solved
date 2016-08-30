# Prime Factorization

`Statement:` **Prime Factorization - Have the user enter a number and find all Prime Factors (if there are any) and display them.**

**Example :**
```
Input  : 10
Output : 1 2 5 

Input  : 19
Output : 1 19

Input  : 12345678910
Output : 1 2 5 1234567891
``` 
---
**Solution 1:**

```
0 <= N <= 10^18
Time : O(sqrt(n))
Memory : O(1)
```

``` c++

#include "large.cpp" // include prime factor upto 10^9
void solve(long long int n) {
	if (n <= 1)
	{
		cout << n;
		return;
	}
	cout << 1 << " ";
	int root = sqrt(n);
	for (int i = 0; factor[i] <= root; i++){
		if (n%factor[i] == 0) {
			cout << factor[i] << " ";
			while (n%factor[i] == 0)
				n /= factor[i];
		}
	}
	if (n != 1)
		cout << n;
}

```
