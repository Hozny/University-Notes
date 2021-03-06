# STAT 230 - Introduction to probability | Fall 2020

# Week 1

## Definitions of probability 
**Definition - Classical probability:**
- (number of ways that an even can occur) / (total number of outcomes in S)

**Definition - Relative frequency definition:**
- the probability an even in an experiment or the fraction of times that the event occurs in a very long            
(theoretically infinite) series

**Definition - Subjective probability:**
- 'best guess' by person making a statement of the chances

**Probability model**
1. a sample space of all possible outcomes is defined
2. a set of events is defined. An even is a subset of the sample space
3. a way of assigning probabilites, which are numbers between 0 and 1, to events specified


**Definition - Random experiment:**
- repetitions of a random experiment are called **trials**
- experiment must be repeatable
- may obtain different outcomes under controlled conditions
    - there are probabilities associated with each outcome

**Definition - Discrete sample spaces:** A sample space with a *finite* number of sample points, or **countable many** many sample points           

**Definition - countable:** A set S is countable if the lements can be put in a 1-1 correspondence with the positive integers           
- the set of all integers is a countable set

**Definition - Event:** an even $A$, defined on a discrete sample space S, is a subset of S

**Definition - Simple event:** An event consisting of only one sample point

**Definition - Compount event:** if an event consists of two or more sample points. A is said to **occur** on a trial of the experiment if one of the simple events in A occurs.        

**Definition - Probability Distribution on S):** Let S be a discrete sample space. 
Let $P(a_1), P(a_2), \cdots$ be a set of numbers associated with sample points such that
1. $0 \leq P(a_i) \leq 1$
2. $\Sigma_{i=1} P(a_i) = 1$

**Definition - Probability of an event:** Let S be a discrete sample space. Let A be an event defined on S. 
- Then $P(A)$ is the sum of the probabilities of all simple events that are in A

**Definition (addition rule):** if we can do job1 p ways, or job2 q ways but not both then we can do p+q ways 

**Definition (multiplication rule:** if we can do p ways job1 and q ways job2 then p\*q ways total

**Definition - n choose k:** $\binom{n}{k} = \frac{n!}{(n-k)! \cdot k!}$         

# Week 2

## Sets and probability 1
**Definition - Union:** $(A \cup B)$ is the set of all points in either A or B

**Definition - Intersection:** $(A \cap B)$ is the set of all points which are in both A and B

**Definition - Complement:** The complement of $A$ written as $\bar{A}$ is the set of all points in $S$ which are not in $A$

De Morgan's Laws: 
- $\bar{A \cup B} = \bar{A} \cap \bar{V}$
- $\bar{A \cap B} = \bar{A} \cup \bar{B}$

**Definition - Mutually Exclusive:** Two events are mutually exclusive if $A \cup B = \emptyset$

**Definition - Probability Set Function:** $P$ associates a real value $P(A)$ with each even A defined on sample space S
1. $0 \leq P(A)$ for every $A$
2. $P(S) = 1$
3. If $A_1, \cdots, A_n$ are mutually exclusive then probability of all of them is equal to sum of individual probabilities
- these three properties are called the **Axioms of probability**

## Sets and probability 2
**Theorem:**
- Probability of event A is between 0 and 1 (inclusive)
- Probability of complement of A is $1 - P(A)$
- If A is a subset of B then $P(A) \leq P(B)$
- If A and B are mutually exclusive then $P(A \cup B) = P(A) + P(B)$
- $P(A \cup B) = P(A) + P(B) - P(A \cap B)$
- $P(A \cup B \cup C) = P(A) + P(B) + P(C) - P(A \cap B) - P(A \cap C) - P(B \cap C) + P(A \cap B \cap C)$

## Independent events
**Definition - n independent events):** $A_1,\cdots, A_n$ are independent if and only if
$P(A_{i_1} \cap A_{i_2} \cap \cdots \cap A_{i_k}) = P(A_{i_1})\cdots P(A_{i_k)$ for all sets $(i_1, \cdots, i_k)$ of distinc subscripts chosen from $(1, \cdots, n)$
- it is not sufficient to only have pairwise independence  

# Week 3

## Independent Events: examples

Example: Out of 10 keys, 2 keys open a door. 2 Keys are drawn at random. 
- probability of first key opens the door a = 2/10
- probability of second key opens the door b = 2/10
- probability of P(A) and P(B) = (2 * 1) / (10 * 9)
    - this is not equal to 2/10 * 2/10 so they are independent

Problem: If A and B are positive probability events and are independent is it posible they are mutually exclusive? 
- $P(A \cap B) = P(A)P(B) > 0$ (since they are independent)
- if they were mutually exclusive then $P(A \cap B) = 0$ but from above we know that is not true, so they cannot be mutually exclusive

## Conditional Probability

**definition - Conditional Probability:** The conditional probability of A occuring giving B occurs is defined by $P(A|B) = \frac{P(A \cap B)}{P(B)}$ provided $P(B) \neq 0$

**Theorem:** A and B are independent if and only if $P(A|B) = P(A)$ and $P(B|A) = P(B)$
- just multiply out denominator of the definition of conditional probability to get definition of independence 

**Theorem: (Multiplication rule):** For any two events A and B, 
1. $P(A \cap B) = P(A|B)P(B)$ and 
2. $P(A \cap B) = P(B|A)P(A)$

**Theorem: (Law of Total Probability):** Let the sample space $S$, be partitioned into $k$ mutually exclusive sets $B_1, \cdots, B_k$ such that $P(B_i) > 0$ for $i = 1, \cdots, k$ and $S = B_1 \cup B_2 \cup \cdots \cup B_k$
- then for any even $A$, $P(A) = \Sigma_{i=1}^kP(A \cap B_i)$.

# Week 4
## Random vairables and distributions 2
**Definition (c.d.f):$$ A cummulative distribution function (c.d.f.) is defined as the funciton $F(x) = P(X \leq x)$, for all real $x$
1. $F(x) is non decreasing
2. $0 \leq F(x) \leq 1$ for all $x$
3. $lim_{x \rightarrow - \infty} F(x) = 0$ and $lim_{x \rightarrow \infty} F(x) = 1$

$f(x) = F(x) - F(x-1)$

## Discrete uniform and hypergeometric distributions

**Theorem:** Suppose $X$ takes values $a, a+1, a+2, \cdots, b$ with all values being equally likely. Then $X$ has a discrete uniform distribution on its domain. The probability function of the discrete uniform is 
$$ f(x) = \frac{1}{b-a+1} $$
- for $x = a, a+1, a+2, \cdots, b$, and $0$ otherwise

**Theorem:** We have a collection of $N$ obejects which can be classified into two distinct types, $r$ of type 1, and $N-r$ of type 2.          
Pick a sample of $n < N$ at random **without replacement**          
Let $X$ be the number of type 1 in the sample.          
Then $X$ has a hypergeometric distributionm with probability function
$$ f(x) = \frac{ways-to-choose-x-type-1) \cdot (ways-to-choose-n-x-type-2)}{(ways-to-choose-sample-of-n)}$$
$$ = \frac{ {r \choose x} l{N-r \choose n-x} }{ {N \choose n} }$$
- the range for $X$ is $max(0, n-N+r) \leq x \leq min(r, n)$

**Theorem:**
$$\Sigma_{all-x} {a \choose x} {b \choose n-x} = {a+b \choose n} $$

**Definition - acceptance sampling** is a statistical method which is used for deciding whether a batch of items produced by a company is acceptable or not for distribution (sale) 

## Binomial distribution

**Definition** Suppose we have an experiment with 2 possible outcomes which, for convenience, we call Success ($S$) and Failure ($F$). Suppose that $P(S) = p$. Repeat the experiment (called a **trial**). Such a sequence of independent trials are called **Bernoulli trials**.          
Key assumptions: 
1. the probability of success, $p$, must be **constant** over $n$ trials
2. the $n$ trials must be **independent**

**Theorem:** the probability function of x for binomial distribution is 
$$ f(x) = {n \choose x} p^x(1 - p)^{n-x}$$
- for $x = 0, 1, 2, \cdots , n$

**Theorem - (binomial theorem):** 
$$ \Sigma_{x = 0}^n {n \choose x} a^xb^{n-x} = (a + b)^n $$

The main difference between Binomial distribution and Hypergeometric is that binomial requires **independent** trials and the hypergeometric requires the draws be made from a collection **without replacement**

# Week 5
Binomial, Negative Binomial, Poission Distribution

# Week 6
## Average and Expected Value

Definition - Expected Value: If a discrete random variable $X$ has p.f. $f(x)$ then the number $E(X) = \Sum_{all-x}x \cdot f(x)$ is the **expected value** of X, denoted $E(X)$ (also referred to as mean or expectation)

Significance of expected value
- E(X) = the 'fair' price to pay to play a game whos payoff is X
- E(X) = the 'center of gravity' of the distribution of X

## Average and Expected Value 2
- Possion: $E(X) = \mu$
- Binomial : $f(x) = {n}\choose{x} p^x (1-p)^{n-x}$, $E(X) = np\Sum_{j = 0}{n - 1} {n-1}\choose{j} p^j (1-p)^{n-1-j}$
- Geometric: $E(X) = \frac{1-p}{p}$ 


$$E(g(X)) = \Sum_{all-x}g(x)f(x)$$
- f(x) is the probability of x

Law of expectation:
$$E(aX + b) = aE(X) + B$$
and thus (theorem for linearity)
$$ E[g(X) + h(X)] = E[g(X)] + E[h(X)] $$

## Variance and Standard Deviation
Definition - Variance: If $E(X) = \mu$, then the average squared distance between $X$ and $\mu$ is $E[(X-\mu)^2]$ ans is called the **variance** of $X$ or $Var(X)$, often denoted as $\sigma^2$
- notice that the variance is squared so if the units are km then the variance is in km squared

Defininition - **standard deviation**: The standard deviation is $\sigma$

$$Var(X) = E(X^2) - \mu^2$$
- this formula can be derived from the definition

Theorem: 
1. $Var(aX + b) = a^2Var(X)$
2. SD(aX+b) = a \times SD(X)$, where SD stands for standard deviation (just square root of the above)

**Theorem:** For many standard distributions with $E(X) = \mu$ we can use $Var(X) = E[X(X-1)] + \mu - \mu^2$


