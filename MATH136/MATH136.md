# MATH 136
Linear Algebra 1
``` 
Instructor: Carrie Knoll
Section: Monday/Wednesday Monday & Wednesday 1:30 p.m.-2:20 p.m.
Email: caknoll@uwaterloo.ca
Office: MC 6236
Office Hours: Mon: 10am-11am, Wed:3pm-4pm, Fri: 9:30am-10:30am
Textbook: Course Notes
Midterm: Monday, February 10, 7:00-8:50 p.m.
```

Week|Dates|Sections|Topics|
---|---|---|---
|1|Jan 6-10|1.1, 1.2|Vectors in Rn, Spanning, Linear Independence|
2|Jan 13-17|1.2, 1.3, 1.4|Bases, Subspaces, Dot Product|
3|Jan 20-24|1.4, 1.5, 2.1|Cross Product, Projections, Systems of Linear Equations|
4|Jan 27-31|2.2, 3.1|Systems of Linear Equations, Matrices|
5|Feb 3-7|3.1, 3.2|Matrix Operations, Matrix Mappings|
6|Feb 10-14|3.2, 3.3, 3.4|Linear Mappings, Special Subspaces, Operations on Mappings|
7|Feb 17-21|READING WEEK||
8|Feb 24-Feb 28|4.1, 4.2|Vector Spaces, Bases9Mar 2-64.2, 4.3Dimension, Coordinates|
10|Mar 9-13|5.1, 5.2|Matrix Inverse, Elementary Matrices|
11|Mar 16-20|5.3, 5.4|Determinants, Inverse by Cofactors, Cramer's Rule|
12|Mar 23-27|5.5, 6.1, 6.2|Area and Volume, Similar Matrices, Eigenvalues|
13|Mar 30-Apr 3|6.2, 6.3, 6.4|Diagonalization, Powers of Matrices

# <p style="text-align: center;">6/1/14 </p>
## Functions
In first year calculus, we study real numbers, $\mathbb{R}$, and functions on the real numers, $f:\mathbb{R} \rightarrow \mathbb{R}$

we ask questions about domain, range, injecti\vec{v_i}ty, surjecti\vec{v_i}ty, invertibility, extrema, continuity, differentiability, integrability, etc.

There are many important functions that do not have domain and codomain $\mathbb{R}$. Let's start by introducing just one new set of objects to consider as inputs and outputs for our functions: 

### Functions $f: \mathbb{R}^{n} \rightarrow \mathbb{R}^m$
$$
\mathbb{R}^{2} = \{(x,y):x,y \in \mathbb{R}\}
$$

>**Real Vectors**: $\mathbb{R}^{n} = \vec{x} = (x_1, x_2,\cdots, x_n): x_i \in \mathbb{R}$


In multivariate calculus and vector calculus, you will talk about graphing functions like this and discuss things liek continuity and differentiability
in **linear algebra** we focus our time as follows: 
- Consider functions $f: \mathbb{R}^{n} \rightarrow \mathbb{R}^m$ that are **linear**
- Ask **algebraic** questions like: 
  - Is $\vec{y}$ in the range of $f$? 
  - What is the range of $f$? 
  - Is f injective? 
  - if m=n, then do we have $f(\vec{x})=\lambda\vec{x}$ for any vector $\vec{x}$

## Chapter 1
> **Definition:** the **n-dimensional Euclidean space**, or $\mathbb{R}^n$, consists of all objects of the form 
> $$\vec{x} = \begin{bmatrix} x_1 \\ x_2 \\ \vdots \\ x_n \end{bmatrix} $$ 
> where $x_1, x_2, \cdots, x_n$ are in $\mathbb{R}$

**Note**: 
- Two **vectors** in $\mathbb{R}$ are equal if their corresponding components are equal, that is, $\vec{x} = \vec{y}$ iff $x_i=y_i$ for $1\leq i \leq n$

In linear algebra all vectors should be denoted with column vectors. However, sometimes n-tuples are used to match notation commonly used in other areas. 

  - $f(x_1, x_2, \cdots, x_n)$ rather than $f(\begin{bmatrix}x_1 \\ x_2 \\ \vdots \\ x_n\end{bmatrix})$

### Arithmetic in $\mathbb{R}$
there are two basic operations performed on vectors in $\mathbb{R}$
> **Definition - Multiplication:**
> Given a scalar $c \in \mathbb{R}$ and a vector $\vec{x}\in \mathbb{R}$ we define $c\vec{x}$ to be 
> $$c \begin{bmatrix} x_1 \\ x_2 \\ \vdots \\ x_n \end{bmatrix} = \begin{bmatrix} cx_1 \\ cx_2 \\ \vdots \\ cx_n \end{bmatrix} $$  

> **Definition - Vector Addition:**
> Given two vectors $\vec{x},\vec{y}\in \mathbb{R}$ we define $\vec{x} + \vec{y}$ to be 
> $$ \begin{bmatrix} x_1 \\ x_2 \\ \vdots \\ x_n \end{bmatrix} + \begin{bmatrix} y_1 \\ y_2 \\ \vdots \\ y_n \end{bmatrix}= \begin{bmatrix} x_1 + y_1 \\ x_2 + y_2 \\ \vdots \\ x_n + y_n \end{bmatrix} $$  

>**Theorem - (p, 4, properties of vector arithmetic)**    
>if $\vec{x},\vec{y}$ are vectors from $\mathbb{R}$ and $c$ and $d$ are scalars from $\mathbb{R}$, then:  
>(V1) $\vec{x} + \vec{y}$ is in $\mathbb{R}$     
>(V2) $(\vec{x} +\vec{y}) + \vec{w} = \vec{x} + (\vec{y} + \vec{w})$    
>(V3) $\vec{x} + \vec{y} = \vec{y} + \vec{x}$   
>(V4) There exists a vector $\vec{0} \in \mathbb{R}$    such that $\vec{x} + \vec{0} = \vec{x}$ for all $\vec{x} \in \mathbb{R}$     
>(V5) For every $\vec{x} \in \mathbb{R}$ there exists $(-\vec{x}) \in \mathbb{R}$ such that $\vec{x} + (-\vec{y}) = \vec{0}$    
>(V6) $c\vec{x} \in \mathbb{R}$     
>(V7) $c(d\vec{x}) = (cd)\vec{x}$   
>(V8) $(c+d)\vec{x} = c\vec{x} + d\vec{x}$  
>(V9) $c(\vec{x} + \vec{y}) = c\vec{x} + c\vec{y}$  
>(V10) $1\vec{x} = \vec{x}$ 
>copy the rest down

****Note**:** The zero vector is $\vec{0} = (0, \cdots, 0)$ and the inverse $(-\vec{x})$ is $(-1)\vec{x}$  
we define the operation of subtraction by $\vec{x}-\vec{y} = \vec{x} + (-1)\vec{y}$
 
 # <p style="text-align: center;"> 8/1/14 </p>
 **Parallelogram Rule:** When adding vectors, the result is the diagonal of the parallelogram formed by the two vectors. The difference of the vectors works similarly.  
  
 Pro\vec{v_i}ng the diagonals of a parallelogram are parallel:   
 Let $\vec{u}$ and $\vec{v}$ be sides of a parallelogram with point $E$ being the intersection of both diagonals of this parallelogram. Note that $\vec{u}$ and $\vec{v}$ cannot lie on the same line and as such are not scalar multiples of each other.   
 One diagonal can be expressed as $\vec{u} - \vec{v}$ and other other as $\vec{u} + \vec{v}$. 

>**Definition - Linear Combination:** Let $\vec{v_1} , \vec{v_2} , \cdots , \vec{v_k}$ be $k$ vectors from $\mathbb{R}^n$. Any sum in the form:
>$$c_1 \vec{v_1} + c_2 \vec{v_2} + \cdots + c_k \vec{v_k}\ | c_1, \cdots, c_k \in \mathbb{R}^n$$
>is called a **linear combination** of the vectors $\vec{v_1} , \vec{v_2} , \cdots , \vec{v_k}$.

>**Definition - Span:** Let $B = \{ c_1 \vec{v_1}, c_2 \vec{v_2}, \cdots, c_k \vec{v_k}\}$ be a set of vectors in $\mathbb{R}^n$. We define the **span** of $B$ by 
>$$Span(B) = \{ c_1 \vec{v_1} + c_2 \vec{v_2} + \cdots + c_k \vec{v_k}\ | c_1, \cdots, c_k \in \mathbb{R}^n \}$$
>We say that Span$B$ is **spanned** by $B$ and that $B$ is a **spanning set** for Span$B$.  
- The span of some set of vectors $B$ is the set of all scalar multiples of the vectors in $B$.

>**Theorem *unnamed*:** Let $\vec{v_1}, \vec{v_2}, \cdots, \vec{v_k} \in \mathbb{R}^n$. Some vector $\vec{v_i}, 1 \leq i \leq k$ can be written as a linear combination of $\vec{v_1}, \vec{v_2}, \cdots, \vec{v_{i-1}}, \vec{v_{i+1}, \cdots , \vec{v_k}}$ if and only if 
>$$Span\{\vec{v_1},\cdots,\vec{v_k}\}=Span\{\vec{v_1}, \vec{v_2}, \cdots, \vec{v_{i-1}}, \vec{v_{i+1}, \cdots , \vec{v_k}}\}$$
alternatively
>**Theorem (p. 10):** Let $S = \{ \vec{v_1}, \vec{v_2}, \cdots, \vec{v_k} \}$ be a set of vectors in $r^n$. For all $i$ satisfying $1 \leq i \leq k$, the vector $\vec{v_i}$ can be written as a linear combination of the vectors in $S - \{ \vec{v_i} \}$ if and only if 
> $$ Span(S) = Span(S-\{\vec{v_i}\}) $$
- Essentially, if some set of vectors' span encompasses a given vector, $\vec{v_i}$, then said vector ($\vec{v_i})$ can be a written as a linear combination of the vectors. The converse is also true. 
- Essentially, if a set of vectors is a subset of another set of vectors then then the "extra" vectors can be represented by some linear combination of the vectors in the subset.

**Exercise 1.3:**
Determine whether $\begin{bmatrix} 3 \\ 1 \\ 2 \end{bmatrix}$ is in $Span\{ \begin{bmatrix} 1 \\ 1 \\ 0 \end{bmatrix} , \begin{bmatrix} 1 \\ 0 \\ 1 \end{bmatrix} , \begin{bmatrix} 0 \\ 1 \\ 1 \end{bmatrix} \}.$  
We determine if there exists $c_1,c_2,c_3 \in \mathbb{R}$ such that $c_1 \begin{bmatrix} 1 \\ 1 \\ 0 \end{bmatrix} + c_2  \begin{bmatrix} 1 \\ 0 \\ 1 \end{bmatrix} + c_3 \begin{bmatrix} 0 \\ 1 \\ 1 \end{bmatrix}$

# <p style="text-align: center;"> 8/1/14 </p>
---
#### latex reference for me to write this
$$\vec{o}$$
$$
f(x) = \frac{x^2+2x-1}{(x-23)^{32}}
$$

Let's try matrices
$$
\begin{bmatrix}
1 & 2 & \cdots & 4 \\
5 & 6 & \cdots & 7 \\
\vdots & \vdots & \ddots & \vdots \\
12 & 13 & 14 & 15
\end{bmatrix}
$$ 

--- 

this is an inline matrix 
$
\begin{bmatrix}
1 & 2 \\
3 & 4
\end{bmatrix}
$

