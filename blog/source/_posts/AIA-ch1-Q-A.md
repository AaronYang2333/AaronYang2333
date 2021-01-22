---
title: $$[Algorithms \, In \, Action]-CH1\,Review$$
catalog: true
mathjax: true
date: 2021-01-21 11:03:51
subtitle:
header-img:
tags:
categories:
---

For any monotonic functions, *f*, *g* from the positive integers to the positive integers, we say **f(n) = O(g(n))** or **f(n) = Ω(g(n))** or **f(n) = Θ(g(n))**

### Concepts
  - **T(n)** counts the \# of steps, where *n* is the input size.
  - **O** big O, $$\exists \quad c $$ which *c* > 0 and real number $${n_0}$$, has $$f(n) 	\leqslant c \cdot g(n)$$, for all  $$n \geqslant {n_0}$$.
  - **Ω** big Omega, $$\exists \quad c $$ which *c* > 0 and real number $${n_0}$$, has $$f(n) 	\geqslant c \cdot g(n)$$, for all  $$n \geqslant {n_0}$$.
  - **Θ** big Theta, $$\exists \quad {c_1} \quad and \quad {c_2} $$ which $${c_1}$$ > 0 and $${c_2}$$ > 0 and real number $${n_0}$$, has $${c_1} \cdot g(n) \leqslant f(n)	\leqslant {c_2} \cdot g(n)$$, for all  $$n \geqslant {n_0}$$.
  
### Theorems
  - *G = (V, E), the following statements are equivalent:*
    > 1. G is a tree.
    > 2. Every two vertices of G are connected by a unique path
    > 3. G is connected and V = E + 1
    > 4. G is acyclic and V = E + 1
    > 5. G is acyclic and if any two non-adjacent vertices are joined by an edge, the resulting graph has exactly one cycle. 
  - *In an undirected simple graph G = (V, E), there are at most $$\frac{V \cdot (V - 1)}{2}$$ edges. In short, by using the asymptotic notation, $$E = O(V^2)$$.*
  - *three way to traversal a graph:*
    > 1. depth-first-search
    > 2. breadth-first-search
    > 3. topological sort
      - the result of topological sort is not unique
  -  *If G is a connected planar graph with V vertices, E edges, and F faces, then V - E + F = 2*
    > - faces represent disjoint area.
  - *In any simple connected planar graph with at least 3 vertices, $$E < 3 \cdot V - 6$$*
  - *A simple connected planar graph with at least 3 vertices has a vertex of degree 5 or less.*
  - *[Coloring Planar Graph] every planar graph can be colored with at most six colors.*
  - *A graph is bipartite if and only if it dose not contain an odd length cycle.*
  - *A connected graph G is a Eulerian graph if and only if all vertices of G are of even degree*

### Review Q&A
1. Mark the following assertions as TRUE or FALSE. No need to provide any justification.
  - a. $$n = O(n^2)$$
    > - True. since $$f(n) = n \, and \, g(n) = n^2 $$ and this is big O annotation, which requires $$f(n) 	\leqslant c \cdot g(n)$$ when  $$n \geqslant {n_0}$$. In the issue, $$n <= c \cdot n^2$$, meets the requirements, so it is correct.
  - b. $$n = O( \sqrt[2]{n})$$
    > - False. $$n >= c \cdot \sqrt[2]{n}$$ should use Ω
  - c. $$log(n) = Ω(n)$$
    > - False. $$log(n) <= c \cdot n$$ should use O
  - d. $$n^2 = \Omega(n \cdot log(n))$$
    > - True. $$n^2 >= c \cdot n \cdot log(n)$$
  - e. $$n^2 \cdot log(n) = \Theta(n^2)$$
    > - False. $$n^2 \cdot log(n) >= n^2 $$ should use $$\Omega$$
  - f. $$7 \cdot (log(n))^2 + 2n \cdot log(n) = Ω(log(n))$$
    > - True. let $$A = log(n)$$, so we have $$7A^2 + 2 \cdot n \cdot A >= A$$
  - g. $$5n \cdot log(n) + 1024 n \cdot log(log(n)) = Θ(n \cdot log(n))$$
    > - True
  - h. $$2^n + 100 \cdot n^2 + n^{100}= O(n^{101})$$
    > - False
  - i. $$(1/3)^n + 100 = O(1)$$
    > - True
2. **(T/F)** Any function which is $$Ω(log(n))$$ is also $$Ω(log(log(n)))$$.
  > - True
3. **(T/F)** If f(n) = Θ(g(n)) then g(n) = Θ(f(n))
  > - True
4. **(T/F)** If f(n) = Θ(g(n)) then f(n) = Ω(g(n)).
  > - True
5. **(T/F)** If f(n) = Ω(g(n)) then $$2^{f(n)} = Ω(2^{g(n)})$$.
  > - True
6. **(T/F)** BFS can be used to find the shortest path between any two nodes in a non-weighted graph.
  > - True
7. **(T/F)** A DFS tree is never the same as a BFS tree.
  > - False.
8. **(T/F)** Algorithm A has a running time of $$O(n^2)$$ and algorithm B has a running time of $$O(n \cdot log(n)).$$ From this we conclude that A can never run faster than B on the same input.
  > - False.
9. **(T/F)** Planar graph is a sparse graph.
  > - True
10. **(T/F)** Every DAG contains a vertex with no incoming edges.
  > - True

### Exercise Q&A

