# MATH 136
Calculus 2
``` 
Instructor: Jen Nelson
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

# <p style="text-align: center;">6/1/20 </p>