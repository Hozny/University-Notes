# MATH 237 - Calculus 3 | Fall 2020 

# Chapter 1
## 1.1 - Scalar Functions
$f : A \rightarrow B$ is a function where each $a \in A$ has a unique $f(a) \in B$              
called the *image* of a under $f$.
- The set $A$ is called the **domain** denoted by $D(f)$
- The set $B$ is called the **codomain** of $f$
- The subset of $B$ which consists of all $f(a)$ is called the **range** of $f$

**Definition - Scalar Function:** $f(x_1, \cdots, x_n)$ of $n$ variables whose domain is                
a subset of $\mathbb{R}^n$ and whose range is a subset of $\mathbb{R}$

Sometimes we use $\vec{x}$ to represent points in $\mathbb{R}^n$

### Finding domain / range
It is sometimes easier to visualize using a picture, example:           
$f(x, y) = \sqrt{xy}$, knowing that $xy>0$ we can see that the domain is the top right          
and bottom left quadrants of a cartesian plane


## 1.2 - Geometric Interpretation of $z = f(x,y)$
In real to real functions we think of the $y$ axis as the height at $x$,        
we extend this thinking to now think of $z$ as the height at $(x, y)$ creating a 3 dimensional surface

In general $f(x, y) = c_1 x + c_2 y + c_3$, where $c_1, c_2, c_3 \in \mathbb{R}$ represents a plane

**Definition - Level Curves:** are the curves $f(x, y) = k$ where the values of $k$ come from the range of $f$
- Set the function $z = f(x, y)$ equal to a constant and increment through the constants (heights)      
to visualize the height map (if the different heights are parallel lines it forms a plane) 

**Definition - Cross Section:** The intersection of a surface, $z = f(x, y)$, with a vertical plane
- set $x$ or $y$ to a constant to find the cross section of the plane at going through that point

### Generalization

**Definition - Level Surfaces:** A level surface of a scalar function $f(x, y, z) is defined by,             
$f(x, y, z) = k, k \in R(f)$

**Definition - Level Sets:** A level set of a scalar function $f(\vec{x}), \vec{x} \in \mathbb{R}^n$ is defined by,             
$\{ \vec{x} \in \mathbb{R}^n | f(\vec{x}) = k$, for $k \in R(f)\}$

# Chapter 2

## 2.1 - Definition of a limit
definition for a function of two variables:         
$|f(x) - L| < \epsilon|$ whenever $0 < |x - a| < \delta$

Before we define a limit we need to generalize the concept of an interval       
$(-r, r) = { x : |x| < r}$ where $r \in \mathbb{R}$         

**Definition - neighbourhood:** an r-**neighbourhood** of a point $(a, b) \in \mathbb{R}^2$ is a set 
$$N_r(a,b) = \{(x, y) \in \mathbb{R}^2 | ||(x, y) - (a,b)|| < r, r \in \mathbb{R}\}$$
- $||(x,y) - (a, b)||$ is the euclidean distance in $\mathbb{R}^2$$

**Definition - limit:** Assume $f(X,y)$ is defined in a neighbourhood of $(a,b)$, except possibly at $(a,b)$. If for every $\epsilon > 0$ there exists a $\delta > 0$ such that
$$ 0 < || (x, y) - (a, b) || < \delta \Rightarrow |f(x, y) - L| < \epsilon$$
then 
$$ lim_{(x,y) \rightarrow (a, b)} f(x, y) = L_. $$

Note that using this definition of limit is very difficult for showing limits exist, so we will develop theorems which make it easier. 

## 2.2 - Limit theorems

**Theorem - Limit Theorem 1:** if $lim_{(x, y) \rightarrow (a,b)}f(x,y)$ and $lim_{(x,y)\rightarrow (a,b)} g(x,y)$ both exist then, 
$$ lim_{(x,y)\rightarrow (a, b)} [f(x,y) + g(x,y)] = lim_{(x,y)\rightarrow (a, b)}f(x,y) + lim_{(x,y)\rightarrow (a, b)}g(x,y)$$
$$ lim_{(x,y)\rightarrow (a, b)} [f(x,y)g(x,y)] = [lim_{(x,y)\rightarrow (a, b)}f(x,y)]\cdot[lim_{(x,y)\rightarrow (a, b)}g(x,y)]$$ 
$$ lim_{(x,y)\rightarrow (a, b)} \frac{f(x,y)}{g(x,y)} = \frac{lim_{(x,y)\rightarrow (a, b)}f(x,y)}{lim_{(x,y)\rightarrow (a, b)}g(x,y)}, lim_{(x,y)\rightarrow (a, b)}g(x,y) \neq 0$$

**Theorem - Limit Theorem 2:** If  $lim_{(x, y) \rightarrow (a,b)}f(x,y)_,$ exists, then the limit is unique.
- exercise prove the theorem above.

## 2.3 - Proving a limit does not exist

With functions of one variable we should the left and right limit do not equal and thus it does not exist.          

Now we can use any line. 

Technique 1: we if we are approaching $(x,y) \rightarrow (0, 0)$$ first we use the line y = 0, and shoe that f(x,y) = a, then we use the line x = 0 and show f(x, y) = b and if $a\neq b$ then the limit does not exist

Technique 2: we can approach the limit using $y = mx$ then if we simplify to an expression which depends on the value of m then the limit is not unique and hence does not exist 

**Caution:** make sure lines used to approach the limit actually approach the limit, (if ur approaching (0,0) the line you use must be a function which actually does approach (0,0))

## 2.4 - Proving a limit exists

**Theorem - Squeeze theorem:** if there exists a function $B(x,y) such that, 
$$|f(x,y) - L| \leq B(x,y)$$
- for all $(x, y) \neq (a, b)$
in some neighbourhood of $(a,b)$ and $lim_{(x,y)\rightarrow (a,b)} B(x, y) = 0$ then 
$$lim_{(x,y)\rightarrow (a,b)} f(x, y) = L$$




    
