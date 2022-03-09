 # [Bubble Sort](https://github.com/nanyahill/coding-interview-resources/blob/master/src/algorithms/sorting/bubblesort/BubbleSort.java)
  #### Key Ideas:
          - Compare adjacent elements of the array and exchange them if they are out of order
	      - Largest/Smallest element is bubbled to the top depending on the sorting direction
	      - After the first pass, the top part of the array is always sorted
	      - Overall, (n-1) comparisons are done in the 1st pass, (n-2) comparisons are done in 2nd pass, etc...
          - Optimizations:
              - inner loop goes from 0..n-i-1 since the end of array is already sorted
              - boolean flag checks if array is already sorted using the inner loop
	      
  #### Properties/Sidenotes:
          - It is a comparison based sorting algorithm
	      - It is a stable algorithm.
	      - It is an in-place algorithm.
	      - It is about four times as slow as insertion sort and twice as slow as selection sort.
          - It has a good best-case behavior, but is impractically slow on almost all real world data sets and is not considered for implementation in real applications.
        
  #### Analysis:
        - **Best Case:** O(n), **Average/Worst Case:** O(n^2)
	
  #### Related Articles/Videos:
  - [BubbleSort on MyCodeSchool](https://youtu.be/Jdtq5uKz-w4)
  - [BubbleSort on InterviewBit](https://www.interviewbit.com/tutorial/bubble-sort/)
