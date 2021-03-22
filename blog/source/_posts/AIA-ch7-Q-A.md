---
title: $$[Algorithms \, In \, Action]-CH7\, Network  \,\, Flow $$
catalog: true
mathjax: true
date: 2021-03-22 17:15:56
subtitle:
header-img: cruves.png
tags:
- Review
- Network Flow
- Q&A
categories:
- CSCI 570
---


### Review Q&A
1. What is a flow?
	> - **Solution**
	
2. What is a flow network?
	> - **Solution**
	
3. What is an augmenting path?
	> - **Solution**
	
4. What is the relationship between a flow value and a cut capacity?
	> - **Solution**
	
5. Among all cuts, how do you distinguish a min-cut in the residual network?
	> - **Solution**
	
6. How do you find a min-cut?
	> - **Solution**
	
7. Is a min-cut unique?
	> - **Solution**
	
8. How do you force the flow to use certain edges?
	> - **Solution**
	
9. **(T/F)** A residual network is a flow network.
	> - **False**

10. **(T/F)** The Ford–Fulkerson algorithm always terminates.
	> - **False**

11. **(T/F)** The Ford–Fulkerson algorithm is a polynomial time algorithm.
	> - **False**

12. **(T/F)** The Ford–Fulkerson algorithm is a greedy algorithm.
	> - **False**

13. **(T/F)** The Edmonds-Karp 1 algorithm is a pseudo-polynomial time algorithm.
	> - **False**

14. **(T/F)** The Edmonds-Karp 2 algorithm is a polynomial time algorithm.
	> - **False**

15. **(T/F)** If all capacities in a flow network are integers, then every maximum flow in the network is such that the flow value on each edge is an integer.
	> - **False**

16. **(T/F)** If we add the same positive number to the capacity of every directed edge, then the minimum cut (but not its value) remains unchanged.
	> - **False**

17. **(T/F)** Given a max-flow value you can find a min-cut in $O(E)$.
	> - **False**

18. **(T/F)** Given a min-cut value you can find a max-flow value in $O(E)$.
	> - **False**

19. **(T/F)** Every flow is a circulation.
	> - **False**

20. **(T/F)** There is a feasible circulation with demands $\{d_v\}$ if $\sum_{v}d_v$ = 0.
	> - **False**


### Exercise Q&A
1. Given a flow network $N = (G = (V, E), s, t, c)$, where E might contain edges $(u, v)$ and $(v, u)$ in both directions for some pair of vertices $u$, $v$, we would like to use the Ford–Fulkerson algorithm to solve the flow problem on $G$, but $G$ is not a flow network. Reduce this problem to the network flow problem.
	> - **Solution**

2. Suppose we have a directed weighted graph $G = (V, E)$ with multiple sources $s_1, s_2, …, s_n$ and multiple sinks $t_1, t_2, …, t_m$. Reduce this problem to the network flow problem.
	> - **Solution**

3. Given a flow network $N = (G = (V, E), s, t, c)$, find the maximum number of edge disjoint paths from $s$ to $t$. A set of paths is edge disjoint if no two paths share an edge.
	> - **Solution**

4. Given a flow network $N = (G = (V, E), s, t, c)$, find the maximum number of vertex ndisjoint paths from $s$ to $t$. A set of paths is vertex disjoint if no two paths share na vertex.
	> - **Solution**

5. Given a flow network $N = (G = (V, E), s, t, c)$, in which, in addition to having a capacity c$(u, v)$ for every edge, we also have a capacity $c(v)$ for every vertex. The flow coming to a vertex $v$ cannot exceed the vertex capacity $c(v)$. Reduce this problem to the network flow problem.
	> - **Solution**

6. You have successfully computed a maximum $s-t$ flow for a network $G = (V, E)$ with positive integer edge capacities. Your manager now gives you another network $G’$ that is identical to $G$ except that the capacity of exactly one edge is decreased by one. You are also explicitly given the edge whose capacity was changed. Describe how you can compute a maximum flow for $G’$ in linear time.
	> - **Solution**

7. The vertex cover of an undirected graph $G = (V, E)$ is a subset of the vertices that touches every edge; that is, a subset $S \in V$ such that for each edge $(u, v) \in E$, one or both of $u, v$ are in $S$. Show that the problem of finding the minimum vertex cover in a bipartite graph reduces to the maximum flow problem.
	> - **Solution**
	
8. A subset of edges is a matching if no two edges have a common vertex. A maximum matching is a matching with the largest possible number of edges. Our goal is to find the maximum matching in a bipartite graph. Show that the problem of finding the maximum matching in a bipartite graph reduces to the maximum flow problem.
	> - **Solution**
	
9. There are $n$ students in a class. We want to choose a subset of $k$ students to join a committee. There has to be $m_1$ number of freshmen, $m_2$ number of sophomores, $m_3$ number of juniors, and $m_4$ number of seniors on the committee. Each student is from one of $k$ departments, where $k = m_1 + m_2 + m_3 + m_4$. Exactly one student from each department has to be chosen for the committee. We are given a list of students, their home departments, and their class (freshman, sophomore, junior, or senior). Describe an efficient algorithm based on network flow techniques to select who should be on the committee such that these constraints are all satisfied.
	> - **Solution**

10. Consider a set of mobile computing clients in a certain town who each need to be connected to one of several possible base stations. We’ll suppose there are $n$ clients, with the position of each client specified by its $(x, y)$ coordinates in the plane. There are also k base stations; the position of each of these is specified by $(x, y)$ coordinates as well. For each client, we wish to connect it to exactly one of the base stations. Our choice of connections is constrained in the following ways. There is a range parameter $R$, which means that a client can only be connected to a base station that is within distance R. There is also a load parameter L, which means that no more than L clients can be connected to any single base station. Given the positions of a set of clients and a set of base stations, as well as the range and load parameters, decide whether every client can be connected simultaneously to a base station.
	> - **Solution**
	
11. The computer science department course structure is represented as a directed acyclic graph $G = (V, E)$ where the vertices correspond to courses and a directed edge $(u, v)$ exists if and only if course $u$ is a prerequisite for course $v$. By taking a course $w \in V$, you gain a benefit of $p_w$ which could be a positive or negative number. Note, to take a course, you have to take all of its prerequisites. Design an efficient algorithm that picks a subset $S \in V$ of courses such that the total benefit is maximized.
	> - **Solution**
	
12. The edge connectivity of an undirected graph $G = (V, E)$ is the minimum number of edges that must be removed to disconnect the graph. For example, the edge connectivity of a tree is $1$. Show how the edge connectivity of an undirected graph can be determined by running a maximum-flow algorithm.
	> - **Solution**

13. There is a precious diamond that is on display in a museum at $m$ disjoint time intervals. There are $n$ security guards who can be deployed to protect the precious diamond. Each guard has a list of intervals for which he or she is available to be deployed. Each guard can be deployed to at most $M$ time slots and has to be deployed to at least $L$ time slots. Design an algorithm that decides if there is a deployment of guards to intervals such that each interval has either one or two guards deployed.
	> - **Solution**
	
14. Your local police department has asked you to help set up the work shift schedule for the next month. There are $n$ policemen on the staff and $m$ days in the month. Each policeman gives a list of the days of the month that he or she is available to work. Let $d_i$ denote the number of days that each policeman $i$ is available to work. Then he or she should be scheduled to work at least $d_i / 2$ of these days. Each day there must be exactly 2 policemen on duty. Design an algorithm that decides whether there exists a schedule that satisfies all of these requirements.
	> - **Solution**
	