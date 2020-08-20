# Search/Sort


### Copyright
Copyright 2020, Kofi Forson, Kyrhee Powell and Curtis Hite \
New York City, NY 11413 \
All Rights Reserved

This is a repository containing course information for Life in Tech. Kofi Forson, Kyrhee Powell and Curtis Hite Jr. assert copyright ownership of this repository and all derivative works, including courses and material derived from this course and/or repository. This copyright statement should not be removed or edited.


### Objectives
At the end of this lesson students should be able to: 
- Implement binary search
- Implement merge sort
- Understand the performance differences between merge and selection sort
- Be aware of Big O


 ### Binary Search
 #### Algorithm
 1. Compare the search value with the value in the middle of the list.
 2. If the search value is equal to the value in the middle of the list, we return True.
 3. Else If the search value is greater than the middle value, then the search value can only lie in right half subarray after the middle value.
 4. Else the search value is less than the middle value, then the search value can only lie in the left half subarray before the middle value.
 
#### Big O
Runtime: O(log(n)) \
Memory: O(1)

#### Implementation
Paste implementation here.

 ### Merge Sort
 #### Algorithm
 1. Find the middle point to divide the array into two halves: middle m = (l+r)/2
 2. Call mergeSort for first half: Call mergeSort(arr, l, m)
 3. Call mergeSort for second half: Call mergeSort(arr, m+1, r)
 4. Merge the two halves sorted in step 2 and 3: Call merge(arr, l, m, r)

#### Big O
Runtime: O(n log(n)) \
Memory: O(n)

#### Implementation
Paste implementation here.

 ### Insertion Sort
 #### Algorithm
 1. Iterate from arr[1] to arr[n] over the array.
 2. Compare the current element (key) to its predecessor.
 3. If the key element is smaller than its predecessor, compare it to the elements before. Move the greater elements one position up to make space for the swapped element.

#### Big O
Runtime: O(n^2) \
Memory: O(n)

#### Implementation
Paste implementation here.

Compare insertion sort to merge sort using Big O time/space complexity. Make sure to emphasize that selection sort isn't commonly used in technical problems.

 ### Big O
 __What is Big O?__ \
Big O notation is the language we use for talking about how long an algorithm takes to run and how much memory it uses in the process. It's how we compare the efficiency of different approaches to a problem.

 ### Homework Assignment
 Write an efficient algorithm that searches for a value in an m x n matrix. This matrix has the following properties:
- Integers in each row are sorted from left to right.
- The first integer of each row is greater than the last integer of the previous row.

__Example 1__:
```python
# Input:
matrix = [
  [1,  3,   5,  7],
  [10, 11, 16, 20],
  [23, 30, 34, 50]
]
target = 3
# The output should be True because 3 is in the first row of the 2D matrix.
```

__Example 2__:
```python
# Input:
matrix = [
  [1,  3,   5,  7],
  [10, 11, 16, 20],
  [23, 30, 34, 50]
]
target = 13
# The output should be False because 13 is not present in the 2D matrix.
```
 Solve the question and write the Big O space and time complexity of your solution.

### Resources
- [Search](https://www.geeksforgeeks.org/searching-algorithms/)
- [Sort](https://www.geeksforgeeks.org/sorting-algorithms/)