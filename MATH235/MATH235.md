# Math 235 - Linear Algebra 2 | Fall 2020 (online)

## Chapter 7 - Fundemental Subspaces
### 7.1 Bases of Fundemental Subspaces

The four fundemental subspaces are: 
- Col($A$) : column space
- Row($A$) : row space 
- Null($A$) : null space 
- Null($A^T$) : left nullspace 

> Theorem: $dim Col(A) = rank A$
> Corollary 7.1.4 : $RankA = RankA^T$

> Theorem: $rankA + dim(Null(A)) = n$

## Chapter 8 - Linear Mappings 
### 8.1 General Linear Mappings
$L : \mathbb{V} \rightarrow \mathbb{W}$

**Definition:** If this property is satisfied then a mapping is linear, $L(s\vec{x} + t\vec{y}) = sL(\vec{x}) + t L(\vec{y})$ 

> Theorem: The set L of a linear mappings from some vector space to another, is
> also a vector space 

**Definition:** $(L \circ M)\vec{v} = L(M(\vec{v}))$ is said to be the composition of L and M 

> Theorem: If $L$, and $M$ are linear mappings then $L \circ M$ is also a lienar mapping

**Definition:** If $(L \circ M)\vec{v} = \vec{v}$ and $(M \circ L)\vec{w} = \vec{w}$
Then L and M are said to be invertible and we write $M = L^{-1}$ and $L = M^{-1}$


