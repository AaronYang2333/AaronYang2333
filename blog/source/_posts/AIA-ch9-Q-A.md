---
title: $$[Algorithms \, In \, Action]-CH7\, NP  \,\, Completeness $$
catalog: true
mathjax: true
date: 2021-04-20 05:47:29
subtitle:
header-img:
tags:
- Review
- NP Completeness
- Q&A
categories:
- CSCI 570
---

### Review Q&A
1. What is an algorithm?
	> - **Solution**

2. What is the Church–Turing thesis?
	> - **Solution**

3. What is a decision problem?
	> - **Solution**

4. What is an undecidable problem?
	> - **Solution**

5. What is the Halting problem?
	> - **Solution**

6. What is the  versus NP conjecture?
	> - **Solution**

7. (T/F) If someone proves  = NP, then it would imply that every decision problem can be solved in polynomial time.
	> - **False**
	
8. (T/F) Any problem in  is also in NP.
	> - **False**
	
9. (T/F) Every decision problem is in NP.
	> - **False**
	
10. (T/F) Every problem in NP can be solved in exponential time by a deterministic Turing machine.
	> - **False**
	
11. (T/F) All NP-hard problems are in NP.
	> - **False**
	
12. (T/F) If a problem X can be reduced to linear programming in polynomial time, then X is in .
	> - **False**
	
13. (T/F) If SAT £p A, then A is NP-hard.
	> - **False**
	
14. (T/F) If 3-SAT £p 2-SAT, then  = NP.
	> - **False**
	
15. (T/F) If a problem Y £p X, then it follows that X £p Y.
	> - **False**
	
16. (T/F) If A £p B and B is in NP, then A is in NP.
	> - **False**
	
17. (T/F) If a problem X can be reduced to a known NP-hard problem, then X must be NP-hard.
	> - **False**
	
### Exercise Q&A
1. Prove that any optimization problem can be converted into a decision problem and vice versa.
	> - **Solution**

2. Prove that if A £p B and B Î NP then A Î NP.
	> - **Solution**

3. Prove that if A £p B and B £p C then A £p C.
	> - **Solution**

4. Prove that if Z £p Y and Y £p X then Z £p X.
	> - **Solution**

5. Prove that the Halting problem is in NP-hard class.
	> - **Solution**

6. Assume that you are given a polynomial time algorithm that given a 3-SAT instance decides in polynomial time if it has a satisfying assignment. Describe a polynomial time algorithm that finds a satisfying assignment (if it exists) to a given 3-SAT instance.
	> - **Solution**

7. Assume that you are given a polynomial time algorithm that decides if a directed graph contains a Hamiltonian cycle. Describe a polynomial time algorithm that outputs a sequence of vertices (in order) that form a Hamiltonian cycle.
	> - **Solution**

8. Prove by reduction from 3-SAT that an integer linear program is NP-complete.
	> - **Solution**

9. The vertex cover problem (VC, in short) is to decide, for a given undirected graph G and natural number k > 0, whether G has a vertex cover of size k. Prove that VC is in NP-complete class by reduction from 3-SAT. No other reductions can be used.
	> - **Solution**

10. You are given a set S of n people and a set L of pairs of people that are mutually friends. Can these n people be seated for dinner around a circular table such that each person will sit next to friends on both sides? Prove that the problem (in short, DINNER) of finding such a sitting arrangement is NP-complete.
	> - **Solution**

11. Consider the 5-COLOR problem of deciding whether all vertices in undirected graph G can be colored with 5 colors so that any two adjacent vertices are colored differently. Prove that 5-COLOR is NP-complete by reducing from 3-COLOR.
	> - **Solution**

12. You are given an undirected connected graph G = (V, E) in which a certain number of tokens t(v) ³ 1 placed on each vertex v. You will now play the following game. You pick a vertex u that contains at least two tokens, remove two tokens from u, and add one token to any one of adjacent vertices. The objective of the game is to perform a sequence of moves such that you are left with exactly one token in the whole graph. You are not allowed to pick a vertex with a 0 or 1 token. Prove that the problem of finding such a sequence of moves is NP-complete by reduction from the Hamiltonian path.
	> - **Solution**

13. We want to become celebrity chefs by creating a new dish. There are n ingredients and we’d like to use as many of them as possible. However, some ingredients don’t go so well with others. There is n ´ n matrix D giving discord between any two ingredients, where D[i, j] is a real value between 0 and 1. Any dish prepared with these ingredients incurs a penalty, which is the sum of the discords between all pairs of ingredients in the dish. We would like the total penalty to be as small as possible. Consider the decision problem EXPERIMENTAL CUISINE: can we prepare a dish with at least k ingredients and with the total penalty at most p? Show that EXPERIMENTAL CUISINE is NP-complete by giving a reduction from INDEPENDENT SET.
	> - **Solution**

14. Given an undirected graph with positive edge weights, the BIG-HAM-CYCLE problem is to decide if it contains a Hamiltonian cycle C such that the sum of weights of edges in C is at least half of the total sum of weights of edges in the graph. Show that BIG-HAM-CYCLE is NP-complete by reduction from the Hamiltonian cycle.
	> - **Solution**

15. We know that finding a Hamiltonian cycle in a graph is NP-complete. Show that finding a Hamiltonian path—a path that visits each vertex exactly once and isn’t required to return to its starting point—is also NP-complete.
	> - **Solution**

16. Given a graph G = (V, E) and a positive integer k, the longest-cycle problem is the problem of determining whether a simple cycle (no repeated vertices) of length k exists in a graph. Show that this problem is NP-complete by reduction from the Hamiltonian cycle.
	> - **Solution**

17. Given a graph G = (V, E) and a positive integer k, the longest-path problem is the problem of determining whether a simple path (no repeated vertices) of length k exists in a graph. Show that this problem is NP-complete by reduction from the Hamiltonian path.
	> - **Solution**

18. You are given an undirected weighted graph G = (V, E) with positive edge costs, a subset of vertices R Í V, and a number C. Is there a tree in G that spans all vertices in R (and possibly some other in V) with a total edge cost of at most C? Prove that this problem is NP-complete by reduction from vertex cover.
	> - **Solution**
