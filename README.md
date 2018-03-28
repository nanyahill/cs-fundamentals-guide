# coding-interview-resources
Resources to help prepare for coding interviews.

### This repository is still under construction

> This repository serves as a way to brush up on CS fundamnetals required for coding interviews. Below, the topics related to Data Strcutures and Algorithms have been grouped as per my understanding thus far. Also, I have added helpful articles that I found when studying each of these topics.

Concepts:
- Recursion
- Big O complexity

Data Structures:
- Arrays
- LinkedLists
- Stacks and Queues
- Binary Trees
- Heaps
- Hash Tables
- Binary Search Trees

Algorithms:
- Searching
- Sorting
  - Comparison-based
    - Selection Sort
    - Bubble Sort
    - Insertion Sort
    - #### Shell Sort
      	##### Key Ideas:
	      - Improves insertion sort algorithm.
	      - Splits original array into multiple subarrays, then h-sort subarrays.
	      - h-sort means rearrange the array such that elements at every hth positions form a sorted sequence.
	      - h consists of an appropriate set of decrementing sequence that ends in 1. e.g. 10, 5, 2, 1.
	      - Each value of h can be called a gap.
	      - A subarray consists of elements that are h elements apart.
	      - Overall, the original array is sorted by h-sorting subarrays for each value of h.
        ##### Properties:
         -It is not a stable algorithm.
         -It is an in-place algorithm.
         -An h-sorted array remains h-sorted after g-sorting it. If otherwise, then shell sort would not make sense because earlier sorting is undone by later sorting.
	      - The choice of the decrementing sequence is KEY to shell sort and can lead to better time complexity. 
	      - For every h-sort, elements are moved closer to their correct position.
	      - When h is 1, shell sort becomes simply insertion sort.
	      
        - For any given gap, multiple subarrays can exist. Example: Using a gap of 3, the below array has three subarrays.
    - Merge Sort
    - Quick Sort
  - Non-Comparison based
    - Radix Sort
    - Counting Sort
- Dynamic Programming
- Greedy Algorithms

