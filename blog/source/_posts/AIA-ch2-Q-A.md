---
title: $$[Algorithms \, In \, Action]-CH2\,Amortized Analysis$$
catalog: true
mathjax: true
date: 2021-01-24 11:09:23
subtitle:
header-img: cruves.png
tags:
- Review
- Amortized Analysis
- Q&A
categories:
- CSCI 570
---

For any monotonic functions, *f*, *g* from the positive integers to the positive integers, we say **f(n) = O(g(n))** or **f(n) = Ω(g(n))** or **f(n) = Θ(g(n))**

### Concepts
  - **T(n)** counts the \# of steps, where *n* is the input size.
  - **O** big O, $$\exists \, c $$ which *c* > 0 and real number $${n_0}$$, has $$f(n) 	\leqslant c \cdot g(n)$$, for all  $$n \geqslant {n_0}$$.
  - **Ω** big Omega, $$\exists \, c $$ which *c* > 0 and real number $${n_0}$$, has $$f(n) 	\geqslant c \cdot g(n)$$, for all  $$n \geqslant {n_0}$$.
  - **Θ** big Theta, $$\exists \, {c_1} \, and \, {c_2} $$ which $${c_1}$$ > 0 and $${c_2}$$ > 0 and real number $${n_0}$$, has $${c_1} \cdot g(n) \leqslant f(n)	\leqslant {c_2} \cdot g(n)$$, for all  $$n \geqslant {n_0}$$.


### Review Q&A
1. What is the definition of the amortized cost using the aggregate method? <img src="lecture.png"  style="width:30px;display:inline;box-shadow: none !important;">
	> - **Solution**

2. (T/F) Amortized analysis is used to determine the average runtime complexity of an algorithm.
	> - **True**

3. (T/F) Compared to the worst-case analysis, amortized analysis provides a more accurate upper bound on the performance of an algorithm.
	> - **True**

4. (T/F) The total amortized cost of a sequence of n operations gives a lower bound on the total actual cost of the sequence.
	> - **True**

5. (T/F) Amortized constant time for a dynamic array is still guaranteed if we increase the array size by 5%.
	> - **True**

6. (T/F) If an operation takes O(1) expected time, then it takes O(1) amortized time.
	> - **True**

7. Suppose you have a data structure such that a sequence of n operations has an amortized cost of O(n * log n). What could be the highest actual time of a single operation?
	> - **Solution**

8. What is the worst-case runtime complexity of searching in an amortized dictionary?
	> - **Solution**

### Exercise Q&A
1. You have a stack data type, and you need to implement a FIFO queue. The stack has the usual POP and PUSH operations, and the cost of each operation is 1. The FIFO has two operations: ENQUEUE and DEQUEUE. We can implement a FIFO queue using two stacks. What is the amortized cost of ENQUEUE and DEQUEUE operations?
	> - **Solution**

2. We are incrementing a binary counter, where flipping the i-th bit costs i + 1. Flipping the lowest-order bit costs 0 + 1 = 1, the next bit costs 1 + 1 = 2, the next bit costs 2 + 1 = 3, and so on. What is the amortized cost per operation for a sequence of n increments, starting from zero?
	> - **Solution**

3. We have argued in the lecture that if the table size is doubled when it’s full, then the amortized cost per insert is acceptable. Fred Hacker claims that this consumes too much space. He wants to try to increase the size with every insert by just two over the previous size. What is the amortized cost per insertion in Fred’s table?
	> - **Solution**

4. This table supports inserts as well as deletions. The protocol is the following: If an array is full, we double its size on insertion; if an array is 1/4 full, we halve the array size on deletion. Show that the amortized cost of insert and delete is 5.
	> - **Solution**

5. Suppose we perform a sequence of n operations on a data structure in which the i-th operation costs i if i is an exact power of 2 and 1 otherwise. Use aggregate analysis to determine the amortized cost per operation.
	> - **Solution**

6. Suppose we perform a sequence of n operations on a data structure in which the i-th operation costs i if i is an exact power of 4 and 1 otherwise. Use aggregate analysis to determine the amortized cost per operation.
	> - **Solution**

7. A MultiStack data structure has the usual POP and PUSH operations, and the cost of each operation is one unit. Additionally, it has MULTIPOP(k) operation that removes k recently pushed items. If k is bigger than the stack size, it removes all items. We wish to analyze the running time for a sequence of n PUSH, POP, and MULTIPOP operations, starting with an empty stack. What is the worst-case complexity for a sequence of n operations? What is the amortized cost per operation? Use the accounting method.
	> - **Solution**

8. Consider a singly linked list as a dictionary that we always insert at the beginning of the list. Now assume that you may perform any number of insert operations but will only ever perform at most one lookup operation. What is the amortized cost per operation?
	> - **Solution**
	