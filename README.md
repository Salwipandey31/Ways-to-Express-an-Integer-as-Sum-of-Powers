# Ways-to-Express-an-Integer-as-Sum-of-Powers
Problem Statement
Given two positive integers n and x, determine how many distinct ways n can be expressed as the sum of the x-th powers of unique positive integers.

Formally, count the number of unique sets {a₁, a₂, …, aₖ} such that:

𝑛
=
𝑎
1
𝑥
+
𝑎
2
𝑥
+
⋯
+
𝑎
𝑘
𝑥
n=a 
1
x
​
 +a 
2
x
​
 +⋯+a 
k
x
​
 
and each integer appears at most once.
Return the result modulo 10⁹ + 7.


Example
Input:
n = 10, x = 2
Output:
1

Explanation:
Only one valid set exists:

10
=
3
2
+
1
2
10=3 
2
 +1 
2


Input:
n = 4, x = 1
Output:
2

Explanation:
Two valid sets:

4
=
4
1
4=4 
1
 

4
=
3
1
+
1
1
4=3 
1
 +1 
1

Constraints
1
≤
𝑛
≤
300
1≤n≤300

1
≤
𝑥
≤
5
1≤x≤5

Solution Approach
Use DFS + Memoization to explore possible integers.

At each step, choose to either take or skip the current integer.

Memoize results for (remainingSum, currentNumber) to avoid recomputation.

Return the total number of valid combinations modulo 10⁹ + 7.

