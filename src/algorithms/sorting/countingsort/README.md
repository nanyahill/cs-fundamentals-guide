 # [Counting Sort](https://github.com/nanyahill/coding-interview-resources/blob/master/src/algorithms/sorting/countingsort/CountingSort.java)
  #### Key Ideas:
	      - Works only on an integer-based array within a GIVEN range. (Range must be given!)
	      - Elements of the input array map to the index of a temporary array (aka count array).
	      - Each index of the count array stores the count of that index, that is, the frequency
	        which the index appears as a value in the input.
	      - A prefix-sum (running sum) is performed for elements in the count array to determine
	        the starting position/place of the element in the sorted array.
	        For example, count[i] = 3 means value i (in the input array) will be in the 3rd place in sorted array.
	        (i.e. position 2 using zero-based array indexing).
	      - Overall there are three arrays- the input array of size n, the count array of size k, and
	        the sorted array of size n.

  #### Properties/Sidenotes:
	      - The size of the count array should be >= max(input[]), for example, if the maximum value of the
	        input value is 9, size of the count array should 10 (due to zero-based array-indexing).
	      - The algorithm is efficient ONLY if the range of values (max - min) is significantly less than n 
	        (the number of elements) or the range is fixed (e.eg ASCII characters).
	      - The algorithm can be extended to include negative integers.
	      - It is a stable sorting algorithm.
	      - It is NOT an in-place sorting algorithm. Hence, useful if additional memory is a no issue.

  #### Usage:
  	- The list is made up of integers or can be mapped to integers
	- The range of elements is known
	- Most of the elements in the range are present
	- The additional memory usage is not an issue

  #### Analysis:
        - **Best Case:** O(n + k); O(n) if k = O(n) **Worst Case:** O(n + k); O(n) if k = O(n)

  #### Related Articles:
  - [Counting Sort](http://www.growingwiththeweb.com/2014/05/counting-sort.html), Growing With the Web
  - [Counting Sort and Radix Sort](http://opendatastructures.org/versions/edition-0.1e/ods-java/11_2_Counting_Sort_Radix_So.html), Open Data Structures
  - [Counting Sort](https://www.geeksforgeeks.org/counting-sort/), Geeks4Geeks
  - [Counting Linearly with Counting Sort](https://medium.com/basecs/counting-linearly-with-counting-sort-cd8516ae09b3),basecs
  - [Counting Sort](https://www.hackerearth.com/practice/algorithms/sorting/counting-sort/tutorial/), HackerEarth
  - [Counting Sort Visualization](https://www.cs.usfca.edu/~galles/visualization/CountingSort.html), Professor David Galles
