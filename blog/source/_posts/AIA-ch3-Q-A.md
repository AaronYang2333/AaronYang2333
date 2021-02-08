---
title: $$[Algorithms \, In \, Action]-CH3\, Heap$$
catalog: true
mathjax: true
date: 2021-02-06 23:08:15
subtitle:
header-img: cruves.png
tags:
- Review
- Heap
- Q&A
categories:
- CSCI 570
---


### Review Q&A
1. What is the worst-case runtime complexity of finding the smallest item in a binary min-heap?<img src="lecture.png"  style="width:30px;display:inline;box-shadow: none !important;">
	> - **Solution**
	> - **O(1)**

2. What is the worst-case runtime complexity of finding the largest item in a binary min-heap?
	> - **Solution**
	> - **O(n)**

3. How many binomial trees does a binomial heap with 31 elements contain?
	> - **Solution**
	> - "Having this in mind, we always will assume in the worst-case analysis that there are $O(log(n))$ binomial trees in a binomial heap with n nodes." --Chpater 3 [3.2.0]
	> $O(log(31)) = 6$

4. How many binomial trees are in a binomial heap of size n?
	> - **Solution**
	> - $O(log(n))$

5. What is the worst-case runtime complexity of inserting into a binomial heap?
	> - **Solution** => $O(1)$
	> <img src="heap_table.png"  style="display:inline;box-shadow: none !important;">
6. What is the worst-case runtime complexity of searching in a binomial heap?
	> - **Solution** => $O(n)$

7. What is the amortized cost of inserting into a binomial heap?
	> - **Solution** => $O(1)$

8. What is the worst-case runtime complexity of deleteMin() from a binomial heap?
	> - **Solution** => $O(log(n))$

9. **(T/F)** The following array is a max heap: [10, 3, 5, 1, 4, 2].
	> - **False**
	
10. **(T/F)** In a binary max-heap with n elements, the worst-case runtime complexity of finding the second largest element is O(1).
	> - **True**

11. **(T/F)** If item A is an ancestor of item B in a heap then it must be the case that the insert(A) operation occurred before insert(B).
	> - **False**
	> - abcd
12. **(T/F)** Using a binary heap we can sort any array of size n in O(n) time.
	> - **False**
	> - abcd
13. **(T/F)** In a binomial min-heap with n elements, the worst-case runtime complexity of finding the smallest element is O(1).
	> - **False**
	> - abcd
14. **(T/F)** In a binomial min-heap with n elements, the worst-case runtime complexity of finding the second smallest element is O(1).
	> - **False**
	> - abcd
15. **(T/F)** By using a binomial heap we can sort data of size n in O(n) time.
	> - **False**
	> - abcd
16. **(T/F)** Given a Fibonacci heap of size n, the maximum number of trees is that heap is n.
	> - **False**
	> - abcd

### Exercise Q&A
1. Given a sequence of numbers, 3, 5, 2, 8, 1, 5, 2,
	- a. draw a binary min-heap (in an array form) by inserting these numbers, reading them from left to right; and
	- b. show an array that would be the result after the call to deleteMi() on this heap

  > - **Solution**
	
2. Devise an algorithm of merging two binary heaps. What is its runtime complexity?
	> - **Solution**
	> - abcd
3. Suppose you have two binary min-heaps, A and B, with a total of n elements between them. You want to discover if A and B have a key in common. Devise an algorithm to this problem that takes O(n log n) time.
	> - **Solution**
	> - abcd
4. The values 1, 2, 3, …, 63 are all inserted (in any order) into an initially empty minheap. What is the smallest number that could be a leaf node?
	> - **Solution**
	> - abcd

5. Prove that it is impossible construct a min-heap (not necessarily binary) in a comparison-based model with both the following properties:
	- a. deleteMin() runs in O(1)
	- b. buildHeap() runs in O(n), where n is the input size.

  > - **Solution**
  > - abcd

6. Given an unsorted array of size n, devise a heap-based algorithm that finds the k-th largest element in the array. What is its runtime complexity?
	> - **Solution**
	> - abcd
7. Recall that two sorted arrays of size n can be merged into a single sorted list in linear time O(n). Suppose there are k > 2 sorted arrays, each of size n. Devise a heap-based algorithm that merges k arrays and requires at most O(k) extra space.
	> - **Solution**
	> - abcd
8. Given a stream of data (its size is unknown in advance), devise a heap-based algorithm that finds the k-th largest element in the array. Your algorithm must take at most O(k) extra space. What is its runtime complexity?
	> - **Solution**
	> - abcd
9. Given a stream of data (its size is unknown in advance), devise a heap-based algorithm that finds the median of elements read so far. What is its runtime complexity?
	> - **Solution**
	> - abcd
10. Given a sequence of numbers, 3, 5, 2, 8, 1, 5, 2, 7,
	- a. draw a binomial heap by inserting these numbers, reading them from left to right; and
	- b. show a heap that would be the result after the call to deleteMin() on this heap.

	> - **Solution**
	> - abcd

11. Discuss the relationship between inserting into a binomial heap and binary increment.
	> - **Solution**
	> - abcd
12. Discuss the relationship between merging two binomial heaps and adding two binary numbers.
	> - **Solution**
	> - abcd
13. Discuss the relationship between inserting into a binomial heap and a Fibonacci heap.
	> - **Solution**
	> - abcd
14. Devise an algorithm of deleting any item from a binomial heap. What is its runtime complexity?
	> - **Solution**
	> - abcd
15. Devise an algorithm to find all nodes less than some given value X in a binomial heap. Analyze its complexity.
	> - **Solution**
	> - abcd