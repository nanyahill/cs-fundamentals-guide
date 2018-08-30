Dynamic Programming
- A general technique for solving optimization, search, and counting problems that can be decomposed into subproblems.
- Like divide and conquer, DP solves the problems by combining the solutions of smaller problems but what makes DP different is that the same subproblem may reoccur.
- Dynamic programming is a technique that combines the correctness of complete search (backtracking) and the efficiency of greedy algorithms. Dynamic programming can be applied if the problem can be divided into overlapping subproblems that can be solved independently. (competitive programmer handbook)
- Dynamic Programming is a technique that takes advantage of overlapping subproblems, optimal substructure, and trades space for time to improve the runtime complexity of algorithms. (source- the algorithmist)
- Key to solving DP problems inludes:
	- finding a way to break the original problem into smaller problems such that:
		1) the problem can be solved easily using solutions to smaller subproblems of the same kind.
		2) These subproblems solutions are cached.
- Top-down DP: uses recursion and usually an O(n) dynamic storage such as a hash table or BST. The table/storage is passed around at each level.
- Bottom-up DP: uses iteration and builds the cache bottom-up using sometimes O(1) space or a one- or two-dimensional space.
- There are two uses for dynamic programming:
	• Finding an optimal solution: We want to find a solution that is as large as possible or as small as possible.
	• Counting the number of solutions: We want to calculate the total number of possible solutions.

Attacking DP problems:
- After identifying the problem as a DP one, we need to come up with a recurrence relation.
- An easy way to come up with the recurrence relation is to think from the nth element downwards i.e. n-1, n-2, etc.
Notes
- When given a DP problem that involves a grid, think about if you are traversing the edges or the squares. Moving into a square is one count; moving along an edge is one count.

Understanding the recurrence relation of binomial coefficeint
Question: How many k element subsets can be built from n elements?
Answer: k element subsets built from n elements will contain subsets that:
	1) include the nth element: if a k element subset includes nth element, then we are looking to choose k-1 elements from n-1 elements.
	2) did not include the nth element: if a k element subset doesn't include nth element, then we're looking to choose k elements from n-1 elements (n-1 because choose k elements from n is what we're trying to answer).
Hence, the sum of the count of (1) and (2) is the answer to the above question.

DP practice problems:
1) https://people.cs.clemson.edu/~bcdean/dp_practice/

Articles
1) Difference between top-down and bottom-up DP. https://stackoverflow.com/questions/6164629/dynamic-programming-and-memoization-bottom-up-vs-top-down-approaches

Ideas of DP 10th of August:
1) The essence of dynamic programming is the idea of a state space and a recurrence relation between states. Once you figure that out for any problem, implementation is straightforward.