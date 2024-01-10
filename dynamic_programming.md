Dynamic Programming(DP)

general, powerful way of algorithm design technique. 

polynomial time??

DP ~ carefule brute force 
DP ~ subproblems + re-use 
=> split problem into subproblems and reuse solution 

- cover memoization & subproblems 
- Fibonacci
- shortest paths
- guessing & DAG view

what is that even mean????

Belman Ford algorithm?

term is quite weird

Fibonacci numbers 
F1 = F2 = 1
Fn = Fn-1 + Fn-2 

goal: compute Fn 

Navive recursive algoritm 
fib(n): 
    if n<=2: f=1
    else f= fib(n-1) + fib(n-2)
    return f

Time complexity of the recurrence 
T(n) = T(n-1) + T(n-2) + O(1)
T(n) is at least O(2^(n/2))

## Memoized DP algorithm

memo = {}
fib(n):
    if n in memo: return memo[n]
    if n<=2: f = 1
    else f= fib(n-1) + fib(n-2)
    memo[n] = f
    return f
