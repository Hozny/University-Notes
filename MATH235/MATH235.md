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
$$ rank(L) + nullity(L) = n$

## 8.3 Matrix of a Linear Mapping

**Definition - Matrix of a Linear Mapping:** Suppose $B = {\vec{v}_1, \cdots, \vec{v}_n} is a basis for $\matbb{V}$ and $C$ is a basis for a finite dimensional vector space $\vec{W}$. For $L : \mathbb{V} \rightarrow \mathbb{W}$, the **matrix of L with respect to bases $B$ and $C$** is defined by
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

