# CMPS 2200 Assignment 3
## Answers

**Name:** Disha Amin


Place all written answers from `assignment-03.md` here for easier grading.

1a) Greedy algorithms involve finding a local optimum at each iteration in attempts to find a global optimum. In this problem, we want to minimize the number of coins. We can apply a greedy algorithm similar to the "finding change" problem from class. The first step of local optimization is finding the greatest possible value we can fulfill with one coin. So, find the greatest denomination of 2^k that is less than or equal to N. Next, subtract the denomnation of 2^k from N, and repeat until we reach 0. 
For example, if we want to exchange N = 10, on the first iteration we can set aside a coin that is equal to 2^3 = 8. Then, we can subtract 10 - 8 = 2, so the next coin we need to find must be less than or equal to 2. 2^1 = 2, and 2 - 2 = 0.

1b)   The properties of greedy algorithms are greedy choice property and optimal substructure. Greedy choice means that we can reach a local optimum at each step. This is true. At each step, we are finding a local optimum that fulfills the greatest value which is less than or equal to N. Next, we must prove optimal substructure. This means that using the local optimums, we can find a global optimum. This is also true, by substracting out the 2^k denominations from N, we end up finding a globally optimal solution when N reaches 0. 

1c) W(n) = O(log_n), S(n) = O(log_n) -- because we are finding denominations that are powers of 2 (2^k), and greedy algorithms cannot be parallelized.

2a) When using an algorithm that finds optimum based on arbitrary denominations rather than fixed denominations of 2, for example, if someone went to a bank that used denominations of 2,3,5 and wanted to exchange N = $10 as above, an algorithm could potentially suggest using 2 coins of 2 + 2 coins of 3, or 1 coin of 5 + 1 coin of 2 + 1 coin of 3. However, the optimal minimal solution here is to use 2 coins of 5.

2b) Optimal substructure means that using local optimum, we can find a globally optimal solution. This problem can use the optimal substructure property because it can find locally optimal solutions and combine them to find the global optimum. For example, with the case above, if the algorithm splits our $10 in half, it can find 1 coin of 5 to be the local optimum with each half and combine it to get the global optimum. However this algorithm does not exhbiit the greedy choice property because it also has small denominations like 2 and 3 where it can determine those to be "local optimums", but in reality, adding those together would not find a globaly optimal solution.

2c) W(n) = O(n*k), S(n) = O(n*k) --> [O(n)]

3b) Please see the grading note in main.py



