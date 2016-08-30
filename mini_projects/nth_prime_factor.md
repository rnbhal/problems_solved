# Next Prime Number

`Statement:` **Next Prime Number - Have the program find the nth prime numbers.**

**Example :**
```
Input  : 78499
Output : 999983 

Input  : 3
Output : 3

Input  : 1
Output : 1

Input  : 10
Output : 23
``` 
---

**Solution 1:**
```
1 <= N <= 78499
Time : O(1)
Memory : O(1)
```

``` c++
#include "large.cpp" // prime factors upto 10^9
void solve(int n) {
	if (n <= 1)
	{
		cout << 1;
		return;
	}
	cout << factor[n - 2];
}
```


**Solution 2:**
```
1 <= N <= 78499
Time : O(N)
Memory : O(1)
```

``` c++
void solve(int n) {
	if (n <= 1)
	{
		cout << 1;
		return;
	}
	int cur = 1;
	int i = 1;
	while (i < n){
		cur++;
		bool prime = true;
		int root = sqrt(cur);
		for (int j = 0; factor[j] <= root; ++j){
			if (cur%factor[j] == 0)
			{
				prime = false;
				break;
			}
		}
		if (prime)
			i++;
	}
	cout << cur;
}

```
