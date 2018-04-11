- It is an integer sorting algorithm.
- It sorts data with integer keys by gropuing the keys based on digits which share the same position and value.
- There are two classifications of radix sort:
	- LSD radix sort: sorts by grouping keys based on digits starting from the right (LSD) to left (MSD).
	- MSD radix sort: sorts by grouping keys based on digits starting from the left (MSD) to right (LSD).
- Underneath, LSD and MSD use countig sort to perform actual sorting.
- Radix sort is limited to data with integer keys such as strings, intergers or specially formatted floating point numbers.


LSD
- Usually solved iteratively, using counting sort internally.
	- For each digit, perform counting sort using that digit.
- Time complexity id O(w(n + R)) where w = word size, R = radix (e.g. 256 for characters). +R because of the count array. In practice, R is much smaller making LSD radix sort a linear sorting algorithm. When w is a constant, LSD radix sort is a linear algorithm.
- Space complexity: O(n + R)
- It is stable.
- Works best with fixed length keys. However, for variable length keys, LSD radix sort can be achieved by grouping all of the keys that have the same length together and separately performing an LSD radix sort on each group of keys for each length, from shortest to longest, in order to avoid processing the whole list of keys on every sorting pass.
- LSD radix sorts typically use the following sorting order: short keys come before longer keys, and keys of the same length are sorted lexicographically. This coincides with the normal order of integer representations, such as the sequence 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11.

MSD
- MSD radix sorts use lexicographic order, which is suitable for sorting strings, such as words, or fixed-length integer representations.
- Usually solved recursively.
- Implementations:
	Stable MSD String Sort
		- Perform counting sort based on the leftmost digit/character. This partitions the inout array into subarrays for each possible value of the leftmost digit/character.
		- Recursively sort subarrays corresponding to each character (excluding the leftmost digit/character, which is the same for each string in each subarray).
		- It works well for sorting variable length strings. Treats shorter strings as if they had an extra char at end 		(smaller than any character). Also, uses an auxillary storage for maintaining stability.
		Pros: Stable; Cons:	much too slow for small subarrays (can use insertion sort), huge number of small subarrays due to recursion, access memory randomly (cache inefficient),
		Time complexity: O(w(n + R)), Space complexity: O(n + dR) where d is from the recursive call stack depth.
	American Flag Sort (R-way partitioning in-place)- sacrifices stability, eliminates auxillary storage.
	MSD three-way quicksort
		- Partition inpt array based on leftmost digit/character into "less", "equal", and "greater" subarrays.
		- Then recursively sort subarrays.
		Pros: Cache efficient, in-place, Cons: Not stable.