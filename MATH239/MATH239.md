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

# Lecture 2
## Counting Subsets 
Let ${n \choose k} = \frac{n!}{k! \cdot (n-k)!}$ denote the number of k-element subsets of an n-element set S. "n choose k".
- ${n \choose 0} = 0$

Theorem 1.5: ${n \choose k} = \frac{n!}{k! \cdot (n-k)!}$ for all $0 \leq k \leq n$

**Example 1.6:** ${n \choose 1} + {n \choose 2} + \cdots + {n \choose n} = 2^n$
- proof: the RHS is the number of subsets of an n-element set S, the LHS sign should be shown to also have the same meaning
    - this proof idea is a combinatorial proof instead of an algebraic one and describes the meaning behind the formula a lot better than an algebraic proof

**Definition 1.10:** Let A, B be sets. A bijection from A to B is a function $f : A \rightarrow B$ so that 
- for all $a, a' \in A$ if $f(a) = f(a')$ then $a = a'$
- for all $b \in B$ there exists $a \in A$ such that $f(a) = b$

**Proposition 1.11:** A function $f : A \rightarrow B$ is a bijection if and only if $f$ has an inverse: a function $g : B \rightarrow A$ such that 
- $g(f(a)) = a$ for all $a \in A$ 
- $f(g(b)) = b$ for all $b \in B$

The reason we care about a bijection from A to B is because if a bijection exists between two finite sets then the bijection uniquely maps elements from one set to the other and so it follows they have the same size. 
- in this course we use the notation $A \rightleftharpoons B$ to indicate that to sets are in bijection 

**Example 1.6/7:** If $k,n \geq 1$, then ${n \choose k} = {n-1 \choose k} + {n-1 \choose k-1}$
- proof: create a bijection between the two sets, let S = {1,...,n} and S'={1,...,n-1} 
    - let A = k element subsets of S 
    - let B = (k-1)-element or k-element subsets of S'
    - let f(x) = x if n not in x and x\{n\} if n in x
    - let g(y) = y if |y| = k and $y \cup \{n\}$ if |y| = k-1
    - f and g are inverses and so the sets are in bijection and have the same size

This formula is Pascal's triangle. 

# Lecture 3
## Multiset
An **n-element multiset with t types** is a **t**-tuple $(n_1, n_2, \cdots, n_t)$ of nonnegative integers with $n_1 + n_2 + \cdots  + n_t = n$

**Theorem 1.9:** The number of **n-element** multisets with **t** types is ${n + t - 1 \choose t - 1}$

Are these proofs rigorous/mathematical? 
- yes! 

How do I come up with proofs like this?
- practice / creativity

**Example:** Prove that $\sum_{m=k}^{n-1} {m \choost k} = {n \choose k+1}$ for all $0 \leq k < n$
