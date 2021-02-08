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

# Week 2 

## Module 1 - MCT 
Definition: (a series is)
1. increasing 
    - if $a_n \geq a_{n+1}$ for all $n \in \mathbb{N}$
2. decreasing
    - if $a_n \leq a_{n+1}$ for all $n \in \mathbb{N}$
3. monotone
    - if it is increasing or decreasing 

Note: We allow a constant sequence to be increasing & decreasing 

**Theorem - Monotone Convergence Theorem:** 
If $(a_n) \subseteq \mathbb{R}$ is increasing and $\{ a_{ni} \n \in \mathbb{N}\}$ is bounded above then 
$$a_n \rightarrow sup\{a_n : n \in \mathbb{n}\}$$

**Corollary**           
If $(a_n) \in \mathbb{R}$ is decreasing and is bounded then 
$$a_n \rightarrow inf\{a_n : n \in \mathbb{N}\}$$

Monotone (either increasing or decreasing). 

## Module 2 Nested Interval Lemma

**Theorem - Nested Intervals Theorem:**
Let $I_1 \supseteq I_2 \supseteq I_3 \supseteq \cdots$ where each $I_i = [ a_i, b_j]$ (each is bounded), $a_i \leq b_i$. Then 
$$\bigcap^\infty_{n=1} I_n \neq \emptyset$$
- their intersection is not empty


## Module 3 - Bolzana Weierstrass Theorem

**Definition:** $(a_n) \subseteq \mathbb{R}$ a subsequence of $(a_n)$ is a sequence 
$$(a_nk)^{\infty}_{k=1}$$
where $n_1 < n_2 < n_3 < \cdots$

**Theorem:** [ Bolzano-Weierstrass Theorem ]
- Every bounded sequence of real numbers has a convergent subsequence. 

## Module 4 - Completeness of $\mathbb{R}$

**Definition:** Cauchy Sequence         
- We say $(a_n)$ is cauchy if $\forall \epsilon > 0, \exists N \in \mathbb{N}$ such that $|a_n - a_m| < \epsilon$ for all $n,m \geq N$

**Proposition:** $(a_n) \subseteq \mathbb{R}$
- if $(a_n)$ is convergent then the sequence is cauchy 

**Proposition:** $(a_n) \subseteq \mathbb{R}$
- if $(a_n)$ is cauchy then the sequence is bounded 

**Theorem - Completeness in $\mathbb{R}$:** 
- A sequence $(a_n) \subseteq \mathbb{R}$ is convergent **iff** it is cauchy 

Remark: Recap of the week 
- LUB 
- $\Rightarrow$ MCT 
- $\Rightarrow$ NIL
- $\Rightarrow$ BW Theorem
- $\Rightarrow$ Cauch $\iff$ Convergent
- $\Rightarrow$ LUB
    - this one is an axiom in this course
    
# Week 3
## Module 1 - Normed Vector Spaces

Main math object we work with. 

Idea [ Normed Vector Space ]
- a vector space where we can measure distance between vectors


**Definition - Norm:**
- let V be a real vector space over $\mathbb{R}$

A **norm** on V is a function $||\cdot ||: V \rightarrow \mathbb{R}$ such that 
1. $||v|| \geq 0$ for all v
2. $||v|| = 0$ iff $v=0$
3. For all $\alpha \in \mathbb{R}, v \in V$
    - $||\alpha v|| = |\alpha | \cdot ||v|||$
4. Triangle inequality 
    - $|| u + v || \leq ||u|| + ||v||$

## Module 2
A NVS is a vector space equipped with a norm 

Example: reals with absolute value 

Example: $\mathbb{R}^n, ||\cdot||_2$ 
- $||(x_1, \cdots, x_n)||_2 = \sqrt{x_1^2 + \cdots + x_n^2}$

Example: $\mathbb{R}^n, ||\cdot||_p$ 
- $||(x_1, \cdots, x_n)||_p = (x_1^p + \cdots + x_n^p)^\frac{1}{p}$

Example: Rn equipped with $||\cdot||_\infty$ 
- we choose the maximum of the elements 
- sup or infinity norm 

$l^p$ is a subset of $\mathbb{R}^{N}$ where its elements have finite p-norm 

## Module 3 - Convergence 

Definition: sequence in NVS

Definition: convergence in NVS

Definition: sequence in NVS

Proposition: if V is NVS
- an->v bn->w sequences in V
1. an + bn -> v + w
2. a \* an -> a \* v

## Module 4 - More convergence examples 

## Module 5 - Cauchy Sequences 

Definition: Cauchy in NVS

## Module 6

Definition: bounded in NVS

Proposition: If in an in NVS, an is couchy then an is bounded

**Definition - complete:** A **subset** of vector space is **complete** if every cauchy sequence in it converges in it. 
- If the whole vector space is complete then it said to be a **Banach space**

# Week 4 

## Module 1 - Topology 1

Topology is the study of subsets of a set X which afford X meaningful analytic / geometric properties

Definition: Let V be NVS. We say $C \subseteq V$ is closed if whenever $(x_n)\subseteq C$ such that $x_n \rightarrow x \in V$ then $x \in C$
- Idea: C is closed iff C is "closed" under taking limits 
