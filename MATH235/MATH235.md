# Math 235 - Linear Algebra 2 | Fall 2020 (online)

# Chapter 7 - Fundemental Subspaces
## 7.1 Bases of Fundemental Subspaces

The four fundemental subspaces are: 
- Col($A$) : column space
- Row($A$) : row space 
- Null($A$) : null space 
- Null($A^T$) : left nullspace 

> Theorem: $dim Col(A) = rank A$
> Corollary 7.1.4 : $RankA = RankA^T$

> Theorem: $rankA + dim(Null(A)) = n$

# Chapter 8 - Linear Mappings 
## 8.1 General Linear Mappings
$L : \mathbb{V} \rightarrow \mathbb{W}$

**Definition:** If this property is satisfied then a mapping is linear, $L(s\vec{x} + t\vec{y}) = sL(\vec{x}) + t L(\vec{y})$ 

> Theorem: The set L of a linear mappings from some vector space to another, is
> also a vector space 

**Definition:** $(L \circ M)\vec{v} = L(M(\vec{v}))$ is said to be the composition of L and M 

> Theorem: If $L$, and $M$ are linear mappings then $L \circ M$ is also a lienar mapping

**Definition:** If $(L \circ M)\vec{v} = \vec{v}$ and $(M \circ L)\vec{w} = \vec{w}$
Then L and M are said to be invertible and we write $M = L^{-1}$ and $L = M^{-1}$

## 8.2 Rank-Nullity Theorem
Kerenel
- if $\vec{v}$ is in the kernel of L then $L(\vec{v}) = 0$

Range 
- if $L(\vec{v}) = \vec{x}$ then $\vec{x}$ is in the range of L 

**Theorem - 8.2.1:** If L is a linear mapping then $L(0) = 0$

**Theorem - 8.2.1:** If $L : \mathbb{V} \rightarrow \mathbb{W}$ is a linear mapping then Ker(L) is subspace of V and Range(L) is subspace of W

**Definition - Rank / Nullity:**
- $rank(L) = dim(Range(L))$
- $nullity(L) = dim(Ker(L))$

**Theorem - 8.2.3:** if $L : \mathbb{V} \rightarrow \mathbb{W}$ and $\mathbb{V}$ is n-dimensional then
$$ rank(L) + nullity(L) = n$$

## 8.3 Matrix of a Linear Mapping

**Definition - Matrix of a Linear Mapping:** Suppose $B = {\vec{v}_1, \cdots, \vec{v}_n}$ is a basis for $\mathbb{V}$ and $C$ is a basis for a finite dimensional vector space $\vec{W}$. For $L : \mathbb{V} \rightarrow \mathbb{W}$, the **matrix of L with respect to bases $B$ and $C$** is defined by
$$ _C[L]_B = [[L(\vec{v}_1)]_C \cdots [L(\vec{v}_n]_c]$$
and satisfies
$$ [L(\vec{x})]_C = _C[L]_B[\vec{x}]_B $$
- for all $\vec{x} \in \mathbb{V}$

## 8.4 Isomorphisms

**Definition - One-To-One and Onto:** Let $L : \mathbb{V} \rightarrow \mathbb{W}$ be a linear mapping. $L$ is called **one-to-one** (*injective*) if for every $\vec{u},\vec{v} \in \mathbb{V}$ such that $L(\vec{u}) = L(\vec{v})$, we must have $\vec{u} = \vec{v}$
- $L$ is called **onto** (*surjective*) if for every $\vec{w} \in \mathbb{W}$, there exists $\vec{v} \in \mathbb{V}$ such that $L(\vec{v}) = \vec{w}$.


**Lemma 1:** Let $L : \mathbb{V} \rightarrow \mathbb{W}$ be a linear mapping. $L$ is one-to-one if and only if $Ker(L) = \{\vec{0}\}$.

**Definiton - Isomorphisms:** A vector space $\mathbb{V}$ is said to be **isomorphic$$ to a vector space $\mathbb{W}$ if there exists a linear mapping $L : \mathbb{V} \rightarrow \mathbb{W}$ which is one-to-one and onto. $L$ is called an $$isomorphism** from $\mathbb{V}$ to $\mathbb{W}$. 

**Theorem 2:** Let $\mathbb{V}$ and $\mathbb{W}$ be finite dimensional vector spaces. $\mathbb{V}$ is isomorphic to $\mathbb{W}$ if and only if $dim \mathbb{V} = dim \mathbb{W}$. 

**Theorem 3:** If $\mathbb{V}$ and $\mathbb{W}$ are both n-dimensional vector spaces and $L : \mathbb{V} \rightarrow \mathbb{W}$ is linear, then $L$ is one-to-one if and only if $L$ is onto. 

**Theorem 4:** Let $\mathbb{V}$ and $\mathbb{W}$ be isomorphic vector spaces and let $\{\vec{v}_1, \cdots, \vec{v}_n\}$ be basis for $\mathbb{V}$. A linear mapping $L : \mathbb{V} \rightarrow \mathbb{W}$ is an isomorphism if and only if $\{ L(\vec{v}_1, \cdots, L(\vec{v}_n)\}$ is a basis for $\mathbb{W}$. 


# Chapter 9 

## 9.1 Inner Products

What makes standard basis easy to use? 
1. All the vectors in the basis are orthogonal
2. All vectors in the basis have unit length

We have only defined the concept of orthogonality and length in $\mathbb{R}^n$, our goal now is to generalize this to general vector spaces

**Definition - Inner Product:** Let $\mathbb{V}$ be a vector space. An inner product on $\mathbb{V}$ is a function $\langle , \rangle : \mathbb{V} \times \mathbb{V} \rightarrow \mathbb{R}$ such that for all $\vec{v}, \vec{w}, \vec{z} \in \mathbb{V}$ and $a, b \in \mathbb{R}$ we have
1. $\langle \vec{v}, \vec{v} \rangle \geq 0$. Also $\lang \vec{v}, \vec{v} \rangle = 0$ if and only if $\vec{v} = \vec{0}$
2. $\langle \vec{v}, \vec{w} \rangle = \langle \vec{w}, \vec{v} \rangle$
3. $\langle a \vec{v} + b \vec{w}, \vec{z} \rangle = a \langle \vec{v}, \vec{z} \rangle + b \langle \vec{w}, \vec{z} \rangle$

a function with property 1 is said to be **positive definite**          
a function with property 2 is said to be **symmetric**          
a function with property 3 is said to be **left linear**

if it is has both property 1 and 2 then it is also right linear and is said to be **bilinear**

## 9.2 - Length and orthagonality 
**Thereom:** If V is an inner product space then the inner product of any vector in V with 0 is 0. 

**Theorem:** Let $\mathbb{V}$ be an innerproduct space with inner product $\langle , \rangle$. The length of $\vec{v}$ is dfeined by, 
$$ ||\vec{v}|| = \sqrt{\langle \vec{v}, \vec{v} \rangle}$$
- notice that the length of a vector can change if we change the inner product

**Definition:** Let $\mathbb{V}$ be an inner product space with inner product $\langle , \rangle$. If $\vec{v}\in\mathbb{V}$ with $||\vec{v}|| = 1$ then $\vec{v}$ is called a **unit vector**

**Theorem 9.2.1:** Let $\vec{v}, \vec{w}$ be in inner product space $\mathbb{V}$ and $t \in \mathbb{R}$. Then 
1. $||\vec{v}|| \geq 0$ , and $||\vec{v}|| = 0$ if and only if $\vec{v}  = \vec{0}$ 
2. $||t \vec{v}|| =  |t|\cdot||\vec{v}||$
3. $\langle \vec{v}, \vec{w} \rangle \leq ||\vec{v}|| \cdot ||\vec{w}||$
4. $|| \vec{v} + \vec{w} || \leq ||\vec{v}|| + || \vec{w} ||$

**Definition:** Let $\mathbb{V}$ be an inner product space. If $\vec{v}, \vec{w} \in \mathbb{V}$ such that $\langle \vec{v}, \vec{w} \rangle = 0$ then we say $\vec{v}$ and $\vec{w}$ are **orthogonal**.           
if $\{ \vec{v}_1, \cdots, \vec{v}_k \} \in \mathbb{V}$ such that $\langle \vec{v}_i , \vec{v}_j \rangle = 0$ for all $i \neq j$ then $\{ \vec{v}_1, \cdots, \vec{v}_k \}$ is called an **orthogonal set**.
- like length, orthogonality is dependent on the definition of the inner product

**Theorem 9.2.2:** Let $\mathbb{V}$ be an inner product space. $\vec{v}_1, \cdots, \vec{v}_k \}$ is an orthogonal set in $\mathbb{V}$, then 
$$ ||\vec{v}_1 + \cdots + \vec{v}_k ||^2 = ||\vec{v}_1||^2 + \cdots + ||\vec{v}_k||^2$$
- notice this is a generalization of pythagorean theorem

**Theorem 9.2.3:** Let $\mathbb{V}$ be an inner product space. If $\{ \vec{v}_1, \cdots, \vec{v}_k \}$ is an orthogonal set of non-zero vectors in $\mathbb{V}$ then the set $\{ \vec{v}_1, \cdots, \vec{v}_k \}$ is linearly independent. 

**Definition:** Let $\mathbb{V}$ be an inner product space. If $\{ \vec{v}_1, \cdots, \vec{v}_k \}$ is an orthogonal set in $\mathbb{V}$ that is a basis for $\mathbb{V}$ then we call $\{ \vec{v}_1, \cdots, \vec{v}_k \}$ an **orthogonal basis** for $\mathbb{V}$.

**Definition:** Let $\mathbb{V}$ be an inner product space. If $\{ \vec{v}_1, \cdots, \vec{v}_k \}$ is an orthogonal set of **unit vectors** in $\mathbb{V}$ that is a basis for $\mathbb{V}$ then we call $\{ \vec{v}_1, \cdots, \vec{v}_k \}$ an **orthonormal basis** for $\mathbb{V}$.

### Orthonormal Bases and Orthogonal Matrices

**Theorem 9.2.4:** If $B = \{ \vec{v}_1, \cdots, \vec{v}_n \}$ is an orthogonal basis for an inner product space $\mathbb{V}$ and $\vec{v} \in \mathbb{V}$ then the coefficient of $\vec{v}_i$ when $\vec{v}$ is written as a linear combination of the vectors in $B$ is 
$$\frac{ \langle \vec{v}, \vec{v}_i \rangle }{ || \vec{v}_i||^2}$$
- so $\vec{v}$ is written as the sum of all the possible $\vec{v}_i$

**Theorem 9.2.6:** If $P \in M_{n \times n}(\mathbb{R})$ then teh following are equivalent:
1. The columns of $P$ form an orthonormal basis for $\mathbb{R}^n$
2. $P^T = P^{-1}$
3. The rows of $P$ form an orthonormal basis for $\mathbb{R}^n$
    - recall equivalence means that if one is true then all are true, and if one is false then all are false

**Definition:** Let $P \in M_{n \times n}(\mathbb{R})$ whose columns form an orthonormal basis for $\mathbb{R}^n$. Then, $P$ is called an **orthogonal matrix**
- **notice** *orthogonal* matrices have *orthonormal* column vectors

**Theorem 9.2.7** if $P$ and $Q$ are $n \times n$ **orthogonal** matrices and $\vec{x}, \vec{y} \in \mathbb{R}^n$, then:
1. $(P\vec{x}) \cdot (P\vec{y}) = \vec{x} \cdot \vec{y}$
2. $||P\vec{x}|| = ||\vec{x}||$
3. $det P = \pm 1$
4. All real eigenvalues of $P$ are $1$ or $-1$
5. $PQ$ is also an orthogonal matrix

## 9.3 The Gram-Schmidt Procedure

**Theorem 9.3.1 - Gram-Schmidt Orthogonalization Theorem):** Let $\{ \vec{w}_1 , \cdots , \vec{w}_n \}$ be a basis for an inner product space $\mathbb{W}$. If we define $\vec{v}_1, \cdots, \vec{v}_n$ successively as follows: 
$$ \vec{v}_1 = \vec{w}_1 $$
$$ \vec{v}_2 = \vec{w}_2 - \frac{ \langle \vec{w}_2, \vec{v}_1 \rangle}{||\vec{v}_1||^2} \vec{v}_1 $$
$$ \vec{v}_i = \vec{w}_i - \frac{ \langle \vec{w}_i, \vec{v}_1 \rangle}{||\vec{v}_1||^2} - \frac{ \langle \vec{w}_i, \vec{v}_2 \rangle}{||\vec{v}_2||^2} \vec{v}_2 - \cdots - \frac{ \langle \vec{w}_i, \vec{v}_{i-1} \rangle}{||\vec{v}_{i-1}||^2} \vec{v}_{i-1}$$
- for $3 \leq k \leq n$ then $\vec{v}_1, \cdots, \vec{v}_n$ is an orthogonal basis for $Span \{ \vec{w}_1, \cdots, \vec{w}_n \}$ for $1 \leq k \leq n$

**Theorem 9.3.2 - QR-Decomposition:**
Let $A = [ \vec{a}_1 \cdots \vec{a}_n ] \in M_{m \times n}(\mathbb{R})$ where $dimCol(A) = n$. Let $\vec{q}_1, \cdots, \vec{q}_n$ denote the vectors that result from applying the Gram-Schmidt procedure to the columns of $A$ (in order) and the normalizing. If we define 
$$ Q = [ \vec{q}_1, \cdots, \vec{q}_n ]$$
and 
$$ R = \begin{bmatrix} \vec{a}_1 \cdot \vec{q}_1 & \vec{a}_2 \cdot \vec{q}_1 & \cdots & \vec{a}_n \cdot \vec{q}_1 \\ 
0 & \vec{a}_2 \cdot \vec{q}_2 & \cdots & \vec{a}_n \cdot \vec{q}_2 \\ 
0 & 0 & \ddots & \vec{a}_n \cdot \vec{q}_{n-1} \\ 
0 & \cdots & 0 & \vec{a}_n \cdot \vec{q}_{n}\end{bmatrix}$$
then $Q$ is orthogonal, R is invertible, and 
$$ A = QR $$

## 9.4 General Projections

**Definition - Orthogonal Complement:** Let $\mathbb{W}$ be a subspace of an inner product space $\mathbb{V}$. The **orthogonal complement** $\mathbb{W}^\bot$ of $\mathbb{W}$ in $\mathbb{V}$ is defined by 
$$ \mathbb{W}^\bot = \{ \vec{v} \in \mathbb{V} | \langle \vec{w}, \vec{v} \rangle = 0 , \forall \vec{w} \in \mathbb{W} \}$$

**Theorem 9.4.1:** Let $\{ \vec{v}_1, \cdots, \vec{v}_k \}$ be a spanning set for a subspace $\mathbb{W}$ of an inner product space $\mathbb{V}$, and let $\vec{x} \in \mathbb{V}$. We have $\vec{x} \in \mathbb{W}^\bot$ if and only if$\langle \vec{x} , \vec{v}_i \rangle = 0$ for $1 \leq i \leq k$

**Theorem 9.4.2:** If $\mathbb{W}$ is a subspace of an inner product space $\mathbb{V}$ , then 
1. $\mathbb{W}^\bot$ is a subspace of $\mathbb{V}$
2. If $dim \mathbb{V} = n$, then $dim\mathbb{W}^\bot = n - dim \mathbb{W}$
3. If $dim \mathbb{V} = n$, then $(\mathbb{W}^\bot)^\bot = W$
4. $\mathbb{W} \cap \mathbb{W}^\bot = \{ \vec{0} \}$
5. If $dim \mathbb{V} = n$, $\{ \vec{v}_1, \cdots, \vec{v}_k \}$ is an orthogonal basis for $\mathbb{W}$ , and $\{ \vec{v}_{k+1} , \cdots , \vec{v}_n \}$ is an orthogonal basis for $\mathbb{W}^\bot$, then $\{ \vec{v}_1, \cdots, \vec{v}_k, \vec{v}_{k+1}, \cdots, \vec{v}_n \}$ is an orthogonal basis for $\mathbb{V}$

**Definition - Projection Perpendicular:** Suppose $\mathbb{W}$_ is a k-dimensional subspace of an inner produce space $\mathbb{V}$ and $\{\vec{v}_1 , \cdots , \vec{v}_k \}$ is an orthogonal basis for $\mathbb{W}$. For an $\vec{v} \in \mathbb{V}$ we define the **projection** of $\vec{v}$ onto $\mathbb{W}$ by 
$$ proj_{\mathbb{W}}(\vec{v}) = \frac{ \langle \vec{v}, \vec{v}_1 \rangle }{||\vec{v}_1||^2}\vec{v}_1 + \cdots + \frac{\langle \vec{v}, \vec{v}_k \rangle }{ || \vec{v}_k || } \vec{v}_k$$
and the **perpendicular** of the projection is defined by, 
$$ perp_\mathbb{W}(\vec{v}) = \vec{v} - proj_\mathbb{W}(\vec{v}) $$

**Theorem 3:** If $\mathbb{W}$ is a k-dimensional subspace of an inner product space $\mathbb{V}$, then for any $\vec{v} \in \mathbb{V}$ we have 
$$ perp_\mathbb{W}(\vec{v}) = \vec{v} - proj_\mathbb{W}(\vec{v})  \in \mathbb{W}^\bot$$

**Theorem 4:** If $\mathbb{W}$ is a k-dimensional subspace of an inner product space $\mathbb{V}$, then $proj_{\mathbb{W}}$ is al inear operator on $\mathbb{V}$ with kernal $\mathbb{W}^\bot$

**Theorem 5:** If $\mathbb{W}$ is a subspace of a finite dimensional inner product spave $\mathbb{V}$, then for any $\vec{v} \in \mathbb{V}$ we have 
$$ proj_{\mathbb{W}^\bot}(\vec{v}) = perp_{\mathbb{W}}(\vec{v})$$
