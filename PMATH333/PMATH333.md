# Introduction to Real Analysis

# Week 1 
## Module 1 - Infimum and Supremum
For the following let $A \subseteq \mathbb{R}$:          
**Definition - bounded above:** $A$ is bounded above if $\exists M \in \mathbb{R}, a \leq M$ for all $a \in A$        
**Definition - bounded below:** $A$ is bounded below if $\exists M \in \mathbb{R}, a \geq M$ for all $a \in A$        
**Definition - bounded:** $A$ is **bounded** if it is bounded above and below 

**Definition - supremum:** given $M \in \mathbb{R}$, $M$ is a supremum if 
1. M is an upper bound for $A$
2. if $N$ is an upper bound for $A$ then $M \leq N$

**Remark:**
1. $\emptyset \neq A \subseteq \mathbb{R}$ and $M,N$ are supremum of A then $M = N$
    - we write $M = sup A$
2. If $A$ is not bounded above we write $supA = \infty$

**Definition - infimum:** given $M \in \mathbb{R}$, $M$ is an infimum if 
1. M is a lower bound for $A$
2. if $N$ is a lower bound for $A$ then $N \leq M$
    - if $A$ is not bounded below we write $infA = \infty$


The big picture is
- supremum = least upper bound
- infimum = greatest upper bound

**Axiom - Least Upper Bound Property (LUB):** If $\emptyset \neq A \subseteq \mathbb{R}$ is bounded above then $supA$ exists. 

## Module 2 - Density of The Reals

**The Archimedian Principle:** Let $a,b \in \mathbb{R}$ be positive. Then there exists some some $n \in \mathbb{N}$ such that $b < n \cdot a$

**Theorem - Density of the rationals:** Let $a < b$ be real numbers. There exists $q \in \mathbb{Q}$ such that $a < q < b$
- simply: there is a rational between any two reals

**Corollary:** Let $a \in \mathbb{R}$ for every $\epsilon > 0, \exists q \in \mathbb{Q}$ such that $|a-q| < \epsilon$

## Module 3 - Sequences

**Definition - sequence of real numbers:** A sequence of numbers is an infite list of real numbers $(a_1, a_2, a_3, \cdots )$ where $a_i \in \mathbb{R}$

**Definition - converges:** $(a_n) \subseteq \mathbb{R}$ **converges** to $a$,$a_n \rightarrow a$, if for all $\epsilon > 0$ there exists $N \in \mathbb{N}$ such that for all $n \geq N$ we have $|a_n - a| \leq \epsilon$
- we call $a$ the limit of $(a_n)$

**Remark:** our definition of convergence requires a natural number but finding a real number is sufficient as we can take the ceiling of it. 

**Remark:** By archimedian principle (AP) we have there exists $N \in \mathbb{N}$ such that $N \cdot \epsilon > 1 \Rightarrow \frac{1}{N}$ and so for $n \geq N$ we have $\frac{1}{n} \leq \frac{1}{N} < \epsilon$
- so $\frac{1}{n}$ converges to 0

**Definition - bounded:** We say $(a_n) \subseteq \mathbb{R}$ is bounded if $\exists M \in \mathbb{r}$ such that $|a_n| \leq M$ for all $n \in \mathbb{N}$

**Proposition:** if $(a_n)$ is convergent then it is bounded
- because sequences are right infinite and so if the right side converges then it must be bounded

**Proposition - convergence rules:** let $(a_n), (b_n) \subseteq \mathbb{r}$, $(a_n) \rightarrow a, (b_n) \rightarrow b$
1. $a_n + b_n \rightarrow a + b$
2. if $\alpha \in \mathbb{r}$ then $\alpha a_n \rightarrow \alpha a$
3. $a_n \cdot b_n \rightarrow ab$
4. if $b_n \neq 0$ for all $n \in \mathbb{N}$ and $b \neq 0$ then $\frac{a_n}{b_n} \rightarrow \frac{a}{b}$

## Module 4 - Practice (contains useful results)

**Limits prserve order:** if $a_n, b_n$ are real and converge to $a$ and $b$ and $\exists M \in \mathbb{N}$ such that $a_n \leq b_n, \forall n \geq M$ then $a \leq b$

