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
- Time/space tradeoff

### Understanding Big O
- Big O describes the rate of growth for an algorithm in time or space depedning on the input size
	- If there exists a constant c and input n0 such that for each n >= n0 f(n) can't be higher than c * g(n), then f(n) = O (g(n))
		- f(n) can't grow faster than g(n)

- Time Complexity
	- Runtime of an algorithm

- Space Complexity
	- Memory required for an algorithm

- O,Ω,θ
	- O: doesn't grow faster than
	- Ω: doesn't grow slower than
	- θ: grows as fast as


### Analyze Solutions
#### Commmon Big O Complexities
	- Constant: O(1)
		- not dependent on input n
	- Linear: O(n)
		- directly proportianl to input n
	- Polynomial: (n^k)
		- grows more quickly as n increases
	- Logarithmic: O(logn)
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
		- when a multipart algorithm does an operation A then an operation B, then the runtimes of both operation are added together
			- O(A + B)
	- Multiplying runtimes
		- when a multipart algorithm does an operation A for each operation B, then the runtimes are multiplies
			- O(A * B)

### Time Space Tradeoff
	- more often than not you will have to choose between optimal time over optimal space, and vice versa
	- important to find a balance between the two depedning on the problem
	- always ask if there is a constraint on time and/or space when given a problem

- Topics
	- Intro to Big O (runtime and memory)
    - Time/space tradeoff
    - When not to worry about Big O

- Resources
	- https://www.geeksforgeeks.org/analysis-algorithms-big-o-analysis/