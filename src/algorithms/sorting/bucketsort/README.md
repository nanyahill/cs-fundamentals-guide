Bucket Sort with doubles
- It is a comparison based sorting algorithm
- It is a generalized form of counting sort.
- Select an appropriate size for each bucket. A large bucket size for densely populated array would lead to a lot of buckets being empty (waste of space) with non-empty buckets being too large. Hence, for densely populate array use a small bucket size and the inverse is also true.
- Based on the max and min value, the bucket count can be computed. max - min / bucketSize + 1
- Sorts by:
	- Partitioning an array into a finite number of buckets.
	- Each bucket is able to hold n/k number of values (if an array is used).
	- Each bucket is then sorted individually, either using a different sorting algorithm, or by recursively applying the bucket sorting algorithm.
- Usually each bucket is implemented as a linkedlist or dynamic array.
- It works best when the elements of the input data set are evenly distributed across all buckets.
- A divider can be computed to determine where each element will be placed in the bucket. divider = ceil(max + 1/bucketSize).
- Elements are placed in the bucket using: floor(array[i]/divider) OR if numbers are in the range 0 and 1, then b_idx = floor(n * array[i]).
- If the inner sorting algorithm is a recursive call on bucket sort itself, it becomes MSD radix sort.
- A bucket size of 2 becomes Quick sort.
- Time complexity: Average case: O(n + k) k = number of buckets. Even though insertion sort is used because buckets are 'small' in expectation and each bucket contains a constant (O(1)) amount of items assuming elements are uniformly distributed between the buckets. Worst case is O(n^2) when all elements are allocated to the same bucket.
- Space complexity: O(n+k) where k is number of buckets.
- Example problem where bucket sort is applicble: One has been given a large array of floating point integers lying uniformly between the lower and upper bound.

Bucket Sort with integers
A note about bucket sizes (the size of each bucket):If the values are sparsely allocated over the possible value range, a larger bucket size is better since the buckets will likely be more evenly distributed. An example of this is [2303, 33, 1044], if buckets can only contain 5 different values then for this example 461 buckets would need to be initialised. A bucket size of 200-1000 would be much more reasonable. The inverse of this is also true; a densely allocated array like [103, 99, 119, 112, 111] performs best when buckets are as small as possible.

Bucket sort is an ideal algorithm choice when:
The additional O(n + k) memory usage is not an issue
Elements are expected to be fairly evenly distributed


References
http://www.growingwiththeweb.com/2015/06/bucket-sort.html, Growing with the web
http://www.shuati123.com/blog/2014/07/22/Bucket-Sort/, Woodstock blog
https://www.geeksforgeeks.org/bucket-sort-2/, G4G
https://cs.stackexchange.com/questions/48815/why-do-we-use-insertion-sort-in-the-bucket-sort, StackExchange
https://stackoverflow.com/questions/7311415/how-is-the-complexity-of-bucket-sort-is-onk-if-we-implement-buckets-using-lin, StackOverflow