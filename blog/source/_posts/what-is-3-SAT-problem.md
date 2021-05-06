---
title: what is 3-SAT problem
catalog: true
mathjax: false
date: 2021-04-08 18:58:25
subtitle:
header-img:
tags:
categories:
---

would start from the question, what's SAT in general. SAT is satisfiability problem - say you have Boolean expression written using only AND, OR, NOT, variables, and parentheses. The SAT problem is: given the expression, is there some assignment of TRUE and FALSE values to the variables that will make the entire expression true?

For example,

x1∧x2∨x3

SAT problem for this Boolean expression: is there such values of x1,x2,x3, that given Boolean expression is TRUE. The answer to SAT problem is only YES or NO. We don't care what's the values of x1,x2,x3, just existence of such values.

If this is OK, let's go further.

3SAT problem is a special case of SAT problem, where Boolean expression should have very strict form. It should be divided to clauses,such that every clause contains of three literals.

For example,

(x1∨x2∨x3)∧(x4∨x5∨x6)
This Boolean expression in 3SAT form, 2 clauses, each clause contains of 3 literals. The question is the same, is there such values of x1...x6, that given Boolean expression is TRUE.