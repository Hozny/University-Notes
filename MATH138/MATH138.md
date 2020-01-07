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

# <p style="text-align: center;">6/1/14 </p>

## Riemann Sums and The Definite Integral (1.2)


**Math 138:** The area problem. That is how do we calculate the area under some function $f(x)$?
- We can approximate the area by rectangles. These approximations are called **Riemann Sums**

>**Definition:** A partition P for the interval $[a,b]$ is a finite sequence of increasing numbers of the form
>$a = t_0 < t_1 < t_2 < \cdots < t_{n-1} < t_n = b$         

**Notes :** 
- This partition subdivides $[a,b]$ into n subintervals: $[t_0,t_1],[t_1,t_2],\cdots,[t_{n-1},t_n]$. The length of the $i^{th}$ subinterval $[t_{i-1},t_i]$ is $\Delta t_i = t_i - t_{i-1}$
- These subintervals do not need to have the same length

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


  