Measure Integration Real Analysis - Supplement <br>
Real Analysis Review
================
Rosie Sun <br>
2026-09-02


# A Complete Ordered Fields

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




# C Supremum and Infimum

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




# D Open and Closed Subsets of $R^n$

### 0.46 Definition: limit
Suppose $a_1, a_2, ... \in R^n$ and $L \in R^n$. Then $L$ is called a limit of the sequence $a_1, a_2, ...$ and we write 

$$lim_{k \rightarrow \inf} a_k = L$$

if for every $\epsilon > 0$, there exists $m \in Z^+$ such that 

$$\lvert a_k - L \rvert_inf < \epsilon$$

for all integers $k \geq m$.


### 0.47 Definition: converge; convergent
A sequence in $R^n$ is said to converge and to be a convergent sequence if it has a limit.


### 0.49 Definition: open cube
For $x \in R^n$ and $\delta > 0$, the open cube $B(x, \delta)$ is defined by

$$B(x, \delta) = \\{y \in R^n: \lvert y - x \rvert_\inf < \delta \\} .$$


### 0.52 Definition: open subsets of $R^n$
- A subset $G$ of $R^n$ is called open if for every $x \in G$, there exists $\delta > 0$ such that $B(x, \delta) \subseteq G$.

- Equivalently, a subset $G$ of $R^n$ is called open if every element of $G$ is contained in an open cube that is contained in $G$.


### 0.62 characterization of closed sets
A subset of $R^n$ is closed if and only if it contains the limit of every convergent sequence of elements of the set.

Proof:

We will prove the contrapositive in both directions.

$\Leftarrow$
First suppose $A$ is a subset of $R^n$ such that some convergent sequence $a_1, a_2, ...$ of elements of $A$ has a limit $L$ that is not in $A$. 

Because $lim_{k \rightarrow \inf} a_k = L$, for each $\delta > 0$ there exists $k \in Z^+$ such that 

$$\lvert L - a_k \rvert_\inf < \delta .$$ 

Thus $L \in R^n \ A$ and 

$$B(L, \delta) \notsubseteq R^n \ A$$

for every $\delta > 0$.

Hence $R^n \ A$ is not an open subset of $R^n$. Thus $A$ is not a closed subset of $R^n$, completing the proof in one direction.

$\Rightarrow$
Now suppose $A$ is a subset of $R^n$ that is not closed.

Thus $R^n \ A$ is not open. Hence there exists $L \in R^n \ A$ such that 

$$B(L, \frac{1}{k}) \notsubseteq R^n \ A$$

for every $k \in Z^+$. 

Thus for each $k \in Z^+$, there exists $a_k \in A$ such that 

$$\lvert L - a_k \rvert_\inf < \frac{1}{k} .$$

The inequality above implies that the sequence $a_1, a_2, ...$ of elements of $A$ has limit $L$. Thus there exists a convergent sequence of elements of $A$ whose limit is not in $A$, completing the proof in the other direction.


### 0.65 sets that are both open and closed
The only subsets of $R^n$ that are both open and closed are $\emptyset$ and $R^n$.

Proof:

Suppose $A$ is a subset of $R^n$ that is both open and closed. 

Suppose towards contradiction that $A \neq \emptyset$ and $A \neq R^n$. Thus there exist $a \in A$ and $b \in R^n \ A$. Let

$$T = \\{t \in [0, 1]: (1 - t) a + tb \in A \\}$$

and let

$$s = sup T.$$

The set $T$ is nonempty because $0 \in T$; thus $s \in [0, 1]$. Let 

$$c = (1 - s) a + sb.$$

Suppose $c \in A$. Then $s \neq 1$ (because otherwise $c = b \notin A$). Because $s \in T$ and $A$ is open, $T$ contains numbers slightly larger than $s$, which contradicts the definition of $s$ as an upper bound of $T$.

Suppose $c \in R^n \ A$. Then $s \neq 0$ (because otherwise $c = a \in A$). Because $s \notin T$ and $R^n \ A$ is open, $T$ contains no numbers slightly less than $s$, which contradicts the definition of $s$ as the least upper bound of $T$.

Thus we arrive at a contradiction whether $c \in A$ or $c \in R^n \ A$, completing the proof. 




# E Sequences and Continuity

### 0.68 Definition: bounded
- A set $A \subseteq R^n$ is called bounded if $sup \\{\lvert a \rvert_\inf : a \in A \\} < \inf$.

- A function into $R^n$ is called bounded if its range is a bounded subset of $R^n$.

- As a special case of the previous bullet point, a sequence $a_1, a_2, ...$ of elements of $R^n$ is called bounded if $sup \\{\lvert a_k \rvert_\inf : k \in Z^+ \\} < \inf$.


### 0.74 characterization of closed bounded sets
Suppose $F$ is a closed bounded subset of $R^n$. Then every sequence of elements of $F$ has a subsequence that converges to an element of $F$.

Proof:

Consider a sequence of elements of $F$. Because $F$ is a bounded set, this sequence is bounded and thus has a convergent subsequence (by the Bolzano-Weierstrass Theorem 0.73). Because $F$ is closed, the limit of this convergent subsequence is in $F$ (by 0.62).


### 0.75


### 0.77


### 0.79 continuity implies uniform continuity on closed bounded sets
Every continuous $R^n$-valued function on each closed bounded subset of $R^m$ is uniformly continuous.

Proof:

Suppose $F$ is a closed bounded subset of $R^m$ and $g: F \rightarrow R^n$ is continuous. We want to show that $g$ is uniformly continuous.

Suppose $g$ is not uniformly continuous. Then there exists $\epsilon > 0$ such that for each $k \in Z^+$, there exist $a_k, b_k \in F$ with 

$$\lvert a_k - b_k \rvert_\inf < \farc{1}{k}$$

and

$$\lvert g(a_k) - g(b_k) \rvert_\inf \geq \epsilon.$$

Because $F$ is bounded, the sequence $a_1, a_2, ...$ is bounded. Thus by the Bolzano-Weierstrass Theorem (0.73), some subsequence $a_{k_1}, a_{k_2}, ...$ converges to some limit $a$. Because $F$ is closed, we have $a \in F$ by 0.62.

Now

$$
\begin{aligned}
\lvert a - b_{k_j} \rvert_\inf 
    &= \lvert (a - a_{k_j}) + (a_{k_j} - b_{k_j}) \rvert_\inf \\
    &\leq \lvert a - a_{k_j} \rvert_\inf + \lvert a_{k_j} - b_{k_j} \rvert_\inf \\
    &< \lvert a - a_{k_j} \rvert_\inf + \frac{1}{k_j}
\end{aligned}
$$

which implies that $lim_{j \rightarrow \inf} b_{k_j} = a$.

Because $g$ is continuous at $a$ and $lim_{j \rightarrow \inf} a_{k_j} = a$ and $lim_{j \rightarrow \inf} b_{k_j} = a$, we conclude that

$$lim_{j \rightarrow \inf} g(a_{k_j}) = g(a)$$

and

$$lim_{j \rightarrow \inf} g(b_{k_j}) = g(a) .$$

Thus 

$$lim_{j \rightarrow \inf} (g(a_{k_j}) - g(b_{k_j})) = 0. $$

The equation above contradicts the inequality $\lvert g(a_k) - g(b_k) \rvert_\inf \geq \epsilon$, which holds for all $k \in Z^+$. This contradiction means that our assumption that $g$ is not uniformly continuous is false, completing the proof.
