# Introduction to Combinatorics 

# Lecture 1

## Products and Sums

The ways of choosing an element from set A **and** from set B is the **cartesian product** of the two sets. 
- the number of ways of choosing a pair from A and B is $|A \times B| = |A| \cdot |B|$

The number of ways of choosing an element from set A **or** and element from B is the union of the two sets
- the number of ways of choosing an element from either set is equal to the size of the union 
- $|A \cup B| = |A| + |B|$ if the sets are **disjoint**

Subsets example:            
Given an n-element set S, how many subsets does S have?             
To specify a subset X of S, we make a choice for each $u \in S$ : IN if $u \in X$ or OUT if $u \nin X$
    - so we choose an element from {IN, OUT} n times
    - we want an element is either (in or out) **and** the next element is in or out and so on... 
    - |{IN, OUT}| * |{IN, OUT}| * ... * |{IN, OUT}| = $2^{|S|}$

How many ways are there to put the elements of an n-elemented set S in order? 
    - |S|! (if |S|=n then ways=n(n-1)(n-2)...1)

0! = 1 by convention

**Partial lists:**
- A length-k partial list of a set S is a k-tuple of distinct elements of S
- if |S|=n we have n(n-1)...(n-k+1) ways to create length-k partial lists of S
    - $\frac{n!}{(n-k)!}$


