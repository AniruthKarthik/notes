# DYNAMIC PROGRAMMING

---
### Memoisation
Memoisation is when we start with the original problem and recursively solve sub problems and store the results in a hash map or a table to prevent recompution. 

```
int fib(int n, int memo[]) {
    if (n <= 1) return n;
    if (memo[n] != -1) return memo[n];
    return memo[n] = fib(n - 1, memo) + fib(n - 2, memo);
}
```
---
### Tabulation
Tabulation is when we solve all the sub problems first, starting from the smallest and use the results to solve the original problem.
``````
int fib(int n) {
    int dp[n + 1];
    dp[0] = 0;
    dp[1] = 1;
    for (int i = 2; i <= n; i++) {
        dp[i] = dp[i - 1] + dp[i - 2];
    }
    return dp[n];
}
``````
---

