---
title: $$[Algorithms \, In \, Action]-CH5\, Divide-and-Conquer $$
catalog: true
mathjax: true
date: 2021-03-03 17:15:56
subtitle:
header-img: cruves.png
tags:
- Review
- Divide-and-Conquer Algorithms
- Q&A
categories:
- CSCI 570
---


### Review Q&A
1. **(T/F)** For a divide-and-conquer algorithm, it is possible that the dividing step takes asymptotically longer time than the combining step.
	> - **False**

2. **(T/F)** A divide-and-conquer algorithm acting on an input size of n can have a lower bound less than $\Theta(n log(n))$.
	> - **False**

3. **(T/F)** There exist some problems that can be efficiently solved by a divide-andconquer algorithm but cannot be solved by a greedy algorithm.
	> - **False**

4. **(T/F)** It is possible for a divide-and-conquer algorithm to have an exponential runtime.
	> - **False**

5. **(T/F)** A divide-and-conquer algorithm is always recursive.
	> - **False**

6. **(T/F)** The master theorem can be applied to the following recurrence: $T(n) = 1.2 T(n/2) + n$.
	> - **False**

7. **(T/F)** The master theorem can be applied to the following recurrence: $T(n) = 9 T(n/3) - n^2 log(n) + n$.
	> - **False**

8. **(T/F)** Karatsuba’s algorithm reduces the number of multiplications from four to three.
	> - **False**

9. **(T/F)** The runtime complexity of mergesort can be asymptotically improved by recursively splitting an array into three parts (rather than into two parts).
	> - **False**

10. **(T/F)** Two $n x n$ matrices of integers are multiplied in $\Theta(n^2)$ time.
	> - **False**

11. (Fill in the blank) Let $A$, $B$ be two $2 x 2$ matrices that are multiplied using the standard multiplication method and Strassen’s method.
	a. Number of multiplications in the standard method:___________
	b. Number of additions in the standard method:___________
	c. Number of multiplications using Strassen’s method:___________
	d. Number of additions using Strassen’s method:___________
	> - **Solution**

12. (Fill in the blank) The space complexity of Strassen’s algorithm is:___________.
	> - **Solution**
	

### Exercise Q&A
1. Solve $T(n) = 3 T(n/4) + n$ by the recurrence tree method.
	> - **Solution**

2. Solve $T(n) = T(3n/4) + T(n/4) + n$ by the recurrence tree method.
	> - **Solution**

3. Solve the following recurrences by the master theorem:
	> - **Solution**

4. Prove Case 2 of the Master theorem.
	> - **Solution**

5. Prove Case 3 of the Master theorem.
	> - **Solution**

6. There are two sorted arrays, each of size $n$. Design a divide-and-conquer algorithm to find the median of the array obtained after merging the 2 arrays. Discuss its worst-case runtime complexity.
	> - **Solution**

7. You are given an unsorted array of all integers in the range $[0, …, 2^k - 1]$ except for one integer, which is denoted by $M$. Describe a divide-and-conquer algorithm to find the missing number $M$ and discuss its worst-case runtime complexity in terms of $n = 2^k$.
	> - **Solution**

8. We know that binary search on a sorted array of size $n$ takes $\Theta(log(n))$ time. Design a similar divide-and-conquer algorithm for searching in a sorted singly linked list of size $n$. Discuss its worst-case runtime complexity.
	> - **Solution**

9. We know that mergesort takes $\Theta(n log(n))$ time to sort an array of items. Design a divide-and-conquer mergesort algorithm for sorting a singly linked list. Discuss its worst-case runtime complexity.
	> - **Solution**

10. Given a sorted array of $n$ integers that has been rotated an unknown number of times, give an $\Theta(log(n))$ divide-and-conquer algorithm that finds an element in the resulting array. Note, after a single rotation, the array is not sorted anymore, so we cannot use the binary search. An example of a rotations sorted array is $A = [1, 3, 5, 7, 11]$; after first rotation it is $A = [3, 5, 7,11, 1]$, and after second rotation it is $A = [5, 7, 11, 1, 3]$. You may assume that that array has no duplicates.
	> - **Solution**

11. Consider a two-dimensional array $A$ of size $n x n$ filled with integers. In the array each row is sorted in ascending order and each column is also sorted in ascending order. Our goal is to determine if a given value x exists in the array. Design a divide-and-conquer algorithm to solve this problem and state the runtime of your algorithm. Don’t just call binary search on each row or column. Your algorithm should take strictly less than $O(n^2)$ time to run.
	> - **Solution**

12. Improve your divide-and-conquer algorithm from Exercise 10 to run in $\Theta(n)$ time.
	> - **Solution**

13. A polygon is called convex if all its internal angles are less than 180°. A convex polygon is represented as an array V with n vertices of the polygon, where each vertex is in the form of a coordinate pair $(x, y)$. We are told that $V[1]$ is the vertex with the least x coordinate and that the vertices $V[1],V [2], …, V[n]$ are ordered counter-clockwise. Design a divide-and-conquer algorithm to find the vertex with the largest x-coordinate. Discuss its worst-case runtime complexity.
	> - **Solution**
	