---
title: $$[Algorithms \, In \, Action]-CH4\, Greedy \,\, Algorithms$$
catalog: true
mathjax: true
date: 2021-02-15 22:01:43
subtitle:
header-img: cruves.png
tags:
- Review
- Greedy Algorithm
- Q&A
categories:
- CSCI 570
---

### Minimum Spanning Trees
#### Kruskal's Algorithm
> <img src="Kruskal.png"  style="display:inline;box-shadow: none !important;">

#### Prim's Algorithm
> **Complexity**
>> <img src="Prim.png"  style="display:inline;box-shadow: none !important;">

#### Dijkstra's Algorithm
> sada

#### Huffman Tree

### Review Q&A
1. **(T/F)** In the interval scheduling problem, if all intervals are of equal size, a greedy algorithm based on earliest start time will always select the maximum number of compatible intervals.
	> - **False**
	> - we need to sort by the finish time first and then find the compatible intervals.

2. **(T/F)** Any weighted undirected graph with distinct edge weights has exactly one minimum spanning tree.
	> - **False**
	> - maybe differnt order.

3. **(T/F)** Suppose we have a graph where each edge weight value appears at most twice. Then, there are at most two minimum spanning trees in this graph.
	> - **False**
	> - maybe some points are unreachable.

4. **(T/F)** Kruskal’s algorithm can fail in the presence of negative cost edges.
	> - **False**
	> - it should work.

5. **(T/F)** If a connected undirected graph $$G = (V, E)$$ has $n = |V|$ vertices and $n + 5$ edges, we can find the minimum spanning tree of $$G$$ in $O(n)$ runtime.
	> - **False**
	> - neither Kruskal nor Prim can do that.

6. **(T/F)** The first edge added by Kruskal’s algorithm can be the last edge added by Prim’s algorithm.
	> - **True**
	> - possible

7. **(T/F)** Suppose graph $$G$$ has a unique minimum spanning tree and graph $$G_1$$ is obtained by increasing the weight of every edge in $$G$$ by 1. The MST of $$G_1$$ must be different from the MST of $$G$$.
	> - **False**
	> - could be the same if the new added edge has a same weight of others.

8. **(T/F)** Suppose graph $$G$$ has a unique minimum spanning tree and graph $$G_1$$ is obtained by squaring the weight of every edge in $$G$$. The MST of $$G_1$$ may be different from the MST of $$G$$.
	> - **True**
	> - square a negative num result in a positive integer.

9. **(T/F)** If path $P$ is the shortest path from $u$ to $v$ and $w$ is a node on the path, then the part of path $P$ from $u$ to $w$ is also the shortest path.
	> - **False**
	> - maybe not

10. **(T/F)** If all edges in a connected undirected graph have distinct positive weights, the shortest path between any two vertices is unique.
	> - **False**
	> - maybe there are some edges have same weight.

11. **(T/F)** Suppose we have calculated the shortest paths from a source to all other vertices. If we modify the original graph $$G$$ such that weights of all edges are doubled, then the shortest path tree of $$G$$ is also the shortest path tree of the modified graph.
	> - **True**
	> - dont know

12. **(T/F)** Suppose we have calculated the shortest paths from a source to all other vertices. If we modify the original graph, $$G$$, such that weights of all edges are increased by 2, then the shortest path tree of $$G$$ is also the shortest path tree of the modified graph.
	> - **True**
	> - dont know

### Exercise Q&A
1. At the Perfect Programming Company, the programmers are paired in order to ensure the highest quality of produced code. The productivity of each pair is the speed of the slowest programmer. Assuming an even number of programmers, devise an efficient algorithm for pairing them up so the total productivity of all programmers is maximized.
	> - **Solution**
	>> **A simple greedy algorithm works for this problem.** Sort the speeds of the programmers in decreasing order using an optimal sorting algorithm such as merge sort. Consecutive sorted programmers are then paired together starting with pairing the fastest programmer with the second fastest programmer. <br>
	>> Sorting takes $O(n \cdot log(n))$ time while pairing the programmers takes $O(n)$ time giving a total running time of O(n lg n). <br>
	>> Correctness: Let $P$ be the set of programmers. The problem exhibits an optimal substructure. Assume the optimal pairing. Given any pair of programmers $(i, j)$ in the optimal pairing, the optimal sum of productivity is just the sum of the productivity of $(i, j)$ with the optimal sum of the productivity of the all pairs in $P − {i, j}$. <br>
	>>  We now show that the greedy choice works by showing that there exists an optimal pairing such that the two fastest programmers are paired together. Assume an optimal pairing where fastest programmer $i$ is not paired with the second faster programmer $j$. Instead let $i$ be paired with $k$ and $j$ be paired with $l$. Let $p_i$ , $p_j$ , $p_k$ and $p_l$ be the programming speeds of $i$, $j$, $k$ and $l$ respectively. We now change the pairings by pairing $i$ with $j$ and $k$ with $l$. The change in the sum of productivities is <center>$$(p_j + min(p_k, p_l)) − (p_k + p_l) ≥ 0$$</center> since $p_j$ is at least as large as the larger of $p_k$ and $p_l$ . We now have an optimal pairing where the fastest programmer is paired with the second fastest programmer. Hence to find the optimal solution, we can keep pairing the two fastest remaining programmers together.

2. A new startup, FastRoute, wants to route information along a path in a communication network, represented as a graph. Each vertex represents a router and each edge a wire between routers. The wires are weighted by the maximum bandwidth they can support. FastRoute comes to you and asks you to develop an algorithm to find the path with maximum bandwidth from any source $s_1, \, s_2, \, …, \, s_k$ to any destination $t_1, \, t_2, \, …, \, t_n$. Devise an algorithm that has the same runtime complexity as Dijkstra’s algorithm.
	> - **Solution**
	>> Data structure change: we’ll use a max heap instead of a min heap used in Dijkstra Algorithm.<br>
	>> Initialization of the min heap. Initially all nodes will have a distance (bandwidth) of zero from $s$, except the starting point $s$ which will have a bandwidth of $\infty$ to itself.<br>
	>> Change in relaxation step. Based on the definition of a path’s bandwidth, the bandwidth of a path from $s$ to $u$ through $u$’s neighbor $v$ will be $d(u) = min( d(v)$,  $weigth(v,u) )$, because the bandwidth of a path is equal to the bandwidth of its lowest bandwidth edge. Therefore, in the relaxation step, we will be replacing:<br>
	>> $d(u) = min (d(u), d(v) + weigth(v,u))$<br>
	>> with<br>
	>> $d(u) = max (d(u), min (d(v) , weigth(v,u))$<br>

3. You are given a set $S$ of $n$ points, labeled $1$ to $n$, on a line. You are also given a set of $k$ finite intervals $I_1, \, …, \, I_k$, where each interval $I_i$, is of the form $[s_i, e_i]$, $I \leq s_i \leq e_i$. Present an efficient algorithm to find the smallest subset $X \subseteq S$ of points such that each interval contains at least one point from $X$. Prove that your solution is optimal.
	> - **Solution**
	>> Sort the intervals in increasing order of $e_i$ . Select the first point as the right end-point of the first interval in this order. Remove all intervals which intersect with this point, and repeat. Proof of correctness is similar to the interval scheduling problem discussed in class. If the algorithm picks points $p_1 < p_2 < · · · < p_k$, and optimum solution picks points $q_1 < q_2 < · · · , q_s$, then prove by induction that $p_i ≥ q_i$ , and so $k ≤ s$.

4. You are given a minimum spanning tree $T$ in a graph $G = (V, E)$. Suppose we remove an edge from $G$, creating a new graph, $G_1$. Assuming that $G_1$ is still connected, devise a linear time algorithm to find an MST in $G_1$.<img src="lecture.png"  style="width:30px;display:inline;box-shadow: none !important;">
	> - **Solution**
	>> Once we delete an edge from $T$, the tree becomes disconnected. We need to find the minimum weight edge that connects two componets, say $T_1$ and $T_2$. Pick any component say $T_2$ and find all edges going to $T_1$. Among them choose the one which has the smallest cost. Runtime: $O(E)$.

5. You are given a minimum spanning tree $T$ in a graph $G = (V, E)$. Suppose we add a new edge (without introducing any new vertices) to $G$, creating a new graph, $G_1$. Assuming that $G_1$ is still connected, devise a linear time algorithm to find an MST in $G_1$.<img src="lecture.png"  style="width:30px;display:inline;box-shadow: none !important;">
	> - **Solution**
	> <img src="e5.png"  style="display:inline;box-shadow: none !important;">

6. Given graph $G = (V, E)$ with positive edge weights, we know that Dijkstra’s algorithm can be implemented in $O((E + V) \cdot log(V))$ time using a binary heap. Suppose you have been told that the input graph $G$ is a dense graph in which $E = O(V^2)$. Find a way to implement Dijkstra’s algorithm in $O(V^2)$ time.
	> - **Solution**
	> - **O(n)**
7. Given a graph, $G = (V, E)$, whose edge weights are integers in the range $[0, W]$, where $W$ is a relatively small integer number, we could run Dijkstra’s algorithm to find the shortest distances from the start vertex to all other vertices. Design a new algorithm that will run in linear time $O(V + E)$ and therefore outperform Dijkstra’s algorithm.
	> - **Solution**
	> - **O(n)**
8. Given a directed acyclic graph, $G = (V, E)$, with nonnegative edge weights and the source $s$, devise a linear time algorithm to find the shortest distances from $s$ to all other vertices.
	> - **Solution**
	> - **O(n)**
9. You are given a graph, $G = (V, E)$, with nonnegative edge weights and the shortest path distances $d(s, u)$ from a source vertex $s$ to all other vertices in $G$. However, you are not given the shortest path tree. Devise a linear time algorithm to find a shortest path from $s$ to a given vertex $t$.
	> - **Solution**
	>> Reverse edges in the original graph. This could be done in linear time (for example, using matrix transform). For all vertices that are connected to a given vertex $t$, find ones such that $d(s, t) = d(s, u) + d(u, t)$. Next, set $u$ as $t$ and repeat this to find new $u$ until $s$ equals to $u$. Nodes saved in the sequence are the shortest path from $s$ to a given vertex $t$.

10. Given a graph, $G = (V, E)$, with nonnegative edge weights and two vertices s and t, the goal is to find the shortest path from $s$ to $t$ with an odd number of edges. Devise an algorithm that has the same runtime complexity as Dijkstra’s algorithm.
	> - **Solution**
	> - **O(n)**
11. Given a graph,$G = (V, E)$, with nonnegative edge weights and the shortest path distances $d(u, v)$ between any pair of vertices in $G$, suppose we add a new edge (without introducing any new vertices) to $G$, creating a new graph $G_1$. Devise an efficient algorithm (that outperforms Dijkstra’s algorithm in the worst case) to update the shortest path distances $d(u, v)$.
	> - **Solution**
	> - **O(n)**
12. Given $n$ rods of lengths $L_1, L_2, …, L_n$, respectively, the goal is to connect all the rods to form a single rod. The length and the cost of connecting two rods are equal to the sum of their lengths. Devise an algorithm to minimize the cost of forming a single rod. 
	> - **Solution**
	> - **O(n)**

13. Given a sorted array of frequencies of size $n$, devise a linear time algorithm for building a Huffman tree.
	> - **Solution**
	> - **O(n)**