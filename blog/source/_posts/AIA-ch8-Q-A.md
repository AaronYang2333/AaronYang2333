---
title: $$[Algorithms \, In \, Action]-CH7\, Linear  \,\, Programming $$
catalog: true
mathjax: true
date: 2021-04-20 05:47:22
subtitle:
header-img:
tags:
- Review
- Linear Programming
- Q&A
categories:
- CSCI 570
---

### Review Q&A
1. What is linear programming?
	> - **Solution**

2. What is an objective function?
	> - **Solution**

3. What are the nonnegativity constraints?
	> - **Solution**

4. What is an optimal solution?
	> - **Solution**

5. What is a feasible solution?
	> - **Solution**

6. (T/F) Every LP has an optimal solution.
	> - **False**
	
7. (T/F) If an LP has an optimal solution it occurs at an extreme point.
	> - **False**
	
8. (T/F) If an LP is feasible and bounded, then it must have an optimal solution.
	> - **False**
	
9. (T/F) An LP allows strict inequalities in the constraints.
	> - **False**
	
10. (T/F) An LP for which the feasible region is unbounded has the finite optimal solution.
	> - **False**
	
11. (T/F) The weak duality theorem does not always hold for an integer linear program.
	> - **False**
	
12. (T/F) An LP must be infeasible if its dual problem is unbounded.
	> - **False**
	
13. (T/F) Both the primal and the dual can be infeasible.
	> - **False**
	
14. (T/F) There is no duality gap in linear programming.
	> - **False**
	

### Exercise Q&A
1. A furniture company produces two types of chairs. The first type takes 10 hours to make and uses 2 square yards of fabric and 20 pounds of padding. The second type takes 70 hours to make and uses 3 square yards of fabric and 10 pounds of padding. The profit of the first type is $2 per chair, and the profit of the second type is $5 per chair. The resources available for production for both chairs are 490 hours of labor, 32 yards of fabric, and 240 pounds of padding. How many chairs of each type should the company make in order to maximize its profit?
	> - **Solution**

2. A cargo plane can carry a maximum weight of 100 tons and a maximum volume of 60 cubic meters. There are three materials to be transported, and the cargo company may choose to carry any amount of each, up to the maximum available limits provided in the table below Density Volume Price Material 1 2 tons/m3 40 m3 $1,000 per m3 Material 2 1 tons/m3 30 m3 $2,000 per m3 Material 3 3 tons/m3 20 m3 $12,000 per m3 Write a linear program that optimizes revenue given the constraints.
	> - **Solution**

3. A furniture company produces three types of couches. The first type uses 1 foot of framing wood and 3 feet of cabinet wood. The second type uses 2 feet of framing wood and 2 feet of cabinet wood. The third type uses 2 feet of framing wood and 1 foot of cabinet wood. The profit of the three types of couches is $10, $8, and $5, respectively. The factory produces 500 couches each month of the first type, 300 of the second type, and 200 of the third type. However, this month there is a shortage of cabinet wood to only 600 feet, but the supply of framing wood is increased by 100 feet. How should the production of the three types of couches
be adjusted to minimize the decrease in profit?
	> - **Solution**

4. You have $1,000 to invest. There are three types of investments. The first type is every dollar invested yields $0.10 a year from now and $1.30 three years from now. The second type is every dollar invested yields $0.20 a year from now and $1.10 two years from now. The third type is every dollar invested a year from now yields $1.50 three years from now. The most that can be invested into a single investment is $500. During each year all leftover cash is placed into money markets that yield 6% per year. Write a linear program to maximize your investment in three years from now.
	> - **Solution**

5. The Canine Products company has two dogfood products, Frisky Pup and Husky Hounds, that are made from a blend of two raw materials, cereal and meat. One pound of cereal and 1.5 pounds of meat are needed to make a package of Frisky Pup, and it sells for $7 a package. Two pounds of cereal and 1 pound of meat are needed to make a package of Husky Hound, and it sells for $6 a package. Raw cereal costs $1 per pound and raw meat costs $2 per pound. It also costs $1.40 to package the Frisky Pup and $.60 to package the Husky Hound. A total of 240,000 pounds of cereal and 180,000 pounds of meat are available per month. The production bottleneck is that the factory can only package 110,000 bags of Frisky Pup per month. Write a linear program to maximize profit.
	> - **Solution**

6. Rewrite the following linear programs in the standard maximum form: a. Maximize 2 x + 3 y subject to 5 x – 6 y ³ 7 7 x + 8 y £ 9 x ³ 0, y ³ 2 b. Maximize 2 x + 3 y subject to 5 x – 6 y ³ 7 7 x + 8 y = 9 x ³ 0 c. Minimize 5 x – 2 y + 9 z subject to 3 x + y + 4 z = 8 2 x + 7 y – 6 z £ 4 x £ 0, z ³ 1
	> - **Solution**

7. Modify the linear program in section 8.3.1 to find the shortest distance from the source s to all other vertices.
	> - **Solution**

8. What happens to the LP in section 8.3.1 if a given graph has negative weight cycles?
	> - **Solution**

9. The all-pairs shortest-paths problem is to find a shortest path between any pair of vertices, u to v. Formulate the all-pairs shortest-paths problem as a linear program.
	> - **Solution**

10. Given a bipartite graph, G = (V, E), a subset of edges is a matching if no two edges have a common vertex. A maximum matching is a matching with the largest possible number of edges. Our goal is to find the maximum matching in a bipartite graph G. Write a linear program that solves the maximum-matching problem.
	> - **Solution**
	
11. There are n people and n jobs. You are given a cost matrix, where each element C(i, j) represents the cost of assigning person i to do job j. You need to assign all the jobs in such a way that each person performs only one job and each job is assigned to only one person. Write a linear program that minimizes the total cost of the assignment.
	> - **Solution**

12. Given an infinite supply of bins, each of which can hold the maximum weight of 1, and there are also n objects, each of which has a weight wi £ 1, your goal is to place all the objects into bins in such a way that the total number of used bins is minimized. Formulate the problem as an integer linear programming problem.
	> - **Solution**

13. Write the duals to the following linear programs: a. Maximize x 1 + x2 + 2 x3 subject to x1 + 2 x3 £ 3 –x 1 + 3 x3 £ 2 2 x 1 + x2 + x3 £ 1 x 1, x2, x3 ³ 0 b. Maximize 3 x 1 – 2 x2 + x3 subject to x1 – x2 + x3 £ 4 3 x 1 + x2 + 2 x3 £ 6 –x 1 + 2 x3 = 3 x 1 + x2 + x3 £ 8 x 1, x2, x3 ³ 0 c. Minimize 3 y1 – 2 y2 + 5 y3 subject to – y2 + 2 y3 ³ 1 y1 + y3 ³ 1 2 y1– 3 y2 + 7 x3 ³ 5 y1, y2, y3 ³ 0
	> - **Solution**

14. Create an example of a linear program showing that the strong duality theorem does not always hold for an integer linear program.
	> - **Solution**

15. Create an example of a linear program showing that the primal and the dual can be both infeasible.
	> - **Solution**
	