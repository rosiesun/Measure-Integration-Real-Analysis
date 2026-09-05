Measure Integration Real Analysis - Supplement <br>
Real Analysis Review
================
Rosie Sun <br>
2026-09-02


# Section A Complete Ordered Fields

### 0.12 no rational number has a square equal to 2
There does not exist a rational number whose square is 2.

Proof:

Suppose there exist integers $m$ and $n$ such that 

$$(\frac{m}{n})^2 = 2 .$$

By canceling common factors, we can choose $m$ and $n$ to have no common integer factors greater than 1. In other words, we can assume that $\frac{m}{n}$ is a fraction in reduced form.

The equation above is equivalent to the equation 

$$m^2 = 2n^2 .$$

Thus $m^2$ is even. Hence $m$ is even. Thus $m = 2k$ for some integer $k$. Substituting $2k$ for $m$ in the equation above gives 

$$4k^2 = 2n^2,$$

or equivalently 

$$2k^2 = n^2 .$$

Thus $n^2$ is even. Hence $n$ is even.

We have now shown that both $m$ and $n$ are even, contradicting our choice of $m$ and $n$ as having no common integer factors greater than 1.

This contradiction means our original assumption that there is a rational number whose square equals 2 was incorrect, completing the proof.


### 0.18 Example $\\{a \in Q: a^2 < 2\\}$ does not have a least upper bound in Q
Suppose $b \in Q$. We want to show that $b$ is not a least upper bound of $A = \\{a \in Q: a^2 < 2\\}$. 

We know from 0.12 that $b^2 \neq 2$. Thus $b^2 < 2$ or $b^2 > 2$.

First consider the case where $b^2 < 2$. If we can find a positive rational number $\delta$ such that $(b + \delta)^2 < 2$, then $b$ is not an upper bound of $A$. Take

$$\delta = \frac{2 - b^2}{5} .$$

Because $b < 2$ and $0 < \delta < 1$, we have $2b + \delta < 5$ and

$$
\begin{aligned}
(b + \delta)^2 
    &= b^2 + \delta^2 + 2b \delta \\
    &= b^2 + (2b + \delta) \delta \\
    &< b^2 + 5 \delta
    &= 2
\end{aligned}
$$

Thus $b$ is not an upper bound of $A$.

Now consider the case where $b > 0$ and $b^2 > 2$. If we can find a rational number $\delta$ such that $0 < \delta < b$ and $(b - \delta)^2 > 2$, then $b - \delta$ is an upper bound of $A$, which implies that $b$ is not a least upper bound of $A$. Take

$$\delta = \frac{b^2 - 2}{2b} .$$

Then $0 < \delta < b$ and 

$$
\begin{aligned}
(b - \delta)^2 
    &= b^2 - 2b \delta + \delta^2 \\
    &> b^2 - 2b \delta \\
    &= 2
\end{aligned}
$$

Thus $b$ is not a least upper bound of $A$. 

This completes the explanation of why $\\{a \in Q: a^2 < 2\\}$ does not have a least upper bound in $Q$.


### 0.19 Definition: complete ordered field
An ordered field $F$ is called complete if every nonempty subset of $F$ that has an upper bound has a least upper bound.




# Section C

### 0.28 Archimedean property
Suppose $t \in R$. Then there is a positive integer $n$ such that $t < n$.


### 0.29 Archimediean property
Suppose $\epsilon \in R$ and $\epsilon > 0$. Then there is a positive integer $n$ such that $\frac{1}{n} < \epsilon$. 


### 0.30 rational number between every two distinct real numbers
Suppose $a, b \in R$, with $a < b$. Then there exists a rational number $c$ such that $a < c < b$.

Proof:

First suppose $a \geq 0$. By the Archimedean property (0.29), there is a positive integer $n$ such that 

$$\frac{1}{n} < b - a .$$

Let 

$$A = \\{m \in Z: a < \frac{m}{n} \\} .$$

By the Archimedean property (0.28), there is a positive integer $m$ such that $an < m$. Thus $A$ is a nonempty set of positive integers. Hence $A$ has a smallest, which we will call $M$. Because $M \in A$, we have $a < \frac{M}{n}$.

Now $M - 1 \notin A$ (because $M$ is the smallest element of $A$). Thus 

$$\frac{M-1}{n} \leq a, $$

which implies that 

$$\frac{M}{n} \leq a + \frac{1}{n} < b .$$

Hence taking $c = \frac{M}{n}$ completes the proof in the case where $a \geq 0$.

Now suppose $a < 0$. If $b > 0$, then take $c = 0$. If $b \leq 0$, then apply the previous case to find a rational number $d$ such that $-b < d < -a$, then take $c = -d$.




# Section D

### 0.46 Definition: limit





# Section E