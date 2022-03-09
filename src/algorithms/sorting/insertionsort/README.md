# [Insertion Sort](https://github.com/nanyahill/coding-interview-resources/blob/master/src/algorithms/sorting/insertionsort/InsertionSort.java)
#### Key Ideas:
          - Maintain two list/subarrays- sorted list (left-side) and unsorted list (right-side)
          - At every iteration, an element is picked from the unsorted list and inserted into their correct position in the sorted list by **shifting pre-existing sorted elements**
          - Basically grows a sorted list/array one element at a time

#### Properties/Sidenotes:
          - It is a comparison based sorting algorithm
	      - It is a stable algorithm
	      - It is an in-place algorithm.
          - Efficient for small data sets or partially sorted input
	      - It is one of the fastest sorting algorithms for sorting very small arrays, even faster than quicksort
          - It requires a linear number of compares when array is partially sorted

#### Algorithm Analysis:
        - Time: **Best Case:** O(n), **Average/Worst Case:** O(n^2)
        - Space: **Best Case:** O(1), **Average/Worst Case:** O(1)

#### Related Articles/Videos:
- [InsertionSort on MyCodeSchool](https://www.youtube.com/watch?v=i-SKeOcBwko)
