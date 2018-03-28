 # [Shell Sort](https://github.com/nanyahill/coding-interview-resources/blob/master/src/sorting/shellsort/ShellSort.java)
  #### Key Ideas:
	      - Improves insertion sort algorithm.
	      - Splits original array into multiple subarrays, then h-sort subarrays.
	      - h-sort means rearrange the array such that elements at every hth positions form a sorted sequence.
	      - h consists of an appropriate set of decrementing sequence that ends in 1. e.g. 10, 5, 2, 1.
	      - Each value of h can be called a gap.
	      - A subarray consists of elements that are h elements apart.
	      - Overall, the original array is sorted by h-sorting subarrays for each value of h.
	      
  #### Properties:
	      - It is not a stable algorithm.
	      - It is an in-place algorithm.
	      - An h-sorted array remains h-sorted after g-sorting it.
	      - Above point has to be true because earlier sorting passes are not undone by later sorting passes.
	      - The choice of the decrementing sequence is KEY to shell sort and can lead to better time complexity. 
	      - For every h-sort, elements are moved closer to their correct position.
	      - When h is 1, shell sort becomes simply insertion sort with much less inversions.
        
  ##### Analysis:
