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

# <p style="text-align: center;">6/1/20 </p>
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
 
 # <p style="text-align: center;"> 8/1/20 </p>
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
>**Theorem (p. 10):** Let $S = \{ \vec{v_1}, \vec{v_2}, \cdots, \vec{v_k} \}$ be a set of vectors in $\mathbb{R}^n$. For all $i$ satisfying $1 \leq i \leq k$, the vector $\vec{v_i}$ can be written as a linear combination of the vectors in $S - \{ \vec{v_i} \}$ if and only if 
> $$ Span(S) = Span(S-\{\vec{v_i}\}) $$
- Essentially, if some set of vectors' span encompasses a given vector, $\vec{v_i}$, then said vector ($\vec{v_i})$ can be a written as a linear combination of the vectors. The converse is also true. 
- Essentially, if a set of vectors is a subset of another set of vectors then then the "extra" vectors can be represented by some linear combination of the vectors in the subset.

**Exercise 1.3:**
Determine whether $\begin{bmatrix} 3 \\ 1 \\ 2 \end{bmatrix}$ is in $Span\{ \begin{bmatrix} 1 \\ 1 \\ 0 \end{bmatrix} , \begin{bmatrix} 1 \\ 0 \\ 1 \end{bmatrix} , \begin{bmatrix} 0 \\ 1 \\ 1 \end{bmatrix} \}.$  
We determine if there exists $c_1,c_2,c_3 \in \mathbb{R}$ such that $c_1 \begin{bmatrix} 1 \\ 1 \\ 0 \end{bmatrix} + c_2  \begin{bmatrix} 1 \\ 0 \\ 1 \end{bmatrix} + c_3 \begin{bmatrix} 0 \\ 1 \\ 1 \end{bmatrix}$


# <p style="text-align: center;"> 10/1/20 </p>
**Example 1.4:**  
Let $\{\vec{v_1},\vec{v_2},\vec{v_3}\} \subseteq \mathbb{R}^n$.   
Prove that $\vec{v_3}$ can be written as a linear combination of $\vec{v_1}$ and $\vec{v_2}$ if and only if 
$$ Span\{\vec{v_1},\vec{v_2},\vec{v_3}\}=Span\{\vec{v_1},\vec{v_2}\}$$

**Proof:**    
Let $\{\vec{v_1},\vec{v_2},\vec{v_3}\} \subseteq \mathbb{R}^n$.   
($\Rightarrow$) Assume that $\vec{v_3} = c_1\vec{v_1} + c_2\vec{v_2}$ for some $c_1,c_2 \in \mathbb{R}$.   
We prove the set equality by showing each set is a subset of the other.     
Certainly $Span\{\vec{v_1},\vec{v_2}\} \subseteq Span\{\vec{v_1},\vec{v_2},\vec{v_3}\}$.    
If $\vec{x} \in Span\{\vec{v_1},\vec{v_2}\}$ then $\vec{x} = d_1\vec{v_1} + d_2\vec{v_2}$ for some $d_1,d_2 \in \mathbb{R}$, and so 
$$ \vec{x} = d_1\vec{v_1} + d_2\vec{v_2} + 0 \cdot \vec{v_3}$$
and hence $\vec{x} \in Span\{\vec{v_1},\vec{v_2},\vec{v_3}\}$.    
Now we show $Span\{\vec{v_1},\vec{v_2},\vec{v_3}\} \subseteq Span\{\vec{v_1},\vec{v_2}\}$.    
If $\vec{x} \in Span\{\vec{v_1},\vec{v_2},\vec{v_3}\}$ then    
$\vec{x} = d_1\vec{v_1} + d_2\vec{v_2} + d_3\vec{v_3}$ for some $d_1,d_2,d_3 \in \mathbb{R}$.    
This means,     
$\vec{x} = d_1\vec{v_1} + d_2\vec{v_2} + d_3(c_1\vec{v_1} + c_2\vec{v_2})$   
$\vec{x} = (d_1 + d_3c_1)\vec{v_1} + (d_2 + d_3c_2)\vec{v_2}$    
Since $d_1 + d_3c1, d_2+d_3c2 \in \mathbb{R}$ we have shown $\vec{x} \in Span\{\vec{v_1},\vec{v_2}\}$ by definition. Therefore $Span\{\vec{v_1},\vec{v_2},\vec{v_3}\} = Span\{\vec{v_1},\vec{v_2}\}$    
$(\Leftarrow)$ Assume $Span\{\vec{v_1},\vec{v_2},\vec{v_3}\} = Span\{\vec{v_1},\vec{v_2}\}$    
Since $\vec{v_3} = 0 \cdot \vec{v_1} + 0 \cdot \vec{v_2} + 1 \cdot \vec{v_3}$ we have $\vec{v_3} \in Span\{\vec{v_1},\vec{v_2},\vec{v_3}\}$. By our assumption, we must have $\vec{v_3} \in Span\{\vec{v_1},\vec{v_2}\}$, and so $\vec{v_3}$ is a linearcombination of $\vec{v_1},\vec{v_2}$.   
QED
- The proof for a general number of vectors follows a similar structure

## Linear Dependance & Independence
>**Definition:** Let $S = \{\vec{v_1},\cdots,\vec{v_k}\}$ be a set of vectors in $\mathbb{R}^n$. We say that the set $S$ is **linearly dependent** if there exists scalars $c_1,\cdots,c_k \in \mathbb{R}$ with at least one $c_i$ non-zero, such that $c_1\vec{v_1} + \cdots + c_k\vec{v_k} = 0$    
Otherwise we call the set **linearly dependent**. 
- a set consisting of one element is not necessarily independent, consider the $0$ vector. 

>**Theorem (p. 13):** A set is linearly dependent if and only if one vector in the set is in the span of the other vectors in the set. 

**Characterizing dependence:** Tossing in $\vec{0}$ will always result in a dependent set. 

**Theorem (p. 16):** If a set of vectors $\{\vec{v_1}, \cdots , \vec{v_k}\}$ contains the zero vector then the set is linearly dependent. 

**Remarks:**
- A set of size one, $S=\{\vec{v}\}$ is linearly dependent if and only if $\vec{v}=0$
- A set of two vectors is linearly dependent if and only if one vector of $S$ is a scalar multiple of the other vector
- If it is a set of 3 or more then it gets complicated
  - If its independent then no scalar multiple pairs, however the converse is not guaranteed 
  - If its independent then there is no zero vector, the converse is not guaranteed

# <p style="text-align: center;"> 13/1/20 </p>
**Week 1 Terminology Review:**
- $\begin{bmatrix} 3 \\ -6 \end{bmatrix}$ is a linear combination of $\begin{bmatrix} 2 \\ 1 \end{bmatrix}$ and $\begin{bmatrix} 1 \\ 2 \end{bmatrix}$ since $\begin{bmatrix} 3 \\ -6 \end{bmatrix} = (4)\begin{bmatrix} 2 \\ 1 \end{bmatrix} + (-5)\begin{bmatrix} 1 \\ 2 \end{bmatrix}$
  - This shoes that $\begin{bmatrix} 3 \\ -6 \end{bmatrix}$ is an element of $Span\{\begin{bmatrix} 2 \\ 1 \end{bmatrix}, \begin{bmatrix} 1 \\ 2 \end{bmatrix} \}$
- The set $S = \{ \begin{bmatrix} 2 \\ 1 \end{bmatrix}, \begin{bmatrix} 1 \\ 2 \end{bmatrix} \}$ spans $\mathbb{R}^2$ since $\forall \vec{x} \in \mathbb{R}^2, \exists c_1,c_2 \in \mathbb{R}, \vec{x} = c_1 \begin{bmatrix} 2 \\ 1 \end{bmatrix} + c_2 \begin{bmatrix} 1 \\ 2 \end{bmatrix}$ Given a vector $\vec{x} = \begin{bmatrix} a \\ b \end{bmatrix}$ then $c_1 = \frac{2a-b}{3}$ and $c_2 = \frac{2b-a}{3}$
- The set $s = \{ \begin{bmatrix} 2 \\ 1 \end{bmatrix} , \begin{bmatrix} 1 \\ 2 \end{bmatrix} \}$ is a linearly independent set since the only scalars
- $c_1$ and $c_2$ that satisfy are $c_1 \begin{bmatrix} 2 \\ 1 \end{bmatrix} + c_2 \begin{bmatrix} 1 \\ 2 \end{bmatrix} = 0$ are $c_1 = c_2 = 0$

## Subspaces of Euclidean Spaces
>**Definition:** A subset of $\mathbb{R}^n$ is called a **subspace** of $\mathbb{R}^n$ if for all $\vec{x} \vec{y},\vec{w}$ in $S$ and all $c,d$ in $\mathbb{R}$ we have (V1 through V10 hold)  

Note:
- Commutivity gets inherited from $\mathbb{R}^n$ no matter what so V2,V3,V7,V8,V9,V10 are always true for any subset of $\mathbb{R}^n$

>**Theorem (p.23 Subspace test):**    
> Let $S$ be a subset of $\mathbb{R}^n$. If $S \neq \emptyset$ and for all $\vec{x},\vec{y} \in S$ and all $c \in \mathbb{R}$ we have $\vec{x} + \vec{y} \in S$ and $c \vec{x} \in S$, then $S$ is a subspace of  $\mathbb{R}^n$
# <p style="text-align: center;"> 15/1/20 </p>
## **Bases**
Since a linearly independent set of vectors is always simpler than a linearly dependent one and a linearly dependent set of vectors can always be reduced to a linearly independent set with the same span; the simplest set of vectors which span some set must be linearly independent. 

>**Definition: Basis**    
>Let $S = \{ \vec{v_1}, \cdots, \vec{v_k} \}$ be a subset of $\mathbb{r}^n$. If $\{ \vec{v_1}, \cdots, \vec{v_k} \}$ is a linearly independent set of vectors in $\mathbb{r}^n$ such that $S = Span\{ \vec{v_1}, \cdots, \vec{v_k} \}$, then the set $\{ \vec{v_1}, \cdots, \vec{v_k} \}$ is called a **basis** for $S$.      
>We define the basis set for $\{\vec{0}\}$ to be the empty set $\emptyset$.

>**Definition: Standard Basis:**     
>In Rn, let $\vec{e_i}$ represent the vector whose $i^{th}$ component is $1$ and all other components
are $0$. The set $\{\vec{e_1},...\vec{e_n}\}$ is called the standard basis for $\mathbb{R}^n$.

## Lines and Planes
>**Definition - Line:**  
> A **line** in $\mathbb{R}^n$ is a subset of $\mathbb{R}^n$ which can be represented using a vector equation of the form 
> $$ \vec{x} = \vec{b} + t \vec{m}, t \in \mathbb{R}$$
> for vectors $\vec{b}$ and $\vec{m}$ in $\mathbb{R}^n$ with $\vec{m} \neq 0$ 

> **Definition - Plane:**  
> A **plane** in $\mathbb{R}^n$ is a subset of $\mathbb{R}^n$ which can be represented using a vector equation of the form 
> $$ \vec{x} = \vec{b} + s \vec{u} + t \vec{v}, s,t \in \mathbb{R}$$
> for vectors $\vec{b},\vec{u},\vec{v}$ in $\mathbb{R}^n$ with $\{\vec{u},\vec{v}\}$ a linearly independent set


# <p style="text-align: center;"> 17/1/20 </p>
 
>**Theorem (p. 19):**
> If $B = \{ \vec{v_1}, \cdots, \vec{v_k} \}$ is a basis for a subset of $S$ of $\mathbb{R}^n$, then every vector in $S$ can be written as a unique linear combination of the vectors in $B$

**Proof:**    
Let $B = \{ \vec{v_1}, \cdots, \vec{v_k} \}$ be a basis for $S \subseteq \mathbb{R}^n$. Since $B$ is a spanning set for $S$, given $\vec{v_x} \in S$, there exists $c_1, c_2, \cdots, c_k \in \mathbb{R}$ such that 
$$ \vec{v_x} = c_1\vec{v_1} + c_2\vec{v_2} + \cdots + c_k \vec{v_k}$$
Now we prove these scalars are **unique**.    
Suppose we also have 
$$ \vec{v_x} = \vec{v_x} = d_1\vec{v_1} + d_2\vec{v_2} + \cdots + d_k \vec{v_k}$$   
for some $d_1, d_2, \cdots d_k \in \mathbb{R}$.    
Well then,
$$ c_1\vec{v_1} + c_2\vec{v_2} + \cdots + c_k \vec{v_k} =  d_1\vec{v_1} + d_2\vec{v_2} + \cdots + d_k \vec{v_k}$$ 
This implies 
$$ (c_1 - d_1)\vec{v_1} + (c_2 - d_2)\vec{v_2} + \cdots + (c_k - d_k)\vec{v_k} = \vec{0}$$    
By linear independence of $B$, must have $(c_1 - d_1)=0 , \cdots , (c_k - d_k)=0$. This means $c_i=d_i$ and so the scalars are unique.    
QED

>**Definition: Dot Product**    
> Given two vectors $\vec{v_x}, \vec{v_y} in \mathbb{R}^n$ the dot product of $\vec{v_x}$ and $\vec{v_y}$ is defined to be 
> $$ \vec{v_x} \cdot \vec{v_y} = \begin{bmatrix} x_1 \\ \vdots \\ x_n \end{bmatrix} \cdot \begin{bmatrix} y_1 \\ \vdots \\y_n \end{bmatrix} = x_1y_1 + \cdots x_ny_n = \sum_{i=1}^{n}x_iy_i$$

**Theorem: Properties of dot product**      
If $\vec{x}, \vec{y}, vvz \in \vec{y}$ and $s,t \in \mathbb{R}$, then we have the following: 
1. $\vec{x} \cdot \vec{x} \geq 0$ and $\vec{x} \cdot \vec{x} = 0$ if and only if $\vec{x} = 0$
2. $\vec{x} \cdot \vec{y} = \vec{y} \cdot \vec{x}$
3. $\vec{x} \cdot (s \vec{y} + t \vec{x}) = s(\vec{x} \cdot \vec{y}) + t(\vec{x} \cdot vvz)$


>**Definition: Norm**   
> Given a vector $\vec{v_x}$ in $\mathbb{R}^n$ the **length** or **norm** of $\vec{v_x}$ is defined to be 
> $$||\vec{v_x}|| = \sqrt{\vec{v_x} \cdot \vec{v_x}}$$

**Theorem: Properties of the norm**   
If $\vec{x}, \vec{y} \in \mathbb{R}^n$ and $c \in \mathbb{R}$ then we have the following: 
1. $||\vec{x}|| \geq 0$ and $||\vec{x}|| = 0$ if and only if $\vec{x} = \vec{0}$
2. $||c\vec{x}||$ = $|c| \cdot ||\vec{x}||$ (note the absolute value on $c$)
3. $| \vec{x} \cdot \vec{y}| \leq ||\vec{x}||\cdot||\vec{y}||$
4. $||\vec{x} +\vec{y}|| \leq ||\vec{x}|| + ||\vec{y}||$

>**Definition: Angle between vectors**    
> Given $\vec{v_x},\vec{v_y}$ in $\mathbb{R}^n$ the angle between $\vec{v_x}$ and $\vec{v_y}$ is defined to be a real number $\theta$ satisfying the equation 
> $$ \vec{v_x} \cdot \vec{v_y} = ||\vec{v_x}|| \cdot ||\vec{v_y}|| cos\theta$$

>**Definition: Orthogonal**   
> Two vectors $\vec{v_x}$ and $\vec{v_y}$ in $\mathbb{R}^n$ are said to be **orthogonal** when they satisfy $\vec{v_x} \cdot \vec{v_y} = 0$

>**Theorem:**     
> The zero vector is orthogonal to every vector in $\mathbb{R}^n$
# <p style="text-align: center;"> 17/1/20 </p>
# <p style="text-align: center;"> 17/1/20 </p>
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

