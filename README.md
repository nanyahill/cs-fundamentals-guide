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
	      - Overall, the original array is sorted by h-sorting subarrays for each value of h.
	      - Each value of h can be called a gap.
        ##### Properties:
	      - Improves insertion sort algorithm.
	      - Splits original array into multiple subarrays, then h-sort subarrays.
	      - h-sort means rearrange the array such that elements at every hth positions form a sorted sequence.
	      - h consists of an appropriate set of decrementing sequence that ends in 1. e.g. 10, 5, 2, 1.
	      - Overall, the original array is sorted by h-sorting subarrays for each value of h.
	      - Each value of h can be called a gap.
	      
	      - The choice of the decrementing sequence is ######key to shell sort and can lead to better time complexity. 
	      - By sorting subarrays, elements are moved closer to their correct position.
	      - A subarray consists of elements that are h elements apart.
	      - When h is 1, shell sort becomes simply insertion sort
        - For any given gap, multiple subarrays can exist. Example: Using a gap of 3, the below array has three subarrays.
    - Merge Sort
    - Quick Sort
  - Non-Comparison based
    - Radix Sort
    - Counting Sort
- Dynamic Programming
- Greedy Algorithms

