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

**Example:** Prove that $\sum_{m=k}^{n-1} {m \choose k} = {n \choose k+1}$ for all $0 \leq k < n$

# Lecture 4 
## Power Series 
- $P(x) = 1 - 2x + 3x^2 - 4x^3 + \cdots = \sum_{n \geq 0} (-1)^n \cdot (n+1) \cdot x^n$

**Example 2.1:** let $P(x) = 1 + x + x^2 + \cdots$
- consider $(1-x) \cdot P(x) = 1$
- we write $P(x) = \frac{1}{1-x} = (1-x)^{-1}$ **(geometric series)**

**Theorem 2.2 (binomial theorem):** For $n \geq 0$
 $$(1+x)^n = \sum_{k=0}^n {n \choose k} x^k$$

 How can we handle these infinite sums without worrying about convergence 
 - these objects are not functions in x; they are **generating series**
$$F(x) = f_0 + f_1 x + f_2 x^2 + \cdots = \sum_{n \geq 0} f_n x^n$$
- also called generating functions 
- formal power series 

"A generating function is a clothesline on which we hang up a sequence of numbers for display" - H. Wilf
- the coeffients are what matter 

$$(F \cdot G) (x) = \sum_{n \geq 0} (\sum_{k=0}^n f_k g_{n-k})x^n$$

# Lecture 5 

**Negative Binomial Thoerem (2.4):** If $t \geq 1$ then, 
$$(1-x)^{-t} = \sum_{n\geq 0} {n + t - 1 \choose t - 1} x^n$$

Combinatorial proof: 
- the combinations is the number of n-multisets with t types
- some manipulation results in 

Notation: 
- for a generating series we write $[x^k]F(x) = c$ to indicate the coefficient is c for the $x^k$ term

So 
- we can extract sum of []
- we can find $[x^k](x^l F(x) = [x^{k-l}]F(x)$
    - since multiplying by $x^l$ shifts exponents l to the right
- we can find the product

# Lecture 6 
Generating series for sets 

Let $S$ be a st, and $w : S \rightarrow \mathbb{Z}_{\geq 0}$ be a weight function. 
- The generating series for $S$ with respect to $w$ is 
$$\Phi_S (x)  = \sum_{\sigma \in S} x^{\sigma}$$
- we require the number of welements with weight $n \in \mathbb{Z}_{\geq  0}$ to be finite

**Proposition 2.7:** If w is a weight function on a set S, then 
$$ \Phi (x)_S = \sum_{n \geq 0} | \{\sigma \in S : w(\sigma) = n \} | x^n$$
- in other words the coefficients count the number of weight n in S

# Lecture 7 - The sum and product lemma 

The sum of two generating series is the union of two generating series 
- say one counts main dishes of certain price and the other is side dishes of some price
- then the sum counts either type of dish for some price

The product of two generating series gives elements which correspond to cartesian product (the new weighting function is the sum) 
- so one counts main dishes of certain price and other is side dishes 
- the product counts how many ways to choose main dish and side dish to get a certain product 

**Sum Lemma**: 
$$\Phi_{s_1}(x) + \Phi_{s_2}(x) = \Phi_{s_1 \cup s_2}(x)$$
- generating series for disjoint unions 
- where the weight of $s_1 + s_2$ is $w(\sigma_1, \sigma_2) = w_1(\sigma_1) + w_2(\sigma_2)$

**Infinite Sum Lemma**: 
$$\Phi_s (x) = \sum_{n \geq 0} \Phi_{s_n}(x)$$

**Product Lemma**: 
$$\Phi_{s_1} (x)  \Phi_{s_2} (x) = \Phi_{s_1 \times s_2}(x)$$
- where the weight of $s_1 \times s_2$ is $w(\sigma_1, \sigma_2) = w_1(\sigma_1) + w_2(\sigma_2)$


# Lecture 8 - The string lemma and compositions 

**Stars:** Let S be a set. $S^2 = S \times S, S^3 = S \times S \times S$, etc.
and 
$$S^\ast = \underset{t \geq 0}{\cup s^t} = \text{all tuples of elements of S}$$  

Definition: (if **no** elements have weight zero): $w^\ast : S^\ast \rightarrow \mathbb{Z}_{\geq 0}$
$$w^\ast ((\sigma_1, \cdots, \sigma_t)) = \sum_{i = 1}^t w(\sigma_i)$$

**String Lemma:** If $w$ is a weight function on $S$ and no elements have weight-zero 
$$\Phi_{S^\ast}(x) \ \frac{1}{1 - \Phi_S(x}$$

**Definition - Composition:** A tuple of positive integers. The terms in the tuple are called parts. The weight of a composition is the sum of its parts. 
- the composition of n means the composition of weight 10 (tuples that add to 10) 
- we could define the composition as an element of the star of positive integers 


$$\Phi_{compositions}(x) = \frac{1-x}{1-2x}$$

# Lecture 9 - Compositions and coefficients 

Recursive method for finding coefficients in generating series 













