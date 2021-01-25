---
title: $$[Algorithms \, In \, Action]-CH1\,Review$$
catalog: true
mathjax: true
date: 2021-01-21 11:03:51
subtitle:
header-img: cruves.png
tags:
- Review
- Graph
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

![as](fn_gn.png)
  
### Theorems
  - *G = (V, E), the following statements are equivalent:*<img src="lecture.png" style="width:30px;display:inline;box-shadow: none !important;">
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
1. Mark the following assertions as TRUE or FALSE. No need to provide any justification.<img src="lecture.png"  style="width:30px;display:inline;box-shadow: none !important;">
  - a. $$n = O(n^2)$$
    > - **True**. since $$f(n) = n \, and \, g(n) = n^2 $$ and this is big O annotation, which requires $$f(n) 	\leqslant c \cdot g(n)$$ when  $$n \geqslant {n_0}$$. <br>In the issue, $$n <= c \cdot n^2$$, meets the requirements, so it is correct.
  - b. $$n = O( \sqrt[2]{n})$$
    > - **False**. $$n >= c \cdot \sqrt[2]{n}$$ should use Ω
  - c. $$log(n) = Ω(n)$$
    > - **False**. $$log(n) <= c \cdot n$$ should use O
  - d. $$n^2 = \Omega(n \cdot log(n))$$
    > - **True**. $$n^2 >= c \cdot n \cdot log(n)$$
  - e. $$n^2 \cdot log(n) = \Theta(n^2)$$
    > - **False**. $$n^2 \cdot log(n) >= n^2 $$ should use $$\Omega$$
  - f. $$7 \cdot (log(n))^2 + 2n \cdot log(n) = Ω(log(n))$$
    > - **True**. let $$A = log(n)$$, so we have $$7A^2 + 2 \cdot n \cdot A >= A$$
  - g. $$5n \cdot log(n) + 1024 n \cdot log(log(n)) = Θ(n \cdot log(n))$$
    > - **True**. let $$A = log(n)$$,<br> so we have $$5 \cdot n \cdot A + 1024 \cdot n \cdot log(A) = \Theta(n \cdot A)$$. not easy to compare. but we already knew log(n) < n. <br> So $$5 \cdot n \cdot A + 1024 \cdot n \cdot log(A) < 5 \cdot n \cdot A + 1024 \cdot n \cdot A$$. <br> let $$B = n \cdot log(n) $$, we will have $$5 \cdot B + 1024 \cdot B = 1029B \, v.s. \Theta(B)$$. <br>f(n) = 1029B, g(n) = B. There exist many $${c_1} \, {c_2}$$ could meet $${c_1} \cdot g(n) \leqslant f(n)	\leqslant {c_2} \cdot g(n)$$.
  - h. $$2^n + 100 \cdot n^2 + n^{100}= O(n^{101})$$
    > - **False**. u can see the head img. $$2^n$$ grow faster than $$n^{100}$$. so left part bigger than right. <br>The statement is wrong, and should use $$\Omega$$
  - i. $$(1/3)^n + 100 = O(1)$$
    > - **False**. $$(1/3)^n$$ will going to zero when n > 0. the left part will never beat the 101. so LHS is smaller or bigger than RHS when choose different *c*. Thus the statement is wrong.
2. **(T/F)** Any function which is $$Ω(log(n))$$ is also $$Ω(log(log(n)))$$.
  > - **True**. Assume there is a f(n) >= c * log(n).<br>
  and we also knew, log(n) > log(log(n)) in any suitation. so we have f(n) >= c * log(n) > c * log(log(n)). 
3. **(T/F)** If f(n) = Θ(g(n)) then g(n) = Θ(f(n))
  > - **True**. becasue f(n) = Θ(g(n)), we have $$c_1 \cdot g(n) <= f(n) <= c_2 \cdot g(n)$$. LHS multiplt $$1 / c_1$$ => $$g(n) <= \frac{1}{c_1}f(n)$$. RHS multiplt $$1 / c_2$$ => $$\frac{1}{c_2}f(n) <= g(n)$$. <br>In all, we have $$\frac{1}{c_2}f(n) <= g(n) <= \frac{1}{c_1}f(n) \, $$ => $$\, b_1f(n) <= g(n) <= b_2f(n)$$
4. **(T/F)** If f(n) = Θ(g(n)) then f(n) = Ω(g(n)).
  > - **True**. becasue f(n) = Θ(g(n)), we have $$c_1 \cdot g(n) <= f(n) <= c_2 \cdot g(n)$$. LHS is what you need. so this is true.
5. **(T/F)** If f(n) = Ω(g(n)) then $$2^{f(n)} = Ω(2^{g(n)})$$.<img src="lecture.png"  style="width:30px;display:inline;box-shadow: none !important;">
  > - **False** prove it by contradiction. <br>
  e.g. f(n) = 2n, g(n) = 4n. when c = 0.25. f(n) >= c * g(n). <br>
  but $$2^{f(n)} = 4^n, 2^{g(n)} = 16^n$$, $$2^{f(n)} <= 2^{g(n)}$$. so this statement is wrong.
6. **(T/F)** BFS can be used to find the shortest path between any two nodes in a non-weighted graph.
  > - **True**. as the professor said. BFS find node in level order.
7. **(T/F)** A DFS tree is never the same as a BFS tree.
  > - **False**. could be the same.
8. **(T/F)** Algorithm A has a running time of $$O(n^2)$$ and algorithm B has a running time of $$O(n \cdot log(n)).$$ From this we conclude that A can never run faster than B on the same input.
  > - **False**. Big O annotation is just telling you the maximum time that your algorithm will cost. But when running in real life, the actual data could be easily handled. 
9. **(T/F)** Planar graph is a sparse graph.
  > - **False**. could be a dense graph.
10. **(T/F)** Every DAG contains a vertex with no incoming edges.
  > - **True**. DAG (directed acyclic graph) cannot has a circle.

### Exercise Q&A
1. Prove g(n) = Ω(f(n)) if and only if f(n) = O(g(n)).
  > - **Solution** To prove a theorem of the form *A IF AND ONLY IF B*, you first prove *IF A THEN B*, then you prove *IF B THEN A*, and that's enough to complete the proof. 
  >> **Proof**
  >> - $A \rightrightarrows B$
  >>> g(n) = Ω(f(n)), means g(n) >=  c \* f(n), c > 0 <br>
    we multiply 1 / c on both side, and we have $$\frac{1}{c} \cdot g((n)$$ >= f(n) which equals to <br>  f(n) <= $${b} \cdot g((n)$$, *b* > 0 , so we can say f(n) = O(g(n)).
  >> - $B \leftleftarrows A$
  >>> f(n) = O(g(n)), means f(n) <= c \* g(n), c > 0 <br>
    we multiply 1 / c on both side, and we have $$\frac{1}{c} \cdot f((n)$$ <= g(n) which equals to <br>  g(n) >= $${b} \cdot f((n)$$, *b* > 0 , so we can say g(n) = Ω(f(n)).

2. Prove or disprove f(n) = O(g(n)) implies $$2^{f(n)} = O(2^{g(n)})$$.<img src="lecture.png"  style="width:30px;display:inline;box-shadow: none !important;">
  > - **Solution** prove it by contradiction. <br>
  e.g. f(n) = 2n, g(n) = n. when c = 4. f(n) <= c \* g(n).<br> 
  but $$2^{f(n)} = 4^n, 2^{g(n)} = 2^n$$, $$2^{f(n)} >= 2^{g(n)}$$. so this statement is wrong.

3. Arrange the following functions<img src="lecture.png"  style="width:30px;display:inline;box-shadow: none !important;">
$$log(n^n),\, n^2,\, n^{log(n)},\, nlog(log(n)),\, 2^{log(n)},\, (log(n))^2,\, n^{\sqrt{2}}$$
in increasing order of growth rate, with g(n) following f(n) in your list if and only if f(n) = O(g(n)).
  > - **Solution** we can follow this order
  $O(1) <= O(log(n)) <= O((log(n))^C) <= O(C^{log(n)}) <= O(n) <= O(n \cdot log(n)) <= O(n^C) <= O((log(n))!) <= O(n^{log(n)}) <= O(C^n)$
  And we can simply some of them in first place.
  $$① \, log(n^n) = n \cdot log(n) \, ⑤ \, 2^{log_2 n} = log_2 2^n = n \cdot 1 = n$$,
  So , finally, we have <br>
  $nlog(n),\, n^2,\, n^{log(n)},\, nlog(log(n)),\, n,\, (log(n))^2,\, n^{\sqrt{2}}$ <br>
  $O(1) \Rightarrow None$
  $O(log(n)) \Rightarrow None$
  $O((log(n))^C) \Rightarrow ⑥$
  $O(C^{log(n)}) \Rightarrow None$
  $O(n) \Rightarrow ⑤$
  $O(n \cdot log(n)) \Rightarrow ①④ since \, n > log(n) \Rightarrow ④①$
  $O(n^C) \Rightarrow ②⑦ since \, \sqrt(2) < 2 \, and \, log(n)\, grow \,slower \,than \,exponential \,func $
  $\quad especially \,when \,a > 1 \, so, ⑦②$
  $O((log(n))!) \Rightarrow None$
  $O(n^{log(n)}) \Rightarrow ③$
  $O(C^n) \Rightarrow None$<br>
  the answers is: ⑥<⑤<④<①<⑦<②<③
  $(log(n))^2,\, 2^{log(n)},\, nlog(log(n)),\, log(n^n),\, n^{\sqrt{2}}, \, n^2,\, n^{log(n)}$

4. Arrange the following functions
$$4^{log(n)},\, \sqrt{log(n)},\, n^{log(log(n))},\, (\sqrt{2})^{log(n)},\, 2^{\sqrt{2log(n)}},\, n^{1/log(n)},\, (log(n))!$$
in increasing order of growth rate with g(n) following f(n) in your list if and only if f(n) = O(g(n)).
  > - **Solution** we can follow this order
  $O(1) <= O(log(n)) <= O((log(n))^C) <= O(C^{log(n)}) <= O(n) <= O(n \cdot log(n)) <= O(n^C) <= O((log(n))!) <= O(n^{log(n)}) <= O(C^n)$
  And we can simply some of them in first place.
  $$① \, 4^{log_2 n} = (2^2)^{log(n)} = 2^{2*log(n)} = 2^{log(n^2)} = log_2 2^{n^2} = n^2$$,<br>
  $$⑥ \, n^{1/log(n)} = n^{log_2 2/log_2 n} = n^{log_n 2} = 2$$,
  So , finally, we have <br>
  $n^2, \, \sqrt{log(n)},\, n^{log(log(n))},\, (\sqrt{2})^{log(n)},\, 2^{\sqrt{2log(n)}},\, 2, \, (log(n))!$ <br>
  $O(1) \Rightarrow ⑥$
  $O(log(n)) \Rightarrow None$
  $O((log(n))^C) \Rightarrow ②$
  $O(C^{log(n)}) \Rightarrow ④⑤ \quad (\sqrt{2})^{log(n)} = 2^{log(n) / 2} $
  $\quad \,we \, can \, just \, compare \, log(n) / 2 \, v.s. \sqrt{2 \cdot log(n)} \, so, ⑤④$
  $O(n) \Rightarrow None$
  $O(n \cdot log(n)) \Rightarrow None$
  $O(n^C) \Rightarrow ①$
  $O((log(n))!) \Rightarrow ⑦$
  $O(n^{log(n)}) \Rightarrow ③$
  $O(C^n) \Rightarrow None$ <br>
  the answers is: ⑥<②<⑤<④<①<⑦<③
  $(log(n))^2,\, 2^{log(n)},\, nlog(log(n)),\, log(n^n),\, n^{\sqrt{2}}, \, n^2,\, n^{log(n)}$

5. What is the Big-O runtime complexity of the following function?<img src="lecture.png"  style="width:30px;display:inline;box-shadow: none !important;">
  ```
  void bigOh1 (int n):
    for i=1 to n
      j=1;
      while j < n
        j = j*2;
  ```
  > - **Solution** $$O(n \cdot log(n))$$
  > <img src="ans_5.png"  style="display:inline;box-shadow: none !important;">

6. What is the Big-O runtime complexity of the following function?<img src="lecture.png"  style="width:30px;display:inline;box-shadow: none !important;">
  ```
  string bigOh3 (int n):
    if(n == 0) return "a";
    string str = bigOh3(n-1);
    return str + str;
  ```
  > - **Solution** $$O(n \cdot 2^n)$$
  > <img src="ans_6.png"  style="display:inline;box-shadow: none !important;">

7. What is the Big-Theta runtime complexity of the following function? Here *find_max* finds the maximum element in the array L[0], L[1], …, L[n - 1].<img src="lecture.png"  style="width:30px;display:inline;box-shadow: none !important;">
  ```
  void bigOh2 (int[] L, int n):
    while (n > 0)
      find_max(L, n);
      n = n/4;
  ```
  > - **Solution**
  > <img src="ans_7.png"  style="display:inline;box-shadow: none !important;">

8. The complete graph on n vertices, denoted $$K_n$$, is a simple graph in which there is an edge between every pair of distinct vertices. What is the height of the DFS tree for the complete graph $$K_n$$? What is the height of the BFS tree for the complete graph $$K_n$$?
  > - **Solution**

9. We are interested in finding a simple path in a directed acyclic graph that visits all vertices once and only once. Design a linear time algorithm to determine if there is such a path in a given DAG.
  > - **Solution**

10. Prove that a complete graph $$K_5$$ is not a planar graph.
  > - **Solution**

11. Prove that a complete bipartite graph $$K_{3,3}$$ is not a planar graph.
  > - **Solution**

12. In a connected bipartite graph, is the bipartition unique? Justify your answer.
  > - **Solution**

13. Given a directed graph G = (V, E) and a particular node v ∈ V, design a linear time algorithm to determine whether v is in a triangle of edges (a cycle of length 3).
  > - **Solution**

14. Design a linear time algorithm which, given an undirected graph G = (V, E) and a particular edge e ∈ E, determines whether G has a cycle containing e.
  > - **Solution**

15. Given an undirected graph G = (V, E), prove that S is an independent set if and only if V - S is a vertex cover
  > - **Solution**

