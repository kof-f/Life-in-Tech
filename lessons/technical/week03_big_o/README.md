# Big O

### Copyright
Copyright 2020, Kofi Forson, Kyrhee Powell and Curtis Hite \
New York City, NY 11413 \
All Rights Reserved

This is a repository containing course information for Life in Tech. Kofi Forson, Kyrhee Powell and Curtis Hite Jr. assert copyright ownership of this repository and all derivative works, including courses and material derived from this course and/or repository. This copyright statement should not be removed or edited.


### Objectives
At the end of this lesson students should be able to: 
- Understand Big O
- Analyze solutions to determine Big O
- Understand time/space tradeoff

### Understanding Big O
- Big O describes the rate of growth for an algorithm in time or space depending on the input size

- Time Complexity
	- Runtime of an algorithm

- Space Complexity
	- Memory required for an algorithm


### Analyze Solutions
#### Commmon Big O Complexities
- Constant: O(1)
	- not dependent on input n
- Linear: O(n)
	- directly proportional to input n
- Polynomial: O(n^k)
	- grows more quickly as n increases
- Logarithmic: O(logn)
	- divide and conquer
	- not using whole input n (ex: only use half of input n)

#### Rules
- Drop the constants
	- when descirbing the rate of increase, constants are unnecessary
	- O(2n) = O(n)
	- O(n + 3) = O(n)
- Drop non-dominant terms
	- the most dominant term is the variable with the biggest power
	- the dominant term is what determines the rate of increase of an algorithm
		- non-dominating terms don't have as much as an impact so they can be droppped
	- O(n^2 + n) = O(n^2)
	- O(n^5 + n^3 + n) = O(n^5)
- Adding runtimes
	- when a multipart algorithm does an operation A then an operation B, then the runtimes of both operations are added together
		- O(A + B)
- Multiplying runtimes
	- when a multipart algorithm does an operation A for each operation B, then the runtimes are multiplied
		- O(A * B)

#### Examples using an algorithm
EX 1
	int sum = 0;
	int product = 1;
	for (int i = 0; i < array.length; i++) {
		sum += array[i];
	}
	for (int i = 0; i < array.length; i++) {
		product *= array[i];
	}
	System.out.println(sum + "," + product);

EX 2
	def binary_search(arr, x): 
		low = 0
		high = len(arr) - 1
		mid = 0
			
		while low <= high: 

			mid = (high + low) // 2
		# Check if x is present at mid 
		if arr[mid] < x: 
		    low = mid + 1

		# If x is greater, ignore left half 
		elif arr[mid] > x: 
		    high = mid - 1

		# If x is smaller, ignore right half 
		else: 
		    return mid 

		# If we reach here, then the element was not present 
		return -1




### Time Space Tradeoff
- more often than not you will have to choose between optimal time over optimal space, and vice versa
- important to find a balance between the two depedning on the problem
- always ask if there is a constraint on time and/or space when given a problem

### Homework
Find the run times for the following problems
1. 
	int mod(int a, int b) { 
		if (b <= 0) {
			return -1;
		}
		int div = a / b;
		return a - div * b;
	}

2. 
	int sumDigits(int n) { 
		int sum = 0;
		while (n > 0) { 
			sum += n % 10;
			n /= 10; 
		}
		return sum;
	}



### Resources
- https://www.geeksforgeeks.org/analysis-algorithms-big-o-analysis/