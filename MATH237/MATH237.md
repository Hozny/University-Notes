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

# Chapter 3
## 3.1 - Definition of a continuous function 

A single variable function is continuous iff: 
1. $f$ is defined at $x = a$
2. $lim_{x \rightarrow a} f(x)$ exists, which means the left and right limits exist and are equal 
3. $lim_{x \rightarrow a} f(x) = f(a)$

For a function $f(x,y)$ to be continuous we can intuively see that this means there are no "breaks" or "holes" in the surface

**Definition - Continuous:** A function $f(x,y)$ is continuous at $(a,b)$ if and only if
$$lim_{(x,y) \rightarrow (a,b)} f(x, y) = f(a,b)$$
Additionally, if $f$ is continuous at every point in a set $D_1 \subset \mathbb{R}^2$

*Remark* just like single variable calculus there are three requirements in this definition: 
1. the limit exists
2. f is defined at (a, b)
3. the limit as (x,y) -> (a, b) f(x, y) = f(a, b)

## 3.2 - The continuity theorems

We will defined basic functions which can be understood as continuous on their domain without further explanation.      
Using these functions we will view other functions as compositions of simpler functions to make proving continuity easier. 

List of continuous functions: 
- the constant function $f(x, y) = k$
- the power functions $f(x, y) = x^n$, $f(x, y) = y^n$
- the logarithm function $ln(\cdot)$
- the exponential fucntion $e^{(\cdot)}$
- the trigonometric functions, $sin(\cdot), cos(\cdot)$, etc. 
- the inverse trigonometric functions, $arcsin(\cdot)$, etc. 
- the absolute value function $|\cdot|$

**Definition - Operations on functions:** if $f(x, y)$ and $g(x, y)$ are scalar functions and (x, y) is in the domain of both functions then: 
1. the **sum** is $f+g$ is defined by $(f+g)(x, y) = f(x, y) + g(x, y)$
2. the **product $fg$ is defined by $(fg)(x, y) = f(x,y)g(x, y)$
3. the **quotient** $\frac{f}{g}$ is defined by $(\frac{f}{g})(x, y) = \frac{f(x, y)}{g(x, y}$ if $g(x, y) \neq 0$

## 3.2 - The continuity theorems

**Theorem: Continuity theorem 1:** if $f$ and $g$ are continuous at $(a, b)$ then $f + g$ and $fg$ are continuous at $(a, b)$

**Theorem: Continuity theorem 2:** if $f$ and $g$ are continuous at $(a, b)$ and $g(a, b) \neq 0$ then $\frac{f}{g}$ is continuous at $(a, b)$ 

**Theorem: Continuity theorem 3:** if $f$ and $g$ are continous at $(a, b)$ then their composition is continuous

# Chapter 4
## Chapter 4.1 - Partial Derivatives

**Definition - Partial Derivatives:** The **partial derivatives** of $f(x,y)$ are defined by 
$$ \frac{\delta f}{\delta x}(x, y) = f_x(x, y) = lim_{h \rightarrow 0} \frac{f(x + h, y) - f(x, y)}{h}$$
$$ \frac{\delta f}{\delta y}(x, y) = f_y(x, y) = lim_{h \rightarrow 0} \frac{f(x, y + h) - f(x, y)}{h}$$
- provided that these limits exist

**Remark:** sometimes it's convenient to use **operator notation**, if $f$ has variables $x$ and $y$
$$D_1f=\frac{\delta f}{\delta x} = f_x$$
$$D_2f=\frac{\delta f}{\delta y} = f_y$$
- sometimes we abbreviate and only write $\frac{\delta f}{\delta y}$

note that the conept of partial derivatives does not match our definition of derivative for single variable functions, where differentiability imples continuity (this is not the case for partial derivatives). 


We can generalize this concept to a scalar function of $n$ variables $f(\vec{x}), \vec{x} \in \mathbb{R}^n$, where we find the partial derivative of $f$ with respect to its $i$-th variable, we hold **all the other variables constant**. 


## Chapter 4.2 - Higher-Order Partial Derivatives

Since we have two first order partial derivatives (1 for each variables) then we have 4 total combinations for second order partial derivitaves. 
- it is often convenient to use subscript or operator notation


**Theorem 1 - Clairaut's Theorem:** If $f_{xy}$ and $f_{yx}$ are defined in some neighbourhood of $(a,b)$ and are both continuous at $(a,b)$, then 
$$f_{xy}(a,b) = f_{yx}(a,b)$$
- the proof of this theorem is beyond the scope of this course

### Higher-order partial derivatives
observe that $f(x,y)$ has eight third partial derivatives
- Clairaut's theorem holds ofr higher-order partial derivatives (the partial derivative is equal to another when they contain the same partial derivatives in a different arrangements)

**Terminology:** if the $k$-th partial derivatives of $f(x_1, \cdots, x_n)$ are continuous then we write, 
$$ f \in C^k $$
- and say "$f$ is in class $C^k$."

## Chapter 4.3 - Tangent Plane
**Definition - Tangent Plane:** The **tangent plane** to $z = f(x,y)$ at the point $(a, b, f(a, b))$ is 
$$ z = f(a, b) + \frac{\delta f}{\delta x}(a,b)(x - a) + \frac{\delta f}{\delta y}(a, b)(y - b)$$

## Chapter 4.4 - Linear Approximation for $z = f(x, y)$

### Review of the 1D case
$L_a(X) = f(a) + f'(a)(x-a)$ and is called the **linearization** of $f$ at $a$ since it approximates $f(x)$ for $x$ sufficiently close to $a$

# Chapter 5 - Differentiable Functions

## Chapter 5.1 - Definition of Differentiability

**Theorem 1 - differentiability of single variable**: if $g'(a)$ exists then $lim_{x \rightarrow a} \frac{ | R_{1,a}(x) | }{|x-a|} = 0$ where 
$$ R_{1,a}(x) = g(x) - L_a(x) = g(x) - g(a) - g'(a)(x-a) $$


**Definition - Dirrefentiable:** a function $f(x, y)$ is **differentiable** at $(a,b)$ if 
$$ lim_{(x,y) \rightarrow (a, b)} \frac{|R_{1,(a,b)}(x, y)|}{||(x, y) - (a, b)||} = 0$$
where
$$R_{1, (a, b)}(x, y) = f(x, y) - L_{(a, b)}(x, y)$$
- as with the one dimensional case there is only one plane which satisfies this result

**Theorem 2:** if a function $f(x, y)$ satisfies
$$ lim_{(x, y) \rightarrow (a, b)} \frac{ |f(x, y) - f(a, b) - c(x - a) - d(y - b)|}{|| (x, y) - (a, b)||} = 0$$
for some constants $c$ and $d$ then $c = f_x(a, b)$ and $d = f_y(a, b)$

A function which is not differentiable at a point $a_1$ has the property that the linear approximation doesn't get any better at approximating the function as we get closer to the point
- this is equivalent to saying there is no good plane to represent the tangent plane at that point

**Definition - Tangent Plane:** if $f$ is differentiable at $(a, b)$ then the tangent plane of the surfance is, 
$$ z = f(a, b) + \frac{\delta f}{\delta x} (a, b) (x - a) + \frac{\delta f}{\delta y}(a, b)(y - b) $$
## Chapter 5.2 - Differentiability and Continuity

**Theorem 1:** if $f(x, y)$ is differentiable at $(a, b)$ then $f$ is continuous at $(a, b)$

## Chapter 5.3 - Continuous Partial Derivatives and Differentiability 

**Theorem 1 - The mean value theorem:** If $f(x)$ is continuous on the closed interval $[x_1, x_2]$ and $f$ is differentiable on the open interval $(x_1, x_2)$, then there exists $x_0 \in (x_1, x_2)$ such that
$$f(x_2) - f(x_1) = f'(x_0)(x_2 - x_1)$$

**Theorem 2:$$ if the partial derivatives $f_x$ and $f_y$ are both continuous at $(a, b)$ then $f(x, y)$ is differentiable at $(a, b)$

**Generalization**
**Definition - Differentiability for $f : \mathbb{R}^n \rightarrow \mathbb{R}$**            
A function $f : \mathbb{R}^n \rightarrow \mathbb{R}$ is differentiable at point $\vec{a}$ if 
$$ lim_{\vec{x} \rightarrow \vec{a}} \frac{ | f(\vec{x}) - f(\vec{a}) - L_{\vec{a}}(\vec{x} - \vec{a})|}{||\vec{x} - \vec{a}||} = 0$$
where $L : \mathbb{R}^n \rightarrow \mathbb{R}$ is a linear transformation

**Theorem 1 for functions of $n$ variables** if $f(x_1, \cdots, x_n)$ is differentiable at $\vec{a}$ then $f$ is continuous at $a$

**Theorem 2 for functions of $n$ variables** if $f_1, \cdots f_n$ are continuous at $\vec{a}$ then $f$ is differentiable at $\vec{a}$

## Chapter 5.4 - Linear Approximation Revisited
$$f(x, y) \approx f(a, b) + \Delta f(a, b) \cdot (x - a, y - b) $$

# Chapter 6 - Chain Rule
## Chapter 6.1 - Basic Chain Rule in two dimensions
First, 
$$\frac{ dT }{ dt } = \frac{\delta T}{\delta x} \frac{dx}{dt} + \frac{\delta T}{\delta y} \frac{dy}{dt} $$
Recall that $T(x) = f(x(t), y(t))$ $$T'(x) = \frac{d}{dt}f(x(t), y(t)) = f_x(x(t), y(t))x'(t) + f_y(x(t), y(t)) y'(t)$$

**Theorem - Chain Rule:** Let $G(t) = f(x(t), y(t))$, and let $a = x(t_0)$ and $b = y(t_0)$. If $f$ is differentiable at $(a, b)$ and $x'(t_0)$ and $y'(t_0)$ exist, then $G'(t_0)$ exists and is given by
$$ G'(t_0) = f_x(a, b) x' (t_0) + f_y(a, b)y'(t_0) $$

Vector form: 
$$\frac{d}{dt} f(\vec{x}(t)) = \Delta f(\vec{x}(t)) \cdot \frac{d\vec{x}}{dt}(t)$$

## 6.2 - Extension of basic chain rule
Use a tree to apply the following algorithm: 
1. Identify all of the variables
2. Take all possible paths from the differentiated variable to the differentiating variable
3. For each lik in a given path, differentiate the upper variable with respect to the lower variable being carefule to consider if thsi is a derivative or a partial derivative. Multiply all such derivatives in that path. 
4. Add the products from step 3 together to complete the Chain Rule

# Chapter 7 - Directional Derivatives and the Gradient Vector

## Chapter 7.1 - Directional Derivative
The **directional derivative** of $f(x, y)$ at a point $(a, b)$ in the direction vector of a **unit vector** $\vec{u} = (u_1, u_2)$ where $||\vec{u}|| = 1$ is defined by
$$D_{\vec{u}}f(a, b) = \frac{d}{ds}f(a + su_1, b + su_2) \rvert_{s=0}$$

**Theorem 1 - Directional Derivative (DD) Theorem:** If $f(x, y)$ si differentiable at $(a, b)$ and $\vec{u} = (u_1, u_2)$ where $||\vec{u}|| = 1$ is a **unit vector**, then 
$$D_{\vec{u}}f(a, b) = \Delta f(a, b) \cdot \vec{u}$$
where $\cdot$ reperesents the dot product

# Chapter 8 
## Chapter 8.1 - The Taylor Polynomial of Degree 2
**Definition - 2nd degree Taylor polynomial:** Let $f$ be a function of two variables. The **second degree Taylor polynomial** $P_{2, (a, b)}$ of $f(x, y)$ and $(a, b)$ is given by 
$$ P_{2, (a, b)}(x, y) = f(a, b) + f_x(a, b)(x - a) + f_y(a, b)(y - b) + \frac{1}{2} [f_{xx}(a, b)(x-a)^2 + 2f_{xy}(a, b)(x-a)(y-b) + f_{yy}(a, b)(y - b)^2]$$
- the second degree Taylor polynomial approximates the functiona round (a, b) with better accuracy than the linear approximation (a plane in comparison to a paraboloid)

## Chapter 8.2 - Taylor's Formula with Second Degree Remainder

**Theorem 2 - Taylor's Theorem for Functions of Two Variables**
## Chapter 8.3 Generalizations of the Taylor Polynomial

**Definition - The **k-th degree Taylor polynomial** of a function $f(x, y)$ is
$$ P_{k, (a, b)}(x, y) = \Sum_{|a| \leq k} \delta^\alpha f(a, b) = \frac{ [(x, y) - (a, b)]^\alpha}{\alpha !}$$
- summing over $|a| \leq k$ means we consider all of the mixed partial derivatives whose orders sum to k or less
- $\alpha$ is a set of numbers where the number in the ith position represents the order of the partial derivative of the ith variable of the function
    - raising to the exponent of alpha means the terms with the ith variable are raised to the ith value in alpha

**Theorem: Taylor's Theorem of order $k$**

**Definition: Taylor polynomial of degree k for functions of n variables:**

# Chapter 10 : Optimization Problems
## 10.1 The extreme value theorem 
Definition: Bounded Set: A set $S \subset \mathbb{R}^2$ is said to be bounded if and only if it is contained in some neighbourhood of the origin
- this implies that any point in $S$ has finite distance to $(0,0)$


**Definition - Boundary Point:** Given a set $S \subset \mathbb{R}^2$ a point $(a, b) \in \mathbb{R}^2$ is said to be a boundary point of S if and only if every neighbourhood of $(a, b)$ contains at least one point in S and one point not in S

**Definition - Boundary of $S$:** is the set $B(S)$ which contains all boundary points of S is called the boundary set of S 

**Definition - Closed set:** A set $S \subseteq \mathbb{R}^2$ is said to be closed if S contains all of its boundary points

### The extreme value theorem for functions of two variables
Theorem - EVT for functions of two variables: If $f(x, y)$ is continuous on a  closed and bounded set $S \subset \mathbb{R}^2$ then there exist points $(a, b), (c, d) \in S$ such that 
$$ f(a, b) \leq f(x, y) \leq f(c, d)$$
- for all $(x, y) \in S$

So a function of two variables which is continuous on a bounded and closed set will always have absolute maxima and minima

## 10.2 - Algorithm for Extreme Valuestttttt

**Algorithm:**      
First, check to see if the given set $S \subset \mathbb{R}^2$ is closed and bounded     
Next check if $f(x, y)$ is continuous on $S$
1. find all critical points in $S$
2. evaluate $f$ at each critical point
3. find the maximum and minimum values of $f$ on the boundary $B(S)$
4. Compare the maximum value from step 3 and 2. Compare the minimum value from step 3 and 2. 

## 10.3 - optimzation with constraints

**Lagrange Multiplier Algorithm:** Assume that $f(x, y)$ is a differentiable function and $g \in C^1$. To find the maxmimum and minimum value of f with contraint $g(x, y) = k$, evalute $f(x, y)$ at all points $(a, b)$ which satisfy one of the following conditions. 
1. $\nabla f(a, b) = \lambda \nabla g(a, b)$ and $g(a, b) = k$
2. $\nabla g(a, b) = (0, 0)$ and $g(a, b) = k$
3. $(a, b)$ is an end point of the curve $g(x, y) = k$

The maximum/minimum value of $f(x, y)$ is the largest/smallest value of $f$ obtained at the points found in conditions 1-3

The variable $\lambda$ is called the **Lagrange multiplier** an can be very useful in some real world applications

Remarks. 
1. observe that condition 2 must be included since we assumed the gradient vector of g does not equal 0 in the derivation
2. if the curve $g(x, y) = k$ is unbounded then we need to consider the limit ad (x, y) go to infinity of f(x, y) which satisfy g(x, y) = k
    - we will not see such cases in this course

### Generalization
The method of lagrange multipliers can be generalized to function of $n$ varaibles $f(\vec{x}), \vec{x} \in mathbb{R}^n$ and with $r$ constraints of the form.          
$$g_1(\vec{x}) = 0, \cdots, g_r(\vec{x}) = 0$$
In order to find the possible maximum and minimum points of $f$ subject to the contraint, we find all points $\vec{x}$ such that
$$\nabla f(\vec{a}) = \lambda_1 \nabla g_1(\vec{a}) + \cdots + \lambda_r \nabla g_r(\vec{a})$$
- $g_i(\vec{a}) = 0$ for $1 \leq i leq r$

Notice the scalars $\lambda$ are the Lagrange multipliers




























































