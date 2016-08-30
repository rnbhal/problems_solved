# Fibonacci Sequence

`Statement:` **Fibonacci Sequence - Enter a number and have the program generate the Fibonacci sequence to that number or to the Nth number.**

---
```
Example :
**Input** : 5
**Output** : 0 1 1 2 3 

**Input** : 10
**Output** : 0 1 1 2 3 5 8 13 21 34
``` 

**Solution 1:**

``` c++

void solve(int n) {
	long long int a = 0, b = 1, c = 1;
	cout << a << " " << b << " ";
	for (int i = 3; i <= n; ++i) {
		c = a + b;
		a = b;
		b = c;
		cout << c << " ";
	}
}

```
