# MATH 138
Calculus 2
``` 
Instructor: Jen (Jennifer) Nelson
Section: idk
Email: jen.nelson@uwaterloo.ca
Office: MC 6222
Office Hours: Mon: 10am-11am, Wed:1pm-2pm, Wed:3:30pm-4:30pm
Textbook: Course Notes
Midterm: 
Quizes: Wednesdays: 5:30 - 6:20
```

|Week|Dates|Text Sections|Topics|Events|
|---|---|---|---|---|
1|Jan 6-10|1.2-1.4|Riemann Sums, De nite Integrals, Average Value||
2|Jan 13-17|1.5-1.7|FTC I, FTC II, Change of Variable|Quiz 1|
3|Jan 20-24*|2.1-2.3|Trig.  Sub., Integration By Parts, Partial Fractions|Quiz 2|
4|Jan 27-31|2.4, 3.1|Improper Integrals, Areas Between Curves|Quiz 3|
5|Feb 3-7|3.2, 3.3, 4.1, 4.5.1|Volumes, Intro to DEs, Direction Fields|Quiz 4|
MT|Feb 10-14**|4.2, 4.3, 4.5-4.8|Separable DEs, Linear DEs, Applications|Quiz 5|
RW|Feb 17-21||READING WEEK||
6|Feb 24-28|5.1-5.4|Intro to Series, Geo.  Series, Div.  Test|midterm|
7|Mar 2-6|5.5-5.7|Positive Series, Integral Test, Alternating Series|Quiz 6|
8|Mar 9-13|5.8-5.10|Types of Convergence, Ratio & Root Tests|Quiz 7|
9|Mar 16-20|6.1, 6.2, 6.3|Intro.  to Power Series, Functions, Differentiation|Quiz 8|
10|Mar 23-27|6.4, 6.5, 6.6, 6.7|Integration, Review of Taylor Polys., Taylor Series|Quiz 9|
FE|Mar 30-Apr 3|6.8, 6.9, 6.10|Convergence, Binomial Series, Applications|Quiz 10

# <p style="text-align: center;">6/1/20 </p>

## Riemann Sums and The Definite Integral (1.2)


**Math 138:** The area problem. That is how do we calculate the area under some function $f(x)$?
- We can approximate the area by rectangles. These approximations are called **Riemann Sums**

>**Definition - partition:** A **partition** P for the interval $[a,b]$ is a finite sequence of increasing numbers of the form
>$a = t_0 < t_1 < t_2 < \cdots < t_{n-1} < t_n = b$     
**Notes :** 
- This partition subdivides $[a,b]$ into n subintervals: $[t_0,t_1],[t_1,t_2],\cdots,[t_{n-1},t_n]$. The length of the $i^{th}$ subinterval $[t_{i-1},t_i]$ is $\Delta t_i = t_i - t_{i-1}$
- These subintervals do not need to have the same length
  
>**Definition - Regular *n*-partition:** Given an interval $[a,b]$ and $n \in \mathbb{N}$, the regular **n-partition** is the partition $P^{(n)}$ with
>$$a = t_0 < t_1 < t_2 < \cdots < t_{n-1} < t_n = b$$
>of $[a,b] where each subinterval ahs the same length $\Delta t_i = \frac{b-a}{n}$

>**Right-hand Riemann Sum:** The *right-hand Riemann sum* for $f$ with respect to the partition $P$ is the Riemann sum $R$ obtained from $P$ by choosing $c_i$ to be $t_i$, the right hand endpoint of $[t_{i-1},t_i]$. That is
>$$ R = \sum_{i=1}^nf(t_i)\Delta t_i.$$
>If $P^{(n)}$ is the Regular *n*-partition, we denote the right hand Riemann sum by: 
> $$R = \sum_{i=1}^nf(t_i)\Delta t_i = \sum_{i=1}^nf(t_i) \frac{b-a}{n} = \sum_{i=1}^nf(a+i(\frac{b-a}{n}) \frac{b-a}{n} $$

>**Lef-hand Riemann Sum:** The *left-hand Riemann sum* for $f$ with respect to the partition $P$ is the Riemann sum $R$ obtained from $P$ by choosing $c_i$ to be $t_i$, the left hand endpoint of $[t_{i-1},t_i]$. That is
>$$ R = \sum_{i=1}^nf(t_{i-1})\Delta t_i.$$
>If $P^{(n)}$ is the Regular *n*-partition, we denote the left hand Riemann sum by: 
> $$R = \sum_{i=1}^nf(t_{i-1})\Delta t_i = \sum_{i=1}^nf(t_{i-1}) \frac{b-a}{n} = \sum_{i=1}^nf(a+(i-1)(\frac{b-a}{n}) \frac{b-a}{n} $$



> The **norm of the partition** P is the length of widest subinterval: 
> $||P|| = max\{\Delta t_1, \Delta t_2, \cdots, \Delta t_n \}$.

>**Definition:** Given a bounded function $f$ on $[a,b]$, a partition P of $[a,b]$, and a set $\{c_1, c_2, \cdots, c_n \}$ where $c_i \in [t_{i-1},t_i]$, then a Riemann sum for $f$ with respect to $P$ is 
> $$ S = \sum_{i=i}^n f(c_i) \Delta t_i$$  

>**Definition:** We say $f$ is integrable on $[a,b]$ if there exists a unique $I \in \mathbb{R}$ such that whenever $\{P_n\}$ is a sequence of partitions with $lim_{n \rightarrow \infty}||P_n||=0$ and ${S_n}$ is any sequence of Riemann sums associated to the $P_n$'s, we have $lim_{n \rightarrow \infty} S_n = I$
>- In this case, we call $I$ the integral of $f$ over $[a,b]$ and denote it by 
>$$\int_a^b f(x)dx $$
**Note:**
- The $f(x)$ is the integrand   
- The $dx$ denotes the variable of integration   
- The $a,b$ denote limits of integration
the whole expression denotes the definite integral    

So, $\int_a^b f(x)dx = I = lim_{n \rightarrow \infty} S_n$.     
It represents the exact area under $f$ from $a$ to $b$ (signed - positive/negative)

**Question:** How do we know $I$ exists? How do we calculate $I$

  # <p style="text-align: center;">8/1/20 </p>

 **Some useful formulas:**
  1. $\sum_{i = 1}^ni = \frac{n(n+1)}{2}$
  2. $\sum_{i = 1}^ni^2 = \frac{n(n+1)(2n+1)}{6}$
  3. $\sum_{i = 1}^ni^3 = \frac{n(n+1)}{2}^2$

**Example:** Find $I = \int_0^4t+t^3dt$ using R.S   
*Solution:* $f(t)=t+t^3$ is continuous so $f$ is integrable, so all Reimann sums converge to the same value $I$.    
Let's choose a simple way to compute R.S: 
1. Choose a *regular*(uniform) subdivisions
$$ \Delta t_i = \Delta t = \frac{b-a}{n} = \frac{4-0}{n} = \frac{4}{n}$$
2. Pick $c_i$'s to be at the right ends of subintervals         
3. Solve:   
    Subinterval: $[t_{i-1},t_i] = c_i = t_i$      
    $t_i = a + i \cdot \Delta t = 0 + i \cdot \frac{4}{n} = \frac{4i}{n}$   
    Right-hand R.S.      
    $R_n = \sum_{i=1}^nf(a+ i \Delta t) \cdot \frac{b-a}{n}$    
    $I = lim_{n \rightarrow \infty} R_n$    
    $= lim_{n \rightarrow \infty} \sum_{i=1}^nf(\frac{4i}{n})\cdot \frac{4}{n}$    
    $= lim_{n \rightarrow \infty} \sum_{i=1}^n(\frac{4i}{n}+(\frac{4i}{n})^3)\frac{4}{n}$   
    $= lim_{n \rightarrow \infty} \sum_{i=1}^n(\frac{16i}{n^2}+\frac{256i^3}{n^4})$     
    $= lim_{n \rightarrow \infty} \frac{16}{n^2} \sum_{i=1}^ni+\frac{256}{n^4}\sum_{i=1}^ni^3$      
    $= lim_{n \rightarrow \infty} \frac{16}{n^2} \cdot \frac{n(n+1)}{2} +\frac{256}{n^4} \cdot \frac{n(n+1)}{2}^2$  

>### Properties of Definite Integrals:   
>**Theorem 2:** Assume $f$ and $g$ are integrable on $[a,b]$:    
>1. $\forall e \in \mathbb{R}. \int_a^bef(t)dt = e\int_a^bf(t)dt$
>2. $\int_a^b f(t) + g(t)dt = \int_a^b f(t)dt + \int_a^bg(t)dt$
>3. If $f$ is bounded between two values, $m \leq f(t) \leq M, \forall t \in [a,b]$, then 
>$$ m(b-a) \leq \int_a^bf(t)dt \leq M(b-a)$$
>4. If $f(t) \geq 0 \forall t \in [a,b]$ then $\int_a^bf(t)dt \geq 0$
>5. If $f(t) \geq g(t), \forall t \in [a,b]$ then $\int_a^bf(t)dt \geq \int_a^bg(t)dt$
>6. The function $|f|$ is integrable on $[a,b]$ and $|\int_a^bf(t)dt| \leq \int_a^b|f(t)|dt$

**More Properties:**
1. Define $\int_a^af(t)dt=0$
2. $\int_a^bf(t)dt = -\int_b^af(t)dt$
    - "Moving backwards is negative"

# <p style="text-align: center;">10/1/20 </p>
**Lecture 3:** Geometric interpretation (1.3), Average value of a function (1.4)

>**Theorem:** Integrals over subintervals
>If $f$ is integrable on an interval containing $a,b,c$, then 
>$$ \int_a^bf(x)dx = \int_a^cf(x)dx + \int_c^b f(x)dx$$
>Note: C does not need to be between a and b.
>$$\int_a^b f(x)dx = \int_a^cf(x)dx - \int_b^cf(x)dx = \int_a^cf(x)dx + \int_c^b f(x)dx

**Geometric interpretation of $\int_a^bf(x)dx$:**   
If $f(x) \geq 0$ on $[a,b]$, then $\int_a^bf(x)dx \geq 0$ and gives the area under $f$ and above the x-axis. If  $f(x) \leq 0$ on $[a,b]$, then $\int_a^bf(x)dx \leq 0$. So $\int_a^bf(x)dx$ gives the **signed**(positive/negative) area between $f$ and the x-axis. 

**Example 3.1:** Calculate $\int_0^4(x-3)dx$:   
*Solution 1:* Use the definition    
*Solution 2:* The function is linear so we find the area above the x-axis and subtract the area below the x-axis on the interval $[0,4]$.

### 1.4 Average value of a function
For $n$ real numbers $a_1,a_2, \cdots, a_n$ the average is $\frac{a_1+a_2+\cdots+a_n}{n}$. How do we extend this to a continuous function $f$ on $[a,b]$?   
We use a regular n-partition where the average is equal to $lim_{n \rightarrow \infty} \frac{\sum_{i = 1}^nf(t_i)}{n}$. This is the average of each value at a given partition where the number of partitions approaches infinity.    
Notice:     
$lim_{n \rightarrow \infty}(\frac{\sum_{i = 1}^nf(t_i)}{n}) = lim_{n \rightarrow \infty} \frac{1}{n} \sum_{i=1}^n f(t_i)$   
$=lim_{n \rightarrow \infty} \sum_{i=1}^n \frac{f(t_i)}{n} \cdot \frac{b-a}{b-a}$   
$=lim_{n \rightarrow \infty} \frac{1}{b-a} \sum_{i=1}^n f(t_i) \cdot \frac{b-a}{n}$   
$=\frac{1}{b-a} lim_{n \rightarrow \infty} \sum_{i=1}^n f(t_i) \cdot \frac{b-a}{n}$   
$= \frac{1}{b-a} \int_a^b f(x) dx$    

>**Definition:** If $f$ is continuous on $[a,b]$ then the average value of $f$ on $[a,b]$ is $f_{average} = \frac{1}{b-a} \int_a^b f(x)dx$. 

>**Theorem: Average Value Theorem (AVT)** If $f$ is continuous on $[a,b]$, then $\exists c \in [a,b]$ such that 
>$$ f(c) = \frac{1}{b-a} \int_a^bf(x)dx$$
- The point $c$ is such that if a rectangle was drawn with points $a,b,f(c)$ where $f(c)$ represents the height, the area of this rectangle is equal to the signed area under $f$ on $[a,b]$. Convince yourself as to why this is expected. 

**Proof of AVT:** Assume $f$ is continuous on $[a,b]$.   
By Extreme Value Theorem, $\exists m,M \in \mathbb{R}$ such that $m \leq f(x) \leq M$ for all $x\in [a,b]$. Also $\exists c_1,c_2 \in [a,b]$ such that $f(c_1) = m$ and $f(c_2)=M$.    
Since $m \leq f(x) \leq M$ by proposition 3 of integrals $m(b-a) \leq \int_a^bf(x)dx \leq M(b-a)$.  
So $m \leq \frac{1}{b-a} \cdot \int_a^bf(x)dx \leq M$,  
or $f(c_1) \leq \frac{1}{b-a} \cdot \int_a^bf(x)dx \leq f(c_2)$.    
Now by Intermediate Value Theoerem there exists some $c$ between $c_1$ and $c_2$ such that $f(c) = \frac{1}{b-a} \cdot \int_a^bf(x)dx$.    
QED


# <p style="text-align: center;">13/1/20 </p>
**Lecture 4:** Fundamental Theorem of Calculus (FTC)

>**Definition:** Suppose $f$ is continuous on $[a,b]$. Define the **integral function:**
>$$G(x) = \int_a^x f(t) dt$$
>$G(x)$ is a function that returns the net (*signed*) area under $f$ from $a$ to $x$. 

>**Theorem - The fundamental theorem of calculus part 1 (FTC 1):** If $f$ is continuous on an open interval $I$ containing a point $x=a$, and if $G(x) = \int_a^xf(t)dt$, then $G(x)$ is differentiable at each $x \in I$ and $G'(x)=f(x)$. That is $\frac{d}{dx} \int_a^x f(t)dt = f(x)$.  

**Proof:** Assume $f$ is continuous on $I$ and $G(x) = \int_a^xf(t)dt$.     
Consider arbitrary $x_0 \in I$.     
We will show $G(x)$ is differentiable at $x$. and $G'(x_0) = f(x_0)$ by showing, 
$$lim_{x \rightarrow x_0} \frac{G(x)-G(x_0)}{x-x_0} = f(x_0)$$    
*First notice:*   
$$
\begin{array}{rcl} 
\frac{G(x)-G(x_0)}{x-x_0}  &=& \frac{\int_a^x f(t)dt - \int_a^{x_0} f(t) dt}{x-x_0}    \\
&=&\frac{(\int_a^{x_0} f(t)dt + \int_{x_0}^x f(t)dt) - \int_a^{x_0} f(t) dt}{x-x_0} \\ 
&=& \frac{1}{x-x_0} \int_a^{x_0} f(t) dt \end{array}
$$

Let $\epsilon > 0$. Since $f$ is continuous at $x_0$ so $\exists \delta > 0$ such that if $0<|x-x_0|<\delta$ then $|f(x)-f(x_0)| < \delta$    
Suppose $0<|x-x_0|<\delta$    
By AVT, there xists some $c$ between $x$ and $x_0$ such that $f(c) = \frac{1}{x-x_0} \int_{x_0}^xf(t)dt$    
Since $c$ is between $x$ and $x_0$, we have $0<|c-x_0|<\delta$ as well.     
Therefore, $|f(c)-f(x_0)| < \epsilon$.    
That is, $|\frac{G(x)-G(x_0)}{x-x_0} - f(x_0)| < \epsilon$    
So, we have shown that for any $\epsilon > 0$, $\exists \delta > 0$ such that if $0 < |x-x_0|<\delta$ then $|\frac{G(x)-G(x_0)}{x-x_0} - f(x_0)| < \epsilon$    
By the definition of a limit, we've shown $lim_{x \rightarrow x_0} \frac{G(x)-G(x_0)}{x-x_0} = f(x_0)$    
That is, $G'(x_0) = f(x_0)$ (by the definition of derivative)   

**Example 4.1:** $G(x) = \int_{-2}^x(e^t-1)dt$, determine $G'(x)$:      
Since $e^{t^3}-1$ is continuous, by FTC 1, 
$$G'(x)=\frac{d}{dx} \int_{-2}^x(e^{t^3}-1)dt = e^{x^3} -1$$

**Example 4.2:** Determine $\frac{d}{dx} \int_{-2}^{x^2}(e^{t^3} - 1)dt$    
Since $G(x) = \int_{-2}^{x^2}(e^{t^3} - 1)dt$   
So 
$$\begin{array}{rcl} \frac{d}{dx} \int_{-2}^{x^2}(e^{t^3} - 1)dt  &=& \frac{d}{dx} G(x^2) \\
&=& G'(x^2) \cdot 2x \\ 
&=& (e^{({x^2})^3}-1)\cdot 2x \\
&=& 2x \cdot (e^{x^6}-1)\cdot 2x
\end{array} $$


# <p style="text-align: center;">15/1/20 </p>
**Lecture 5**: Antiderivatives FTCII(1.6)

>**Definition:** Given a function $f_1$, an antiderivative of $f$ is a function $F$ such that 
>$$ F'(x) = f(x) $$
- Example: for $f(x)=x$, $F(x) = \frac{x^2}{2}$

>**Definition:** The collection of all antiderivatives of $f(x)$ is denoted by $\int f(x) dx$. This is called the **indefinite integral** of $f$

By the antiderivative theorem, any two antiderivatives of $f$ differ by a constant. Therefore, $\int f(x) dx = F(x) + c$, where $c \in \mathbb{R}$ and $F$ is any antiderivative of $f$ ($F'(x)=f(x)$)

The indefinite integral, $\int f(x)dx$, is a family of functions, it represents all functions whose derivative is $f(x)$, The definite integral,$\int_a^bf(x)dx$, is a number defined as a limit of Riemann sums. It represents the **signed** area under $f(x)$ from $x=a$ to $x=b$. 

You should know all of the following indefinite integrals: **ADD FROM PAGE 43**

>**Theorem (FTCII):** The Fundemental Theorem of Calculus part II (FTCII) 
>If  $f$ is continuous on $[a,b]$ and $F$ is any antiderivative of $f$, then 
>$$ \int_a^bf(x)dx = F(b) - F(a) = F(x)|_a^b  $$
- Note that $F(x)_a^b$ means $F(b) - F(a)$

**Example 5.1:** Calculate $\int_0^3(x^3+2x)dx$
$$\begin{array}{rcl} \int_0^3(x^3+2x)dx &=& \frac{x^4}{4} + x^2 + c |_1^3, c = 0 \\
&=& \frac{81}{4} + 9 \\
&=& \frac{117}{4}\end{array}$$

**Proof of FTCII:**   
Suppose $f$ is continuous on $[a,b]$. Consider $G(x) = \int_0^xf(t)dt$    
By FTCI, $G'(x) = f(x)$. That is, G(x) is an antiderivative of $f(x)$.    
Consider any antiderivative $F(x)$ of $f(x)$.     
By the antiderivative theorem, 
$F(x) = G(x) + c$, where $c\in\mathbb{R}$   
So, 
$$\begin{array}{rcl} F(b) - F(a) &=& (G(b) + c) - (G(a) + c) \\ &=&  G(b) - G(a)  \\ &=&  \int_a^bf(t)dt - \int_a^af(t)dt \\ &=& \int_a^bf(t)dt\end{array}$$ 
As required. 

**Example 5.2:** Calculate $\int_2^4 \frac{2x+2}{x}dx$    
$$\begin{array}{rcl} \int_2^4 2 + \frac{1}{x}dx 
&=& (2x + ln|x|)|_2^4 \\
&=& (8 + ln4) - (4 + ln2) \\
&=& 4 + ln2 \end{array}$$
**Note:** We can use any antiderivative 
$$\begin{array}{rcl} \int_2^4 2 + \frac{1}{x}dx 
&=& (2x + ln|x| + C)|_2^4 \\
&=& (8 + ln4 + C) - (4 + ln2 + C) \\
&=& 4 + ln2 \end{array}$$

**Example 5.4:** $\int_0^{2 \pi}|cosx|dx$   
$$\begin{array}{rcl} \int_0^{2 \pi}|cosx|dx &=&4\int_0^{2 \pi} cosx dx \\
&=& 4(sinx)|_0^{\frac{\pi}{2}} \\
&=& 4 (sin\frac{\pi}{2} - sin0) \\
&=& 4 \end{array}$$
- Consider the graph of $|cosx|$, a geometric understanding of $cos$ shows that the first "hill" of area is equal to a quarter of one period's area  
  
**OR**    
$$\int_0^{2 \pi}|cosx|dx = \int_0^{\frac{\pi}{2}}cosxdx + \int_{\frac{\pi}{2}}^{\frac{3\pi}{2}}-cosxdx  + \int_{\frac{3\pi}{2}}^{2 \pi}cosxdx$$


>**Corollary:** Extended version of FTCI.    
>If $f$ is continuous and $g$ and $g$ are differentiable, then, 
>$$ \frac{d}{dx}[\int_{g(x)}^{h(x)}f(t)dt] - f(h(x))h'(x) - f(g(x)g'(x)$$    
**Proof 1:** Use FTCII    
**Proof 2:** Use splitting over subintervals, then, 
$$ \int_{g(x)}^{h(x)}f(t)dt = \int_{g(x)}^{c}f(t)dt + \int_{c}^{h(x)}f(t)dt$$

**Example 5.5:**
# <p style="text-align: center;">17/1/20 </p>
**Lecture 6:** Change of Variable (1.7)

>**Theorem:** If $u=g(x)$ is differentiable and $f$ is continuous on the range of $g$, then 
>$$\int f(g(x))g'(x)dx = \int f(u)du $$
- We're reversing the chain rule

**Example 6.1:** $\int \frac{x^3}{(x+5)^2}dx$   
**Step 1:** Choose a substitution let $u = g(x) = x + 5$ then $g'(x) = 1$       

**Step 2:** Replace original variable w with new variable 

$$\begin{array}{rcl} \int \frac{x^3}{(x+5)^2}dx  &=& \int \frac{(u-5)^3}{u^2}du  \\
&=& \int \frac{u^3-15u^2+75^u-125}{u^2}du \\
&=& \int (u - 15 - \frac{75}{u} - \frac{125}{u^2} - \frac{125}{u^2})du \\
&=& u^2 - 15u + 75ln|u| + \frac{125}{u} + C
\end{array}$$

**Proof of:** $\int f(g(x))g'(x)dx = \int f(u)du$   
Since f is continuous on the range of $g$, by FTC1, there is a function $f$ such that $F' = f$ (that is, $f$ has an antiderivative).
$$\frac{d}{dx} (F(g(x))) = F'(g(x))g'(x) = f(g(x))g'(x)$$   
So $F(g(x))$ is an antiderivative of $f(g(x))g'(x)$.    
$$\int f(g(x))g'(x)dx = F(g(x)) + C = F(u) + C = \int f(u)du$$

**Notation trick:** If $u=g(x)$ then $du = g'(x)dx$   

**Example 6.2:** $\int \frac{(lnx)^2}{x}dx$   
**Tip:** A good choice for $u$ is often $u$ = function in the integrand whose derivative is also in the integrand.      
Choose $u =lnx \Rightarrow \frac{du}{dx} = \frac{1}{x} \Rightarrow du = \frac{1}{x}dx$
$$\int \frac{(lnx)^2}{x}dx = \int u^2 du = \frac{u^3}{3} + C = \frac{(lnx)^3}{3} + C$$

**Example 6.3:** $\int \sqrt{1 + \sqrt{x}}dx$   
**Tip:** Good choice for $u$ is often $u$ = a function whose inside another function    
Choose $u=\sqrt{x}$   
$du = \frac{1}{2\sqrt{x}}dx$ so $dx = 2 \sqrt{x} du = 2udu$   
$\int \sqrt{1 + \sqrt{x}}dx =  \int \sqrt{1 + u}2udu = 2 \int \sqrt{1 + u}udu$

Let $t = 1 + u$, $dt = du$
$$\begin{array}{rcl} 2 \int (t-1)\sqrt{t}dt &=& 2\int{t^\frac{3}{2}} - t^\frac{1}{2} \\
&=& 2 \cdot (\frac{2}{5} t^\frac{5}{2} - \frac{2}{3}t^\frac{3}{2}) + C \\
&=& \frac{4}{5}(1 + \sqrt{x})^\frac{5}{2} - \frac{2}{3}(1 + \sqrt{x})^\frac{3}{2} + C
\end{array}$$

**Example 6.4:** $\int tanx dx$     
$u = cosx \Rightarrow du = sinxdx$    
$\int tanxdx = \int \frac{sinx}{cosx}dx = - \int \frac{1}{u} du = - ln|u| + C$

>Theorem: If $g'(x)$ is continuous on [a,b] and $f$ is continuous on the range of $g$, then 
>$$ \int f(g(x)dx) = \int_{u = g(a)}^{u = g(b)}f(u)du$$
- Proven in course notes on pages 52-53

**Example 6.5:** $\int_1^2 \frac{e^\frac{1}{x}}{x^2}dx$     
Let $u = \frac{1}{x}$ $du=\frac{-1}{x^2}dx$   
$x = 1 \Rightarrow u = 1$   
$x = 2 \Rightarrow u = \frac{1}{2}$     
$\int_1^2 \frac{e^\frac{1}{x}}{x^2}dx = -\int_1^{\frac{1}{2}} e^u du = \int_{\frac{1}{2}}^1 e^u du = e^u|_{\frac{1}{2}}^1 = e - e^{\frac{1}{2}}$

**Example 6.6:** $\int_{\frac{\pi}{2}}^{\pi}sin^2xcos^3xdx$   
$= \int_{\frac{\pi}{2}}^{\pi} sin^2xcos^2xcosxdx$   
$= \int_{\frac{\pi}{2}}^{\pi} sin^2x(1-sin^2x)cosxdx$   
Let $u = sinx$, $du = cosxdx$   
$= \int_{x= \frac{\pi}{2}}^{z =\pi} u^2(1-u^2)$   
$= \frac{u^3}{3} - \frac{u^5}{5} |_{x = \frac{\pi}{2}}^{x = \pi}$       
$= \frac{sin^3x}{3} - \frac{sin^5x}{5} |_{\frac{\pi}{2}}^{\pi}$

# <p style="text-align: center;">5/2/20 </p>
**Lec 14:** Volumes Continued (3.2 & 3.3)   
**Example 4.1**: Determine the volume of the solid obtained by rotating the region bounded by $x = 5 - y^2$ and $x=0$ about the y-axis

``` 
sketch 
"sideways parabola opening to the left rotating about the the y axis"
```
- Note that we would need to use horizontal rectangles with this shape (integrating with respect to y)
  - you could also do with respect to x using the shell method

Use horizontal rectangles of width $\Delta y$   
From $y = -\sqrt{5}$ to $y = \sqrt{5}$ will get disks and the cross-sectional area of solid is  $\pi (5 - y^2)^2$   

Therefore, 
$$ \begin{array}{rcl} v &=& \int_{-\sqrt{5}}^{\sqrt{5}} \pi (5 - y^2)^2 dy \\
&=& \cdots \\
&=& \frac{80\sqrt{5}}{3}\pi \end{array}$$ 

**Summary**: we get disks/washers when we rotate
- functions of $x$ about horizontal lines (Ex: 13.2,13.3)
  - use vertical rectangles (integrate with respect to x)
- functions of $y$  about vertical lines (Ex: 14.1)
  - Use horizontal rectangles (integrate with respect to y)

**Exercise**: Rotate region in Ex 14.1 about $x=6$

**Exercise**: Find the volume of the cap heigh with h, of a sphere of radius r. 
- (cap is the top semi-sphere where h is the height from the top of the sphere to the base of the semi-sphere)

### **Example 14.2**: Determine the volume of the solid obtained by rotating the region bounded by $y = (x-1)(x-3)^2$, the x-axis, $x=1$ and $x=3$, about the y-axis

``` 
Sketch "from 1 to 3 it looks like a small hill going up from 1 and down to 3"
```
- if we use horizontal rectangles we'll get washers, but to find the length of each rectangle would need to be determined using the inverse of the function (x values with respect to y), this is difficult for the given function
  
Instead we use vertical rectangles of width $\Delta x$ and length $(x-1)(x-3)^2$.       
Rotate this rectangle around the y-axis. We will get a **cylindrical shell** (an infinitesimally thin hollow cylinder, its volume is equal to its surface area)
- What is the volume of one shell? "cut and flatten"
  - Width: $\Delta x$
  - Height: $f(x) = (x-1)(x-3)^2$
  - Length: $2\pi r = 2\pi x$

So volume $=2\pi xf(x)^2 \Delta x= 2\pi x(x-1)(x-3)^2 \Delta x$     
Therefore total volume is 
$$ \begin{array}{rcl} V &=& \int_1^3 2 \pi x (x-1)(x-3)^2 dx \\ 
&=& \cdots \\ 
&=& \frac{24 \pi}{5} \end{array} $$

### **Example 14.3:** Find the volume of solid obtained by rotating the region bounded by $x=y^2$, $x+y=2$ about $y=-3$
```
Sketch "parabola opening outward with the line crossing it diagonally from top left to bottom right
```
- Intersection points: $(1,1)$, $(4,-2)$

Let's use horizontal rectangles (since $x=f(y)$) of width $\Delta y$. Rotate one such rectangle about $y=-3$. Cut & flatten: 
- width: $\Delta y$
- Length: $(2-y) - y^2 = 2 - y - y^2$
- Height: $2\pi r = 2 \pi (y - (-3)) = 2 \pi (y +3)$

So, 
$$\begin{array}{rcl} V &=& \int_{-2}^{1} 2 \pi (y + 3)(2 - y - y^2)dy \\ 
&=& \cdots \\ 
&=& \frac{45\pi}{2}\end{array}$$
# <p style="text-align: center;">6/1/20 </p>