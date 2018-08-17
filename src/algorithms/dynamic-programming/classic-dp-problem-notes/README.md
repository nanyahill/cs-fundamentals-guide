Gotchas in DP problem solving:
1) Using Arrays.fill(..) to fill a 2D array.
2) Forgetting to change the method name from <method_name>_Recursion to <metod_name>_TopDownDP

Classic DP Problems:
1) Min Coin Change Problem:
	a) Recursive Backtracking: Generate all possible combinations of the coins that give the change while computing the minimum number of coins that make up that combination. Complexity Analysis: Every coin denomination can have at most S/ci values. Hence number of possible combinations is: S/c1 * S/c2 ....* S/cn. O(S^n).
	b) Top Down DP: Cache computed results. There are at most S subproblems that need to be computed using n iterations of the coin denomination. O(S * n).
	c) Bottom-Up: Cache computed results. Initialize cache[0] to 0 and other entries to Integer.MAX_VALUE. Outer loop: Iterate over change, inner loop iterates over coin denominations. At each iteration of the inner loop, check if i - coins[j] >= 0 and if cache[i - coins[j]] != Integer.MAX_VALUE.

2) Longest Common Subsequence
This problem is similar to edit distance (Levenstein Distance). The difference is that there are no substitiution operations. Only increment when there is a match, no need to increment for insertion or deletion operations. It is advisable to start from the right hand side of both strings.
	a) Recursive Backtracking: Generate all the possible subsequence of each string and find the one that is common to both. Complexity is 2^n since the number of possible subsequence is 2^n.
	b) Top-Down:
	c) Bottom-Up:
Variant: Compute the minimum number of edit operations to transform s1 to s2 where you can delete from either string. The idea here is that the result = s1.length - LCS + s2.length - LCS = s1.length + s2.length - 2*LCS.

3) Longest Increasing Subsequence.
The simplest approach (recursive) is to generate all possible subsequence, find the increasing subsequences and then find the longest of these increasing subsequence. This can be implemented recursivley and inside each function call, we consider two cases:

	* The current element is larger than the previous element included in the LIS. In this case, we can include the current 	element in the LIS. Thus, we find out the length of the LIS obtained by including it. Further, we also find out the length 	of LIS possible by not including the current element in the LIS. The value returned by the current function call is, thus, the 	maximum out of the two lengths.

	* The current element is smaller than the previous element included in the LIS. In this case, we can't include the current 	element in the LIS. Thus, we find out only the length of the LIS possible by not including the current element in the LIS, 	which is returned by the current function call.

Top-Down: Use a cache and check if cache value has already been computed.
	Gotchas:
		1) Two method arguments change state, the 'next' or 'prev' parameter (depending on how you move through the array) and the idx of the next element to consider. Hence, a 2D array is required.
		2) The final result is found in cache[nums.length + 1][nums.length]
Bottom-up: Use a 1D cache