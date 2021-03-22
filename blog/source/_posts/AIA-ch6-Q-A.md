---
title: $$[Algorithms \, In \, Action]-CH6\, Dynamic \,\, Programming $$
catalog: true
mathjax: true
date: 2021-03-20 05:47:31
subtitle:
header-img: cruves.png
tags:
- Review
- Dynamic Programming
- Q&A
categories:
- CSCI 570
---


### Review Q&A
1. **(T/F)** If a dynamic programming algorithm has n subproblems, then its running time complexity is W(n).
	> - **False**

2. **(T/F)** It is possible for a dynamic programming algorithm to have an exponential runtime complexity.
	> - **False**

3. **(T/F)** In a dynamic programming formulation, the subproblems must be mutually independent.
	> - **False**

4. **(T/F)** A pseudo-polynomial time algorithm is always asymptotically slower than a polynomial time algorithm.
	> - **False**

5. **(T/F)** If a dynamic programming solution is set up correctly (i.e., the recurrence equation is correct) and each unique sub-problem is solved only once, then the resulting algorithm will always find the optimal solution in polynomial time.
	> - **False**

6. **(T/F)** If a problem can be solved by divide and conquer, then it can always be solved by dynamic programming.
	> - **False**

7. **(T/F)** If a problem can be solved by dynamic programming, then it can always be solved by exhaustive search.
	> - **False**

8. **(T/F)** The Bellman-Ford algorithm always fails to find the shortest path between two nodes in a graph if there is a negative cycle present in the graph.
	> - **False**

9. **(T/F)** In a dynamic programming solution, the space requirement is always at least as big as the number of unique sub problems.
	> - **False**

10. **(T/F)** In a connected, directed graph with positive edge weights, the BellmanFord algorithm runs asymptotically faster than the Dijkstra algorithm.
	> - **False**

11. **(T/F)** The dynamic programming for the knapsack problem runs in polynomial time.
	> - **False**

12. **(T/F)** The longest simple path can be computed by negating the weights of all the edges in the graph and then running the Bellman-Ford algorithm.
	> - **False**
	
13. **(T/F)** There exist some problems that can be solved by dynamic programming but cannot be solved by greedy algorithms.
	> - **False**

14. **(T/F)** The Bellman-Ford algorithm always finds the shortest path in undirected graphs.
	> - **False**

15. Which of the following standard algorithms are solved using dynamic programming?
	a. Bellman-Ford’s algorithm
	b. Dijkstra’s algorithm
	c. Prim’s algorithm
	d. Karatsuba’s algorithm
	> - **False**


### Exercise Q&A


1. Design a DP algorithm that solves the 0-1 knapsack problem, which allows repetitions (i.e., assume that there are unlimited quantities of each item available). What is its space complexity?
	> - **Solution**

2. Design a DP algorithm that takes a string and returns the length of the longest palindromic subsequence. A subsequence of a string is obtained by deleting zero or more symbols from that string. A subsequence is palindromic if it reads the same left and right. For example, the string QRAECCETCAURP has several palindromic subsequences, but the longest one is RACECAR.
	> - **Solution**

3. Given a non-empty string $str$ and a dictionary containing a list of unique words, design a dynamic programming algorithm to determine if $str$ can be segmented into a sequence of dictionary words. For example, if $str$ =“algorithmdesign” and your dictionary contains “algorithm” and “design,” then your algorithm should answer yes since str can be segmented to “algorithm” and “design.” You may assume that a dictionary lookup can be done in $O(1)$ time.
	> - **Solution**

4. You are given $n$ balloons, indexed from $0$ to $n - 1$, where each balloon is painted with a number on it represented by array $nums$. You are asked to burst all the balloons. If you burst balloon i you will get $nums[left] · nums[i] · nums[right]$ coins. Here, left and right are adjacent indices of $i$. After the burst, the left and right then becomes adjacent. You may assume $nums[-1] = nums[n] = 1$, and they are not real; therefore, you cannot burst them. For example, if you have the $nums = [3, 1, 5, 8]$, the optimal solution would be $167$, where you burst balloons in the order of $1, 5, 3$ and $8$. The array nums after each step is $[3, 1, 5, 8] \rightarrow [3, 5, 8] \rightarrow [3, 8] \rightarrow [8] \rightarrow []$. Design a dynamic programming algorithm to find the maximum coins you can collect by bursting the balloons. Analyze the running time of your algorithm.
	> - **Solution**

5. A rope has length of $n$ units, where $n$ is an integer. You are asked to cut the rope (at least once) into different smaller pieces $p_j$ of integer lengths so that the product of lengths of those new smaller ropes is maximized. Design a dynamic programming algorithm and analyze its running time. Explain how you would find the optimal set of cutting positions.
	> - **Solution**

6. There is a series of $n > 0$ jobs lined up one after the other. The $i_{th}$ job has a duration $t_i \in N$ units of time, and you earn $p_i \leq 0$ amount of money for doing it. Also, you are given the number $s_i \in N$ of immediately following jobs that you cannot take if you perform that $i_{th}$ job. Design a dynamic programming algorithm to maximize the amount of money one can make in $T$ units of time.
	> - **Solution**

7. You are to compute the minimum number of coins needed to make change for a given amount $m$. Assume that we have an unlimited supply of coins. All denominations $d_k$ are sorted in ascending order: $1 = d_1 < d_2 < … < d_n$. Design a dynamic programming algorithm to minimize the amount of coins.
	> - **Solution**

8. Given an unlimited supply of coins of denominations $d_1 < d_2 < … < d_n$, we wish to make change for an amount $m$. This might not be always possible. Your goal is to verify if it is possible to make such change. Design an algorithm by reduction to the knapsack problem.
	> - **Solution**

9. There are two strings: string $S$ of length $n$, and string $T$ of length $m$. Design a dynamic programming algorithm to compute their longest common subsequence. A subsequence is a subset of elements in the sequence taken in order (with strictly increasing indexes.)
	> - **Solution**

10. A polygon is called convex if all its internal angles are less than 180°. A convex polygon is represented as an array $V$ with $n$ vertices in counterclockwise order, where each vertex is in the form of a coordinate pair $(x, y)$. Given is a convex polygon, we would like to triangulate this polygon (i.e., decompose it into disjoint triangles by adding line segments (diagonals) between its corners (vertices)). Design a dynamic programming algorithm for triangulating a convex polygon while minimizing the total perimeter of all the triangles.
	> - **Solution**
	
11. Given a row of $n$ houses that can each be painted red, green, or blue with a cost $P(i, c)$ for painting house $i$ with color $c$, design a dynamic programming algorithm to find a minimum cost coloring of the entire row of houses such that no two adjacent houses are the same color.
	> - **Solution**
	
12. A tourism company is providing boat tours on a river with $n$ consecutive segments. According to previous experience, the profit they can make by providing boat tours on segment $i$ is known as $a_i$. Here, $a_i$ could be positive (they earn money), negative (they lose money), or zero. Because of the administration convenience, the local community requires that the tourism company do their boat tour business on a contiguous sequence of the river segments (i.e., if the company chooses segment $i$ as the starting segment and segment $j$ as the ending segment, all the segments in between should also be covered by the tour service, no matter whether the company will earn or lose money). The company’s goal is to determine the starting segment and ending segment of boat tours along the river, such that their total profit can be maximized. Design a dynamic programming algorithm to achieve this goal and analyze its runtime.
	> - **Solution**
	
13. You have two rooms to rent out. There are $n$ customers interested in renting the rooms. The $i_{th}$ customer wishes to rent one room (either room you have) for $d[i]$ days and is willing to pay $bid[i]$ for the entire stay. Customer requests are nonnegotiable in that they would not be willing to rent for a shorter or longer duration. Design a dynamic programming algorithm to determine the maximum profit that you can make from the customers over a period of $D$ days.
	> - **Solution**
	
14. You are to plan the fall 2025 schedule of classes. Suppose that you can sign up for as many classes as you want, and you’ll have infinite amount of energy to handle all the classes, but you cannot take two classes at the same time. Also assume that the problem reduces to planning your schedule for one particular day. Thus, consider one day of the week and all the classes happening on that day: $c_1, …, c_n$. Associated with each class $c_i$ is a start time $s_i$ and a finish time $f_i$ such that $s_i < f_i$. Also, there is a score $v_i$ assigned to that class, $c_i$, based on your interests and your program requirement. You would like to choose a set of courses for that day to maximize the total score. Design a dynamic programming algorithm for planning your schedule.
	> - **Solution**
	

15. There are $n$ trading posts along a river numbered $n, n - 1 …, 1$. At any of the posts you can rent a canoe to be returned at any other post downstream. (It is impossible to paddle against the river.) For each possible departure point $i$ and each possible arrival point $j < i$, the cost of a rental is $C[i, j]$. However, it can happen that the cost of renting from $i$ to $j$ is higher than the total costs of a series of shorter rentals. In this case you can return the first canoe at some $+post \,\, k$ between $i$ and $j$ and continue your journey in a second (and, maybe, third, fourth, and so on) canoe. There is no extra charge for changing canoes in this way. Design a dynamic programming algorithm to determine the minimum cost of a trip by canoe from each possible departure point $i$ to each possible arrival point $j$. Analyze the running time of your algorithm in terms of $n$.
	> - **Solution**
	
16. Given a weighted directed acyclic graph $G = (V, E)$ in which we allow negative edge weights, design a dynamic programming algorithm to find the longest simple path between two given vertices. 
	> - **Solution**
	
17. Design a dynamic programming algorithm for counting the number of paths between two given vertices in a $DAG$.
	> - **Solution**
	