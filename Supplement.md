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

$$\left( \frac{m}{n} \right)^2 = 2 .$$

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


### 0.18 Example $\\{a \in \mathbb{Q}: a^2 < 2\\}$ does not have a least upper bound in \mathbb{Q}
Suppose $b \in \mathbb{Q}$. We want to show that $b$ is not a least upper bound of $A = \\{a \in \mathbb{Q}: a^2 < 2\\}$. 

We know from 0.12 that $b^2 \neq 2$. Thus $b^2 < 2$ or $b^2 > 2$.

First consider the case where $b^2 < 2$. If we can find a positive rational number $\delta$ such that $(b + \delta)^2 < 2$, then $b$ is not an upper bound of $A$. Take

$$\delta = \frac{2 - b^2}{5} .$$

Because $b < 2$ and $0 < \delta < 1$, we have $2b + \delta < 5$ and

$$
\begin{aligned}
(b + \delta)^2 
    &= b^2 + \delta^2 + 2b \delta \\
    &= b^2 + (2b + \delta) \delta \\
    &< b^2 + 5 \delta \\
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

This completes the explanation of why $\\{a \in \mathbb{Q}: a^2 < 2\\}$ does not have a least upper bound in $\mathbb{Q}$.


### 0.19 Definition: complete ordered field
An ordered field $F$ is called complete if every nonempty subset of $F$ that has an upper bound has a least upper bound.




# C Supremum and Infimum

### 0.28 Archimedean property
Suppose $t \in \mathbb{R}$. Then there is a positive integer $n$ such that $t < n$.


### 0.29 Archimediean property
Suppose $\epsilon \in \mathbb{R}$ and $\epsilon > 0$. Then there is a positive integer $n$ such that $\frac{1}{n} < \epsilon$. 


### 0.30 rational number between every two distinct real numbers
Suppose $a, b \in \mathbb{R}$, with $a < b$. Then there exists a rational number $c$ such that $a < c < b$.

Proof:

First suppose $a \geq 0$. By the Archimedean property (0.29), there is a positive integer $n$ such that 

$$\frac{1}{n} < b - a .$$

Let 

$$A = \left\\{m \in \mathbb{Z}: a < \frac{m}{n} \right\\} .$$

By the Archimedean property (0.28), there is a positive integer $m$ such that $an < m$. Thus $A$ is a nonempty set of positive integers. Hence $A$ has a smallest, which we will call $M$. Because $M \in A$, we have $a < \frac{M}{n}$.

Now $M - 1 \notin A$ (because $M$ is the smallest element of $A$). Thus 

$$\frac{M-1}{n} \leq a, $$

which implies that 

$$\frac{M}{n} \leq a + \frac{1}{n} < b .$$

Hence taking $c = \frac{M}{n}$ completes the proof in the case where $a \geq 0$.

Now suppose $a < 0$. If $b > 0$, then take $c = 0$. If $b \leq 0$, then apply the previous case to find a rational number $d$ such that $-b < d < -a$, then take $c = -d$.




# D Open and Closed Subsets of $\mathbb{R}^n$

### 0.46 Definition: limit
Suppose $a_1, a_2, ... \in \mathbb{R}^n$ and $L \in \mathbb{R}^n$. Then $L$ is called a limit of the sequence $a_1, a_2, ...$ and we write 

$$\lim_{k \to \infty} a_k = L$$

if for every $\epsilon > 0$, there exists $m \in \mathbb{Z}^+$ such that 

$$\lvert a_k - L \rvert_\infty < \epsilon$$

for all integers $k \geq m$.


### 0.47 Definition: converge; convergent
A sequence in $\mathbb{R}^n$ is said to converge and to be a convergent sequence if it has a limit.


### 0.49 Definition: open cube
For $x \in \mathbb{R}^n$ and $\delta > 0$, the open cube $B(x, \delta)$ is defined by

$$B(x, \delta) = \\{y \in \mathbb{R}^n: \lvert y - x \rvert_\infty < \delta \\} .$$


### 0.52 Definition: open subsets of $\mathbb{R}^n$
- A subset $G$ of $\mathbb{R}^n$ is called open if for every $x \in G$, there exists $\delta > 0$ such that $B(x, \delta) \subseteq G$.

- Equivalently, a subset $G$ of $\mathbb{R}^n$ is called open if every element of $G$ is contained in an open cube that is contained in $G$.


### 0.62 characterization of closed sets
A subset of $\mathbb{R}^n$ is closed if and only if it contains the limit of every convergent sequence of elements of the set.

Proof:

We will prove the contrapositive in both directions.

$\Leftarrow$
First suppose $A$ is a subset of $\mathbb{R}^n$ such that some convergent sequence $a_1, a_2, ...$ of elements of $A$ has a limit $L$ that is not in $A$. 

Because $\lim_{k \to \inf} a_k = L$, for each $\delta > 0$ there exists $k \in \mathbb{Z}^+$ such that 

$$\lvert L - a_k \rvert_\infty < \delta .$$ 

Thus $L \in \mathbb{R}^n \ A$ and 

$$B(L, \delta) \nsubseteq \mathbb{R}^n \ A$$

for every $\delta > 0$.

Hence $\mathbb{R}^n \ A$ is not an open subset of $\mathbb{R}^n$. Thus $A$ is not a closed subset of $\mathbb{R}^n$, completing the proof in one direction.

$\Rightarrow$
Now suppose $A$ is a subset of $\mathbb{R}^n$ that is not closed.

Thus $\mathbb{R}^n \ A$ is not open. Hence there exists $L \in \mathbb{R}^n \ A$ such that 

$$B(L, \frac{1}{k}) \nsubseteq \mathbb{R}^n \ A$$

for every $k \in \mathbb{Z}^+$. 

Thus for each $k \in \mathbb{Z}^+$, there exists $a_k \in A$ such that 

$$\lvert L - a_k \rvert_\infty < \frac{1}{k} .$$

The inequality above implies that the sequence $a_1, a_2, ...$ of elements of $A$ has limit $L$. Thus there exists a convergent sequence of elements of $A$ whose limit is not in $A$, completing the proof in the other direction.


### 0.63 De Morgan's Laws
Suppose $\mathcal{A}$ is a collection of subsets of some set $X$. Then

$$X \setminus \bigcup_{E \in \mathcal{A}} E = \bigcap_{E \in \mathcal{A}} (X \setminus E)$$

and

$$X \setminus \bigcap_{E \in \mathcal{A}} E = \bigcup_{E \in \mathcal{A}} (X \setminus E) .$$

Proof:

An element $x \in X$ is not in $\bigcup_{E \in \mathcal{A}} E$ if and only if $x$ is not in $E$ for every $E \in \mathcal{A}$. Thus the first equality above holds.

An element $x \in X$ is not in $\bigcap_{E \in \mathcal{A}} E$ if and only if $x$ is not in $E$ for some $E \in \mathcal{A}$. Thus the second equality holds.


### 0.64 union and intersection of closed sets
- The intersection of every collection of closed subsets of $\mathbb{R}^n$ is a closed subset of $\mathbb{R}^n$.
- The union of every finite collection of closed subsets of $\mathbb{R}^n$ is a closed subset of $\mathbb{R}^n$.


### 0.65 sets that are both open and closed
The only subsets of $\mathbb{R}^n$ that are both open and closed are $\emptyset$ and $\mathbb{R}^n$.

Proof:

Suppose $A$ is a subset of $\mathbb{R}^n$ that is both open and closed. 

Suppose towards contradiction that $A \neq \emptyset$ and $A \neq \mathbb{R}^n$. Thus there exist $a \in A$ and $b \in \mathbb{R}^n \ A$. Let

$$T = \\{t \in [0, 1]: (1 - t) a + tb \in A \\}$$

and let

$$s = \sup T.$$

The set $T$ is nonempty because $0 \in T$; thus $s \in [0, 1]$. Let 

$$c = (1 - s) a + sb.$$

Suppose $c \in A$. Then $s \neq 1$ (because otherwise $c = b \notin A$). Because $s \in T$ and $A$ is open, $T$ contains numbers slightly larger than $s$, which contradicts the definition of $s$ as an upper bound of $T$.

Suppose $c \in \mathbb{R}^n \ A$. Then $s \neq 0$ (because otherwise $c = a \in A$). Because $s \notin T$ and $\mathbb{R}^n \ A$ is open, $T$ contains no numbers slightly less than $s$, which contradicts the definition of $s$ as the least upper bound of $T$.

Thus we arrive at a contradiction whether $c \in A$ or $c \in \mathbb{R}^n \ A$, completing the proof. 



## Exercises D

### (1) Suppose $a_1, a_2, ...$ and $c_1, c_2, ...$ are convergent sequences in $\mathbb{R}^n$. Prove that $\lim_{k \to \infty} (a_k + c_k) = \lim_{k \to \infty} a_k + \lim_{k \to \infty} c_k$.

Let $\lim_{k \to \infty} a_k = A$ and $\lim_{k \to \infty} c_k = C$ for some $A, C \in \mathbb{R}^n$.

Let $\epsilon > 0$. By 0.46, there exists $m_1 \in \mathbb{Z}^+$ such that $\lVert a_k - A \rVert_\infty < \epsilon/2$ for all $k \geq m_1$, and there exists $m_2 \in \mathbb{Z}^+$ such that $\lVert c_k - C \rVert_\infty < \epsilon/2$ for all $k \geq m_2$.

Let $M = max(m_1, m_2)$. Then we have $\lVert a_k - A \rVert_\infty < \epsilon/2$ for all $k \geq M \geq m_1$ and $\lVert c_k - C \rVert_\infty < \epsilon/2$ for all $k \geq M \geq m_2$.

By the triangle inequality, 

$$
\begin{aligned}
\lVert (a_k + c_k) - (A + C) \rVert_\infty 
    &= \lVert (a_k - A) + (c_k - C) \rVert_\infty \\
    &\leq \lVert a_k - A \rVert_\infty + \lVert c_k - C \rVert_\infty \\
    &< \epsilon
\end{aligned}
$$

Thus for all $k \geq M$, $\lVert (a_k + c_k) - (A + C) \rVert_\infty < \epsilon$.

Hence we conclude 

$$\lim_{k \to \infty} (a_k + c_k) = A + C = \lim_{k \to \infty} a_k + \lim_{k \to \infty} c_k$$



### (2) Suppose $a_1, a_2, ...$ and $c_1, c_2, ...$ are convergent sequences in $\mathbb{R}$. Prove that $\lim_{k \to \infty} (a_k c_k) = (\lim_{k \to \infty} a_k)(\lim_{k \to \infty} c_k)$.

Let $\lim_{k \to \infty} a_k = A$ and $\lim_{k \to \infty} c_k = C$ for some $A, C \in \mathbb{R}$.

First we want to show that since $a_1, a_2, ...$ is a convergent sequence in $\mathbb{R}$, it is bounded.

Let $\epsilon = 1$. There exists $m \in \mathbb{Z}^+$ such that $|a_k - A| < 1$ for all $k \geq m$. By the triangle inequality, we have

$$|a_k| \leq |a_k - A| + |A| < 1 + |A|$$

for all $k \geq m$.

Let $N = max \\{|a_1|, |a_2|, ..., |a_{m-1}|, 1 + |A|\\}$. Then for each $k < m$, $|a_k| \leq N$. For each $k \geq m$, $|a_k| < 1 + |A| \leq N$. 

Thus $|a_k| \leq N < \infty$ for all $k \in \mathbb{Z}^+$, and the sequence is bounded.

Now we want to show that $a_k c_k$ converges to $AC$.

Note that we have

$$
\begin{aligned}
|a_k c_k - AC| 
    &= |a_k c_k - AC + a_k C - a_k C| \\
    &= |a_k (c_k - C) + C (a_k - A)| \\
    &\leq |a_k (c_k - C)| + |C (a_k - A)| \\
    &= |a_k| |c_k - C| + |C| |a_k - A| \\
    &\leq N |c_k - C| + |C| |a_k - A|
\end{aligned}
$$

Let $\epsilon > 0$. There exists $m_1 \in \mathbb{Z}^+$ such that $|a_k - A| < \frac{\epsilon}{2(|C|+1)}$ for all $k \geq m_1$. There exists $m_2 \in \mathbb{Z}^+$ such that $|c_k - C| < \frac{\epsilon}{2(N+1)}$ for all $k \geq m_2$. 

Let $M = max \\{m_1, m_2\\}$. Then for all $k \geq M$, 

$$
\begin{aligned}
|a_k c_k - AC| 
    &\leq N |c_k - C| + |C| |a_k - A| \\
    &< N \frac{\epsilon}{2(N+1)} + |C| \frac{\epsilon}{2(|C|+1)} \\
    &< \epsilon/2 + \epsilon/2 \\
    &= \epsilon
\end{aligned}
$$

Thus $a_k c_k$ converges to $AC$. Hence we conclude 

$$\lim_{k \to \infty} (a_k c_k) = AC = (\lim_{k \to \infty} a_k) (\lim_{k \to \infty} c_k) .$$



### (3) Prove or give a counterexample: If $a_1, a_2, ...$ and $c_1, c_2, ...$ are convergent sequences in $\mathbb{R}$ and $c_k \neq 0$ for each $k \in \mathbb{Z}^+$, then $\lim_{k \to \infty} a_k / c_k = (\lim_{k \to \infty} a_k) / (\lim_{k \to \infty} c_k)$.

The statement is not true and we provide a counterexample.

Suppose $a_k = 1, k \in \mathbb{Z}^+$ and $c_k = \frac{1}{k}, k \in \mathbb{Z}^+$.

Then we can see that $\lim_{k \to \infty} a_k = 1$ and $\lim_{k \to \infty} c_k = 0$. 

Thus the sequence $\frac{a_k}{c_k} = k, k \in \mathbb{Z}^+$ is not convergent. 



### (4) Suppose $a \in \mathbb{R}$. Prove that there exists a sequence $a_1, a_2, ...$ of rational numbers such that $a = \lim_{k \to \infty} a_k$. 

By 0.30, there is a rational number between every two distinct real numbers. Thus there exists $a_k$ such that $a < a_k < a + \frac{1}{k}$, for all $k \in \mathbb{Z}^+$, where $a, a + \frac{1}{k} \in \mathbb{R}$.

Let $\epsilon > 0$. There exists $m \in \mathbb{Z}^+$ such that $\frac{1}{m} < \epsilon$ by the Archimedean property. For all $k \geq m$, we have

$$|a - a_k| < \frac{1}{k} \leq \frac{1}{m} < \epsilon$$

Hence there exists a sequence of rational numbers $a_1, a_2, ...$ such that $a = \lim_{k \to \infty} a_k$.



### (5) Suppose $a \in \mathbb{R}$. Prove that there exists a sequence $a_1, a_2, ...$ of irrational numbers such that $a = \lim_{k \to \infty} a_k$.

Same argument as (4), invoking 0.39 (there is an irrational number between every two distint real numbers) instead of 0.30.



### (8) Suppose $G$ is an open subset of $\mathbb{R}$. Prove that $\inf G \notin G$ and $\sup G \notin G$.

If $G$ is empty then $\inf G = \infty$, if $G$ has no lower bound then $\inf G = -\infty$. In either case, $inf G \notin G$ vacuously. Thus suppose $inf G = a$ for some $a \in \mathbb{R}$. 

Assume towards contradiction that $a \in G$.

Since $G$ is open, there exists $\delta > 0$ such that $(a - \delta, a + \delta) \subseteq G$. Then $a - \frac{\delta}{2} \in G$. But this contradicts the fact that $a$ is a lower bound of $G$.

Hence we conclude $inf G \notin G$.

Similarly we conclude $\sup G \notin G$ by the same argument.


### (9) Suppose $F$ is a nonempty closed set of positive numbers. Prove that $\inf F \in F$.

Since $F$ is nonempty and bounded below by 0, $\inf F \in \mathbb{R}$. Let $\inf F = a$.

Assume towards contradiction that $a \notin F$. Then $a \in \mathbb{R} \setminus F$ where $\mathbb{R} \setminus F$ is an open subset of $\mathbb{R}$. 

Since $\mathbb{R} \ F$ is open, there exists $\delta > 0$ such that $(a - \delta, a + \delta) \subseteq \mathbb{R} \setminus F$. We have 

$$[a, a + \frac{\delta}{2} ] \subset (a - \delta, a + \delta) \subseteq \mathbb{R} \setminus F .$$

There is no $x \in F$ such that $a \leq x \leq a + \frac{\delta}{2}$. Thus $a + \frac{\delta}{2}$ is a lower bound of $F$. 

This contradicts the fact that $a$ is the greatest lower bound of $F$.

Hence we conclude $\inf F \in F$.



# E Sequences and Continuity

### 0.68 Definition: bounded
- A set $A \subseteq \mathbb{R}^n$ is called bounded if $\sup \\{\lvert a \rvert_\infty : a \in A \\} < \infty$.

- A function into $\mathbb{R}^n$ is called bounded if its range is a bounded subset of $\mathbb{R}^n$.

- As a special case of the previous bullet point, a sequence $a_1, a_2, ...$ of elements of $\mathbb{R}^n$ is called bounded if $\sup \\{\lvert a_k \rvert_\infty : k \in \mathbb{Z}^+ \\} < \infty$.


### 0.74 characterization of closed bounded sets
Suppose $F$ is a closed bounded subset of $\mathbb{R}^n$. Then every sequence of elements of $F$ has a subsequence that converges to an element of $F$.

Proof:

Consider a sequence of elements of $F$. Because $F$ is a bounded set, this sequence is bounded and thus has a convergent subsequence (by the Bolzano-Weierstrass Theorem 0.73). Because $F$ is closed, the limit of this convergent subsequence is in $F$ (by 0.62).


### 0.75


### 0.77


### 0.79 continuity implies uniform continuity on closed bounded sets
Every continuous $\mathbb{R}^n$-valued function on each closed bounded subset of $\mathbb{R}^m$ is uniformly continuous.

Proof:

Suppose $F$ is a closed bounded subset of $\mathbb{R}^m$ and $g: F \to \mathbb{R}^n$ is continuous. We want to show that $g$ is uniformly continuous.

Suppose $g$ is not uniformly continuous. Then there exists $\epsilon > 0$ such that for each $k \in \mathbb{Z}^+$, there exist $a_k, b_k \in F$ with 

$$\lVert a_k - b_k \rVert_\infty < \frac{1}{k}$$

and

$$\lVert g(a_k) - g(b_k) \rVert_\infty \geq \epsilon.$$

Because $F$ is bounded, the sequence $a_1, a_2, ...$ is bounded. Thus by the Bolzano-Weierstrass Theorem (0.73), some subsequence $a_{k_1}, a_{k_2}, ...$ converges to some limit $a$. Because $F$ is closed, we have $a \in F$ by 0.62.

Now

$$
\begin{aligned}
\lVert a - b_{k_j} \rVert_\infty
    &= \lVert (a - a_{k_j}) + (a_{k_j} - b_{k_j}) \rVert_\infty \\
    &\leq \lVert a - a_{k_j} \rVert_\inf + \lVert a_{k_j} - b_{k_j} \rVert_\infty \\
    &< \lVert a - a_{k_j} \rVert_\infty + \frac{1}{k_j}
\end{aligned}
$$

which implies that $\lim_{j \to \infty} b_{k_j} = a$.

Because $g$ is continuous at $a$ and $\lim_{j \to \infty} a_{k_j} = a$ and $\lim_{j \to \infty} b_{k_j} = a$, we conclude that

$$\lim_{j \to \infty} g(a_{k_j}) = g(a)$$

and

$$\lim_{j \to \infty} g(b_{k_j}) = g(a) .$$

Thus 

$$\lim_{j \to \infty} (g(a_{k_j}) - g(b_{k_j})) = 0. $$

The equation above contradicts the inequality $\lVert g(a_k) - g(b_k) \rVert_\infty \geq \epsilon$, which holds for all $k \in \mathbb{Z}^+$. This contradiction means that our assumption that $g$ is not uniformly continuous is false, completing the proof.



# Exercises E

### (1) Prove that every convergent sequence of elements of $\mathbb{R}^n$ is bounded.

Suppose $a_1, a_2, ...$ is a convergent sequence in $\mathbb{R}^n$. Let $\lim_{k \to \infty} a_k = L$ for some $L \in \mathbb{R}^n$. 

Let $\epsilon = 1$. By 0.46, there exists $m \in \mathbb{Z}^+$ such that $\lVert a_k - L \rVert_\infty < 1$ for all $k \geq m$.

By the triangle inequality, we have for all $k \geq m$

$$\lVert a_k \rVert_\infty \leq \lVert a_k - L \rVert_\infty + \lVert L \rVert_\infty < 1 + \lVert L \rVert_\infty .$$

Let 

$$M = max \\{ \lVert a_1 \rVert_\infty, ..., \lVert a_{m-1} \rVert_\infty, 1 + \lVert L \rVert_\infty \\} .$$

Since $\lVert L \rVert_\infty$ is a real number and the set has a finite numbe of elements, $M$ is a real number.

Then for $k \geq m$, 

$$\lVert a_k \rVert_\infty \leq 1 + \lVert L \rVert_\infty \leq M$$

and for $k \in \\{1, ..., m-1\\}$,

$$\lVert a_k \rVert_\infty \leq M .$$

Thus for all $k \in \mathbb{Z}^+$, 

$$\lVert a_k \rVert_\infty \leq M .$$

Hence we conclude 

$$\sup \\{\lVert a_k \rVert_\infty: k \in \mathbb{Z}^+ \\} \leq M < \infty$$ 

and the sequence $a_1, a_2, ...$ is bounded.



### (2) Prove that a sequence of elements of $\mathbb{R}^n$ converges if and only if every subsequence of the sequence converges.

$\Rightarrow$

Suppose $a_1, a_2, ...$ is a sequence in $\mathbb{R}^n$ that converges. Let $\lim_{k \to \infty} a_k = L$ for some $L \in \mathbb{R}^n$. 

We want to show that all subsequences of the form $a_{k_1}, a_{k_2}, ...$ where $k_1 < k_2 < ...$ converges to $L$. 

Suppose $\epsilon > 0$. There exists $m \in \mathbb{Z}^+$ such that $\lVert a_k - L \rVert_\infty < \epsilon$ for all $k \geq m$. 

Since $k_1 < k_2 < ...$ are positive integers, $k_i \geq i$ for each $i \in \mathbb{Z}^+$. So if $i \geq m$, then $k_i \geq m$.

Thus $\lVert a_{k_i} - L \rVert_\infty < \epsilon$ for all $k_i \geq m$. 

Hence we conclude every subsequence of the sequence $a_1, a_2, ...$ converges to the same limit $L$.

$\Leftarrow$
Suppose every subsequence of the sequence converges.

By 0.70, a sequence is a subsequence of itself, if we take $k_i = i$ for each $i \in \mathbb{Z}^+$. Thus if every subsequence of the sequence converges, then the sequence converges.



### (3) Prove the converse of 0.74. Specifically, prove that if $F$ is a subset of $\mathbb{R}^n$ with the property that every sequence of elements of $F$ has a subsequence that converges to an element of $F$, then $F$ is closed and bounded.

First we want to show that $F$ is bounded. Assume towards contradiction that $F$ is not bounded. 

Then $\sup \\{ \lVert a \rVert_\infty: a \in F \\} = \infty$. 

For every $k \in \mathbb{Z}^+$, we can find an element $a_k \in F$ such that $\lVert a_k \rVert_\infty > k$, so the sequence is not bounded.

By hypothesis, $a_1, a_2, ...$ has a subsequence $a_{k_1}, a_{k_2}, ...$ that converges to an element of $F$, which we call $L$. Every convergent sequence is bounded (by Exercise 1). 

Since $k_i \geq i$ for each $i \in \mathbb{Z}^+$, we have $\lVert a_{k_i} \rVert_\infty > k_i \geq i$ for every $i \in \mathbb{Z}^+$. Thus the subsequence is unbounded, which is a contradiction. 

Hence we conclude that $F$ is bounded.

Next we want to show that $F$ is closed.

Suppose $a_1, a_2, ...$ is a convergent sequence in $F$ with limit $M$. By hypothesis, it has a convergent subsequence $a_{k_1}, a_{k_2}, ...$ which converges to $L \in F$. 

Let $\epsilon > 0$. There exists $m \in \mathbb{Z}^+$ such that $\lVert a_k - M \rVert_\infty < \epsilon$ for all $k \geq m$. 

Since $k_i >= i$ for each $i \in \mathbb{Z}^+$, for all $i \geq m$, we have $\lVert a_{k_i} - M \rVert_\infty < \epsilon$ for all $k_i \geq i \geq m$. Thus $\lim_{k_i \to \infty} a_{k_i} = M$.

Since $a_{k_1}, a_{k_2}, ...$ converges to $L$, by the uniqueness of limit, $L = M$ and $M \in F$. 

By 0.62, $F$ is closed. 



### (5) Prove 0.76. Suppose $A \subseteq \mathbb{R}^m$ and $f: A \to \mathbb{R}^n$ is a function. Suppose $b \in A$. Then $f$ is continuous at $b$ if and only if $\lim_{k \to \infty} f(b_k) = f(b)$ for every sequence $b_1, b_2, ...$ in $A$ such that $\lim_{k \to \infty} b_k = b$. 

$\Rightarrow$

Suppose $f$ is continuous at $b$. We want to show that $\lim_{k \to \infty} f(b_k) = f(b)$ for every sequence $b_1, b_2, ... \in A$ where $\lim_{k \to \infty} b_k = b$.

Let $b_1, b_2, ...$ be a sequence in $A$ such that $\lim_{k \to \infty} b_k = b$.

Let $\epsilon > 0$. There exists $\delta > 0$ such that $\lVert f(a) - f(b) \rVert_\infty < \epsilon$ for all $a \in A$ with $\lVert a - b \rVert_\infty < \delta$. There exists $M \in \mathbb{Z}^+$ such that $\lVert b_k - b \rVert_\infty < \delta$ for all $k \geq M$. 

Thus for all $k \geq M$, $\lVert f(b_k) - f(b) \rVert_\infty < \epsilon$. 

Hence we conclude that $\lim_{k \to \infty} f(b_k) = f(b)$ for every sequence $b_1, b_2, ...$ in $A$ such that $\lim_{k \to \infty} b_k = b$.

$\Leftarrow$

Suppose $\lim_{k \to \infty} f(b_k) = f(b)$ for every sequence $b_1, b_2, ...$ in $A$ where $\lim_{k \to \infty} b_k = b$. 

Assume towards contradiction that $f$ is not continuous at $b$.

Then there exists some $\epsilon > 0$ such that, for all $\delta > 0$, there is some $a \in A$ such that $\lVert a - b \rVert_\infty < \delta$ but $\lVert f(a) - f(b) \rVert_\infty \geq \epsilon$.

In particular, for each $k \in \mathbb{Z}^+$, taking $\delta = \frac{1}{k}$ gives $\lVert a_k - b \rVert_\infty < \frac{1}{k}$ and $\lVert f(a_k) - f(b) \rVert_\infty \geq \epsilon$.

We can see that $\lim_{k \to \infty} a_k = b$. 

By hypothesis, $\lim_{k \to \infty} f(a_k) = f(b)$. There exists $N \in \mathbb{Z}^+$ such that $\lVert f(a_N) - f(b) \rVert_\infty < \epsilon$. We have arrivded at a contradiction.

Hence we conclude that $f$ is continuous at $b$.



### (6) Show that the function $f: (0, \infty) \to \mathbb{R}$ defined by $f(x) = \frac{1}{x}$ is not uniformly continuous.

We want to show that $f(x) = \frac{1}{x}$ is not uniformly continuous, i.e., there exists $\epsilon > 0$ such that for all $\delta > 0$, $|f(a) - f(b)| \geq \epsilon$ and $|a-b| < \delta$ for some $a, b \in (0, \infty)$.

Let $\epsilon = \frac{1}{2}$. Let $\delta > 0$. By the Archimedean property, choose $k \in \mathbb{Z}^+$ such that $\frac{1}{k} < \delta$. 

Let $a = \frac{1}{k+1}$ and $b = \frac{1}{k}$, $a, b \in (0, \infty)$. Then

$$\left| \frac{1}{k+1} - \frac{1}{k} \right| = \frac{1}{k(k+1)} < \frac{1}{k} < \delta$$

but

$$\left| f(\frac{1}{k+1}) - f(\frac{1}{k}) \right| = (k+1) - k = 1 > \frac{1}{2} .$$

Thus for $\epsilon = \frac{1}{2}$, no $\delta > 0$ works.

Hence we conclude $f(x) = \frac{1}{x}$ is not uniformly continuous.


### (7) Suppose $p \in (0, \infty)$. Show that the function $f: \mathbb{R} \to \mathbb{R}$ defined by $f(x) = |x|^p$ is uniformly continuous if and only $p \in (0, 1]$.

First we want to show that $f(x) = |x|^p$ is not uniformly continuous when $p > 1$. There exists $\epsilon > 0$ such that, for all $\delta > 0$, we have $|b-a| < \delta$ but $|f(b) - f(a)| \geq \epsilon$ for some $a, b \in \mathbb{R}$.

Let $\epsilon = frac{p}{2}$.

Let $\delta > 0$. Take $n \in \mathbb{Z}^+$ such that $n^{1-p} < \delta$. This is doable because $p > 1$, so $n^{1-p} \to 0$ as $n \to \infty$.

Consider $a = n$ and $b = n + n^{1-p}$. Since 

$$f''(n) = p (p-1) n^{p-2} > 0,$$

the function is convex at $x \in [a, b]$. We have

$$
\begin{aligned}
f(n + n^{1-p}) 
    &\geq f(n) + f'(n) (n^{1-p}) \\
    &= n^p + p n^{p-1} n^{1-p} \\
    &= n^p + p
\end{aligned}
$$

and

$$f(n + n^{1-p}) - f(n) \geq n^p + p - n^p = p .$$

Thus for $\epsilon = \frac{p}{2}$, $\forall \delta > 0$, we have found

$$|b-a| = n^{1-p} < \delta$$

but

$$|f(b) - f(a)| \geq p > \frac{p}{2} .$$

Hence we conclude that $f(x) = |x|^p$ is not uniformly continuous when $p > 1$.

Now we want to show that $f(x) = |x|^p$ is uniformly continuous when $p \in (0, 1]$. For every $\epsilon > 0$, there exists $\delta > 0$ such that $|f(a) - f(b)| < \epsilon$ for all $a, b \in \mathbb{R}$ with $|a-b| < \delta$.

Before we prove the claim, we will prove this lemma needed in the proof: For $p \in (0, 1]$ and $s, t \geq 0$, $(s+t)^p \leq s^p + t^p$.

Let $\lambda = \frac{s}{s + t} \in [0, 1]$. We have $\lambda^p \geq \lambda$ and $(1 - \lambda)^p \geq 1 - \lambda$. Then

$$\lambda^p + (1 - \lambda)^p \geq \lambda + (1 - \lambda) = 1$$

Substituting back $\lambda = \frac{s}{s+t}$, we have

$$\frac{s^p}{(s+t)^p} + \frac{t^p}{(s+t)^p} \geq 1$$

Multiplying $(s+t)^p$ to both sides, we obtain the desired inequality:

$$s^p + t^p \geq (s+t)^p.$$

Now we are going to prove the claim. Let $\epsilon > 0$. Let $\delta = \epsilon^{1/p}$. Let $x, y \in \mathbb{R}$ with $|x-y| < \delta$. 

By the triangle inequality, we have

$$|x| = |x - y + y| \leq |x - y| + |y|$$

Since $t \to t^p$ is non-decreasing on $[0, \infty)$, the inequality is preserved if we raise it to the power of $p$. Then we can use the lemma from above.

$$|x|^p \leq (|x - y| + |y|)^p \leq |x-y|^p + |y|^p$$

Thus we have

$$|x|^p - |y|^p \leq |x-y|^p .$$

Since the same inequality would hold if we flip the role of $x$ and $y$, i.e. $|y|^p - |x|^p \leq |y-x|^p$, we can conclude

$$
\begin{aligned}
\left| |x|^p - |y|^p \right| 
    &\leq |x-y|^p \\
    &< \delta^p \\
    &= (\epsilon^{1/p})^p \\
    &= \epsilon
\end{aligned}
$$

Hence we conclude that $f(x) = |x|^p$ is uniformly continuous when $p \in (0, 1]$.



### (8) Prove or give a counterexample: If $f: \mathbb{R} \to \mathbb{R}$ is a bounded continuous function, then $f$ is uniformly continuous.


### (9) Prove or give a counterexample: If $f: (0, 1) \to \mathbb{R}$ is a bounded continuous function, then $f$ is uniformly continuous.


### (13) Prove or give a counterexample: If $f: \mathbb{R}^m \to \mathbb{R}^n$ is continuous and $\lVert f(x) \rVert < \frac{1}{\lVert x \rVert}$ for all $x \in \mathbb{R}^m$ with $\lVert x \rVert > 1$, then $f$ is uniformly continuous.


### (14) Prove or give a counterexample: The sum of two uniformly continuous functions from $\mathbb{R}^m$ to $\mathbb{R}^n$ is uniformly continuous.



### (15) Prove or give a counterexample: The product of two uniformly continuous functions from $\mathbb{R}$ to $\mathbb{R}$ is uniformly continuous.



### (16) Prove or a give a counterexample: If $f: \mathbb{R} \to (0, \infty)$ is uniformly continuous, then the function $\frac{1}{f}$ is uniformly continuous on $\mathbb{R}$.



### (17) Prove or give a counterexample: If $f, g: \mathbb{R} \to \mathbb{R}$ are uniformly continuous functions, then the composition $f \circ g: \mathbb{R} \to \mathbb{R}$ is uniformly continuous.


### (18) Suppose $h: \mathbb{R}^m \to \mathbb{R}^n$ is a function. Prove that $h$ is continuous if and only if $h^{-1} (G)$ is an open subset of $\mathbb{R}^m$ for every open subset of $G$ of $\mathbb{R}^n$.


### (19) Suppose $h: \mathbb{R}^m \to \mathbb{R}^n$ is a function. Prove that $h$ is continuous if and only if $h^{-1} (F)$ is a closed subset of $\mathbb{R}^m$ for every closed subset $F$ of $\mathbb{R}^n$.


### (32) Prove that every convergent sequence of elements of $\mathbb{R}^n$ is a Cauchy sequence.


### (33) 
#### (a) Prove that every Cauchy sequence of elements of $\mathbb{R}^n$ is bounded.

#### (b) Prove that if some subseqeunce of a Cauchy sequence of elements of $\mathbb{R}^n$ converges to some $L \in \mathbb{R}^n$, then the Cauchy sequence has limit $L$.

#### (c) Prove that every Cauchy sequence of elements of $\mathbb{R}^n$ converges.

