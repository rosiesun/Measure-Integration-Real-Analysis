Measure Integration Real Analysis - Chapter 3 <br>
Integration
================
Rosie Sun <br>
2026-09-13


# 3A Integration with Respect to a Measure

### 3.1 Definition: $\mathcal{S}$-partition
Suppose $\mathcal{S}$ is a $\sigma$-algebra on a set $X$. An $\mathcal{S}$-partition of $X$ is a finite collection $A_1, ..., A_m$ of disjoint sets in $\mathcal{S}$ such that $A_1 \cup ... \cup A_m = X$.


### 3.2 Definition: lower Lebesgue sum
Suppose $(X, \mathcal{S}, \mu)$ is a measure space, $f: X \to [0, \infty]$ is an $\mathcal{S}$-measurable function, and $P$ is an $\mathcal{S}$-partition $A_1, ..., A_m$ of $X$. The lower Lebesgue sum $\mathcal{L}(f, P)$ is defined by

$$\mathcal{L}(f, P) = \sum_{j=1}^m \mu(A_j) \inf_{A_j} f .$$


### 3.3 Definition: integral of a nonnegative function
Suppose $(X, \mathcal{S}, \mu)$ is a measure space and $f:  X \to [0, \infty]$ is an $\mathcal{S}$-measurable function. The integral of $f$ with respect to $\mu$, denoted $\int f d\mu$, is defined by

$$\int f d\mu = \sup \\{\mathcal{L}(f, P): P \text{ is an } \mathcal{S} \text{-partition of } X \\} .$$


### 3.4 integral of a characteristic function
Suppose $(X, \mathcal{S}, \mu)$ is a measure space and $E \in \mathcal{S}$. Then

$$\int \chi_E d\mu = \mu(E) .$$

Proof:

If $P$ is the $\mathcal{S}$-partition of $X$ consisting of $E$ and its complement $X \setminus E$, then 

$$\mathcal{L}(\chi_E, P) = \mu(E) \inf_E \chi_E + \mu(X \setminus E) \inf_{X \setminus E} \chi_E = \mu(E) * 1 + \mu(X \setminus E) * 0 = \mu(E)$$

Thus 

$$\int \chi_E d\mu \geq \mu(E) .$$

To prove the inequality in the other direction, suppose $P$ is an $\mathcal{S}$-partition $A_1, ..., A_m$ of $X$. Then

$$
\mu(A_j) \inf_{A_j} \chi_E =
\begin{cases}
    \mu(A_j) \text{ if } A_j \subset E \\
    0 \text{ otherwise}
\end{cases}
$$

Thus

$$
\begin{aligned}
\mathcal{L}(\chi_E, P) 
    &= \sum_{j=1}^m \mu(A_j) \inf_{A_j} \chi_E \\
    &= \sum_{j: A_j \subset E} \mu(A_j) \\
    &= \mu \left( \bigcup_{j: A_j \subset E} A_j \right) \\
    &\leq mu(E)
\end{aligned}
$$

Thus 

$$\int \chi_E d\mu \leq \mu(E) ,$$

completing the proof.



### 3.5 Example: integrals of $\chi_{\mathbb{Q}} and \chi_{[0,1] \setminus \mathbb{Q}}$
Suppose $\lambda$ is Lebesgue measure on $\mathbb{R}$. As a special case of the result above, we have 

$$\int \chi_{\mathbb{Q}} d\lambda = 0 $$

because $|\mathbb{Q}| = 0$. Recall that $\chi_{\mathbb{Q}}$ is not Riemann integrable on [0, 1].

Note also that 3.4 implies that 

$$\int \chi_{[0, 1] \setminus \mathbb{Q}} d\lambda = 1$$

because $|[0, 1] \setminus \mathbb{Q} | = 1$, which is what we want. In contrast, the lower Riemann integral of $\chi_{[0, 1] \setminus \mathbb{Q}}$ on [0, 1] equals 0, which is not what we want.


### 3.6 Example: integration with respect to counting measure is summation
Suppose $\mu$ is counting measure on $\mathbb{Z}^+$ and $b_1, b_2, ...$ is a sequence of nonnegative numbers. Think of $b$ as the function from $\mathbb{Z}^+$ to $[0, \infty)$ defined by $b(k) = b_k$. Then

$$\int b d\mu = \sum_{k=1}^\infty b_k .$$


### 3.7 integral of a simple function
Suppose $(X, \mathcal{S}, \mu)$ is a measure space, $E_1, ..., E_n$ are disjoint sets in $\mathcal{S}$, and $c_1, ..., c_n \in [0, \infty]$. Then

$$\int \left( \sum_{k=1}^n c_k \chi_{E_k} \right) d\mu = \sum_{k=1}^n c_k \mu(E_k) .$$

Proof:

Without loss of generality, we can assume that $E_1, ..., E_n$ is an $\mathcal{S}$-partition of $X$, by replacing $n$ by $n+1$, and setting $E_{n+1} = X \setminus (E_1 \cup ... \cup E_n)$ and $c_{n+1} = 0$.

If $P$ is the $\mathcal{S}$-partition $E_1, ..., E_n$ of $X$, then 

$$
\begin{aligned}
\mathcal{L}(\sum_{k=1}^n c_k \chi_{E_k}, P) 
    &= \sum_{k=1}^n \mu(E_k) (\inf_{E_k} \sum_{k=1}^n c_k \chi_{E_k}) \\
    &= \sum_{k=1}^n \mu(E_k) c_k
\end{aligned}
$$

Thus

$$\int (\sum_{k=1}^n c_k \chi_{E_k} ) d\mu \geq \sum_{k=1}^n c_k \mu(E_k) $$

To prove the inequality in the other direction, suppose that $P$ is an $\mathcal{S}$-partition $A_1, ..., A_m$ of $X$. Then

$$
\begin{aligned}
\mathcal{L} \left(\sum_{k=1}^n c_k \chi_{E_k}, P \right) 
    &= \sum_{j=1}^m \mu(A_j) \inf_{A_j} \sum_{k=1}^n c_k \chi_{E_k} \\
    &= \sum_{j=1}^m \mu(A_j) \min_{i: A_j \cap E_i \neq \emptyset} c_i \\
    &= \sum_{j=1}^m \sum_{k=1}^n \mu(A_j \cap E_k) \min_{i: A_j \cap E_k \neq \emptyset} c_i \\
    &\leq \sum_{j=1}^m \sum_{k=1}^n \mu(A_j \cap E_k) c_k \\
    &= \sum_{k=1}^n c_k \sum_{j=1}^m \mu(A_j \cap E_k) \\
    &= \sum_{k=1}^n c_k \mu(E_k)
\end{aligned}
$$

The inequality above implies that 

$$\int (\sum_{k=1}^n c_k \chi_{E_k}) d\mu \leq \sum_{k=1}^n c_k \mu(E_k) $$

completing the proof.



### 3.8 integration is order-preserving
Suppose $(X, \mathcal{S}, \mu)$ is a measure space and $f, g: X \to [0, \infty]$ are $\mathcal{S}$-measurable functions such that $f(x) \leq g(x)$ for all $x \in X$. Then $\int f d\mu \leq \int g d\mu$.

Proof:

Suppose $P$ is an $\mathcal{S}$-partition $A_1, ..., A_m$ of $X$. Then

$$\inf_{A_j} f \leq \inf_{A_j} g$$

for each $j = 1, ..., m$. Thus $\mathcal{L}(f, P) \leq \mathcal{L}(g, P)$. Hence $\int f d\mu \leq \int g d\mu$.



### 3.9 integrals via simple functions
Suppose $(X, \mathcal{S}, \mu)$ is a measure space and $f: X \to [0, \infty]$ is $\mathcal{S}$-measurable. Then

$$
\begin{multiline}
(3.10)  \int f d\mu = \sup 
    \left\\{
    \sum_{j=1}^m c_j \mu(A_j): A_1, ..., A_m \text{ are disjoint sets in } \mathcal{S}, \\
    c_1, ..., c_m \in [0, \infty), \text{ and } \\
    f(x) \geq \sum_{j=1}^m c_j \chi_{A_j}(x) \forall x \in X 
    \right\\}
\end{multiline}
$$

Proof:

First note that the left side of 3.10 is bigger than or equal to the right side by 3.7 and 3.8.

Since 

$$f(x) \geq \sum_{j=1}^m c_j \chi_{A_j}(x) \forall x \in X$$ 

we have

$$
\begin{aligned}
\int f d\mu 
    &\geq \int (\sum_{j=1}^m c_j \chi_{A_j}) d\mu \\
    &= \sum_{j=1}^m c_j \mu(A_j)
\end{aligned}
$$

where the first inequality follows from 3.8 and the first equality follows from 3.7.

Since the inequality holds for arbitrary disjoint $A_1, ..., A_m \in \mathcal{S}$, taking the supremum preserves the inequality. 

To prove that the right side of 3.10 is bigger than or equal to the left side, first assume that $\inf_A f < \infty$ for every $A \in \mathcal{S}$ with $\mu(A) > 0$.

Then for $P$ an $\mathcal{S}$-partition $A_1, ..., A_m$ of nonempty subsets of $X$, take $c_j = \inf_{A_j} f$, which shows that $\mathcal{L}(f, P)$ is in the set on the right side of 3.10. Recall that if $E_1 \supseteq E_2$, then $\sup E_1 \geq \sup E_2$. Thus the definition of $\int f d\mu$ shows that the right side of 3.10 is bigger than or equal to the left side.

The only remaining case to consider is when there exists a set $A \in \mathcal{S}$ such that $\mu(A) > 0$ and $\inf_A f = \infty$ (which implies that $f(x) = \infty \forall x \in A$). In this case, for arbitrary $t \in (0, \infty)$, we can take $m = 1$, $A_1 = A$, and $c_1 = t$. These choices show that the right side of 3.10 is at least $t \mu(A)$. Because $t$ is an arbitrary positive number, this shows that the right side of 3.10 equals $\infty$, which of course is greater than or equal to the left side, completing the proof.



### 3.11 Monotone Convergence Theorem
Suppose $(X, \mathcal{S}, \mu)$ is a measure space and $0 \leq f_1 \leq f_2 \leq ...$ is an increasing sequence of $\mathcal{S}$-measurable functions. Define $f: X \to [0, \infty]$ by

$$f(x) = lim_{k \to \infty} f_k(x) .$$

Then

$$lim_{k \to \infty} \int f_k d\mu = \int f d\mu .$$


Proof:

The function $f$ is $\mathcal{S}$-measurable by 2.53.

Because $f_k(x) \leq f(x)$ for every $x \in X$, we have 

$$\int f_k d\mu \leq \int f d\mu$$

for each $k \in \mathbb{Z}^+$ by 3.8. Thus 

$$\lim_{k \to \infty} \int f_k d\mu \leq \int f d\mu $$

To prove the inequality in the other direction, suppose $A_1, ..., A_m$ are disjoint sets in $\mathcal{S}$ and $c_1, ..., c_m \in [0, \infty)$ are such that

$$f(x) \geq \sum_{j=1}^m c_j \chi_{A_j}(x) \forall x \in X$$

Let $t \in (0, 1)$. For $k \in \mathbb{Z}^+$, let 

$$E_k = \left\\{x \in X: f_k(x) \geq t \sum_{j=1}^m c_j \chi_{A_j}(x) \right\\} $$

Then $E_1 \subset E_2 \subset ...$ is an increasing sequence of sets in $\mathcal{S}$ whose union equals $X$. Thus by 2.59,

$$\lim_{k \to \infty} \mu(A_j \cap E_k) = \mu(A_j) \forall j \in \\{1, ..., m\\}$$

If $k \in \mathbb{Z}^+$, then

$$f_k(x) \geq \sum_{j=1}^m t c_j \chi_{A_j \cap E_k}(x)$$

for every $x \in X$. Thus, by 3.9,

$$\int f_k d\mu \geq t \sum_{j=1}^m c_j \mu(A_j \cap E_k)$$

Taking the limit as $k \to \infty$ of both sides of the inequality above gives

$$\lim_{k \to \infty} \int f_k d\mu \geq t \sum_{j=1}^m c_j \mu(A_j)$$

Now taking the limit as $t$ increases to 1 shows that 

$$\lim_{k \to \infty} \int f_k d\mu \geq \sum_{j=1}^m c_j \mu(A_j)$$

Taking the supremum of the inequality above over all $\mathcal{S}$-partitions $A_1, ..., A_m$ of $X$ and all $c_1, ..., c_m \in [0, \infty)$ satisfying 3.12 shows (using 3.9) that we have

$$\lim_{k \to \infty} \int f_k d\mu \geq \int f d\mu$$

completing the proof.



The representation of a simple function $h: X \to [0, \infty]$ in the form $\sum_{k=1}^n c_k \chi_{E_k}$ is not unique. Requiring the numbers $c_1, ..., c_n$ to be distinct and $E_1, ..., E_n$ to be nonempty and disjoint with $E_1 \cup ... \cup E_n = X$ produces what is called the standard representation of a simple function [take $E_k = h^{-1}(\\{c_k\\})$, where $c_1, ..., c_n$ are the distinct values of $h$]. 



### 3.13 integral-type sums for simple functions
Suppose $(X, \mathcal{S}, \mu)$ is a measure space. Suppose $a_1, ..., a_m, b_1, ..., b_n \in [0, \infty]$ and $A_1, ..., A_m, B_1, ..., B_n \in \mathcal{S}$ are such that 

$$\sum_{j=1}^m a_j \chi_{A_j} = \sum_{k=1}^n b_k \chi_{B_k} .$$

Then

$$\sum_{j=1}^m a_j \mu(A_j) = \sum_{k=1}^n b_k \mu(B_k).$$

Proof:

We assume $A_1 \cup ... \cup A_m = X$ (otherwise add the term $0 \chi_{X \setminus (A_1 \cup ... \cup A_m)}$).

Suppose $A_1$ and $A_2$ are not disjoint. Then we can write

$$(3.14) \quad a_1 \chi_{A_1} + a_2 \chi_{A_2} = a_1 \chi_{A_1 \setminus A_2} + a_2 \chi_{A_2 \setminus A_1} + (a_1 + a_2) \chi_{A_1 \cap A_2}$$

where the three sets appearing on the right side of the equation above are disjoint. 

Now 

$$A_1 = (A_1 \setminus A_2) \bigcup (A_1 \bigcap A_2)$$

and

$$A_2 = (A_2 \setminus A_1) \bigcup (A_1 \bigcap A_2)$$

each of these unions is a disjoint union. Thus 

$$\mu(A_1) = \mu(A_1 \setminus A_1) + \mu(A_1 \bigcap A_2)$$

and

$$\mu(A_2) = \mu(A_2 \setminus A_1) + \mu(A_1 \bigcap A_2)$$

Hence

$$a_1 \mu(A_1) + a_2 \mu(A_2) =
a_1 \mu(A_1 \setminus A_2) + a_2 \mu(A_2 \setminus A_1) + (a_1 + a_2) \mu(A_1 \bigcap A_2)
$$

The equation above, in conjunction with 3.14, shows that if we replace the two sets $A_1, A_2$ by the three disjoint sets $A_1 \setminus A_2$, $A_2 \setminus A_1$, $A_1 \cap A_2$ and make the appropriate adjustments to the coefficients $a_1, ..., a_m$, then the value $\sum_{j=1}^m a_j \mu(A_j)$ is unchanged (although $m$ has increased by 1).

Repeating this process with all pairs of subsets among $A_1, ..., A_m$ that are not disjoint after each step, in a finite number of steps we can convert the initial list $A_1, ..., A_m$ into a disjoint list of subsets without changing the value of $\sum_{j=1}^m a_j \mu(A_j)$.

The next step is to make the numbers $a_1, ..., a_m$ distinct. This is done by replacing the sets corresponding to each $a_j$ by the union of those sets, and using finite additivity of the measure $\mu$ to show that the value of the sum $\sum_{j=1}^m a_j \mu(A_j)$ does not change.

Finally, drop any terms for which $A_j = \emptyset$, getting the standard representation for a simple function.

We have now shown that the original value of $\sum_{j=1}^m a_j \mu(A_j)$ is equal to the value if we use the standard representation of the simple function $\sum_{j=1}^m a_j \chi_{A_j}$. 

The same procedure can be used with the representation $\sum_{k=1}^n b_k \chi_{B_k}$ to show that $\sum_{k=1}^n b_k \mu(B_k)$ equals what we would get with the standard representation. 

Thus the equality of the functions 

$$\sum_{j=1}^m a_j \chi_{A_j} = \sum_{k=1}^n b_k \chi_{B_k}$$ 

implies the equality 

$$\sum_{j=1}^m a_j \mu(A_j) = \sum_{k=1}^n b_k \mu(B_k)$$



### 3.15 integral of a linear combination of characteristic functions
Suppose $(X, \mathcal{S}, \mu)$ is a measure space, $E_1, ..., E_n \in \mathcal{S}$, and $c_1, ..., c_n \in [0, \infty]$. Then

$$\int \left( \sum_{k=1}^n c_k \chi_{E_k} \right) d\mu = \sum_{k=1}^n c_k $$


### 3.16 additivity of integration 
Suppose $(X, \mathcal{S}, \mu)$ is a measure space and $f, g: X \to [0, \infty]$ are $\mathcal{S}$-measurable functions. Then

$$\int (f + g) d\mu = \int f d\mu + \int g d\mu .$$

Proof:

The desired result holds for simple nonnegative $\mathcal{S}$-measurable functions by 3.15. Thus we approximate by such functions.

Specifically, let $f_1, f_2, ...$ and $g_1, g_2, ...$ be increasing sequences of simple nonnegative $\mathcal{S}$-measurable functions such that

$$\lim_{k \to \infty} f_k(x) = f(x)$$

and

$$\lim_{k \to \infty} g_k(x) = g(x)$$

for all $x \in X$ by 2.89. Then

$$
\begin{aligned}
\int (f + g) d\mu &= \lim_{k \to \infty} (f_k + g_k) d\mu \\
    &= \lim_{k \to \infty} \int f_k d\mu + \lim_{k \to \infty} g_k d\mu \\
    &= \int f d\mu + \int g d\mu
\end{aligned}
$$

where the first and third equalities follow from the Monotone Convergence Theorem and the second equality holds by 3.15.



### 3.17 Definition: $f^+$; $f^-$
Suppose $f: X \to [-\infty, \infty]$ is a function. Define functions $f^+$ and $f^-$ from $X$ to $[0, \infty]$ by

$$
f^+(x) = 
\begin{cases}
    f(x) & \text{ if } f(x) \geq 0 \\
    0 & \text{ if } f(x) < 0
\end{cases}
$$

and

$$
f^-(x) = 
\begin{cases}
    0 & \text{ if } f(x) \geq 0 \\
    -f(x) & \text{ if } f(x) < 0
\end{cases}
$$

Note that if $f: X \to [-\infty, \infty]$ is a function, then

$$f = f^+ - f^-$$

and

$$|f| = f^+ + f^-$$

The decomposition above allows us to extend our definition of integration to functions that take on negative as well as positive values.


### 3.18 Definition: integral of a real-valued function
Suppose $(X, \mathcal{S}, \mu)$ is a measure space and $f: X \to [-\infty, \infty]$ is an $\mathcal{S}$-measurable function such that at least one of $\int f^+ d\mu$ and $\int f^- d\mu$ is finite. The integral of $f$ with respect to $\mu$, denoted $\int f d\mu$, is defined by

$$\int f d\mu = \int f^+ d\mu - \int f^- d\mu$$


The condition $\int |f| d\mu < \infty$ is equivalent to the condition $\int f^+ d\mu < \infty$ and $\int f^- d\mu < \infty$ (because $|f| = f^+ + f^-$).


### 3.19 Example: a function whose integral is not defined
Suppose $\lambda$ is Lebesgue measure on $\mathbb{R}$ and $f: \mathbb{R} \to \mathbb{R}$ is the function defined by

$$
f(x) =
\begin{cases}
1 & \text{ if } x \geq 0 \\
-1 & \text{ if } x < 0
\end{cases}
$$

Then $\int f d\lambda$ is not defined because $\int f^+ d\lambda = \infty$ and $\int f^- d\lambda = \infty$.


### 3.20 integration is homogeneous
Suppose $(X, \mathcal{S}, \mu)$ is a measure space and $f: X \to [-\infty, \infty]$ is a function such that $\int f d\mu$ is defined. If $c \in \mathbb{R}$, then

$$\int cf d\mu = c \int f d\mu$$

Proof:

First consider the case where $f$ is a nonnegative function and $c \geq 0$. If $P$ is an $\mathcal{S}$-partition $A_1, ..., A_m$ of $X$, then 

$$
\begin{aligned}
\mathcal{L}(cf, P) 
    &= \sum_{j=1}^m \mu(A_j) \inf_{A_j} cf \\
    &= c \sum_{j=1}^m \mu(A_j) \inf_{A_j} f \\
    &= c \mathcal{L}(f, P) 
\end{aligned}
$$

Thus

$$\int cf d\mu = c \int f d\mu$$

Now consider the general case where $f$ takes values in $[-\infty, \infty]$. Suppose $c \geq 0$. Then

$$
\begin{aligned}
\int cf d\mu 
    &= \int (cf)^+ d\mu - \int (cf)^- d\mu \\
    &= \int cf^+ d\mu - \int cf^- d\mu \\
    &= c \left( \int f^+ d\mu - \int f^- d\mu \right) \\
    &= c \int f d\mu
\end{aligned}
$$

where the third line follows from the first paragraph of this proof.

Finally, now suppose $c < 0$ (still assuming that $f$ takes values in $[-\infty, \infty]$). Then $-c > 0$ and

$$
\begin{aligned}
\int cf d\mu 
    &= \int (cf)^+ d\mu - \int (cf)^- d\mu \\
    &= \int (-c) f^- d\mu - \int (-c) f^+ d\mu \\
    &= (-c) \left( \int f^- d\mu - \int f^+ d\mu \right) \\
    &= c \left( \int f^+ d\mu - \int f^- d\mu \right)
    &= c \int f d\mu
\end{aligned}
$$

completing the proof.



### 3.21 additivity of integration
Suppose $(X, \mathcal{S}, \mu)$ is a measure space and $f, g: X \to \mathbb{R}$ are $\mathcal{S}$-measurable functions such that $\int |f| d\mu < \infty$ and $\int |g| d\mu < \infty$. Then

$$\int (f + g) d\mu = \int f d\mu + \int g d\mu$$

Proof:

We have

$$f + g = (f + g)^+ - (f + g)^- $$

and

$$f + g = f^+ - f^- + g^+ - g^-$$

Thus 

$$(f + g)^+ - (f + g)^- = f^+ - f^- + g^+ - g^-$$

Rearranging, we have

$$(f + g)^+ + f^- + g^- = (f + g)^- + f^+ + g^+$$

Both sides of the equation above are sums of nonnegative functions. Thus integrating both sides with respect to $\mu$ and using 3.16 gives

$$
\int (f + g)^+ d\mu + \int f^- d\mu + \int g^- d\mu =
\int (f + g)^- d\mu + \int f^+ d\mu + \int g^+ d\mu
$$

Rearranging the equation above gives

$$
\int (f + g)^+ d\mu - \int (f + g)^- d\mu =
\int f^+ d\mu - \int f^- d\mu + \int g^+ d\mu - \int g^- d\mu
$$

where the left side is not of the form $\infty - \infty$ because $(f + g)^+ \leq f^+ + g^+$ and $(f + g)^- \leq f^- + g^-$. The equation above can be rewritten as

$$\int (f + g) d\mu = \int f d\mu + \int g d\mu$$

completing the proof.



### 3.22


### 3.23 absolute value of integral $\leq$ integral of absolute value
Suppose $(X, \mathcal{S}, \mu)$ is a measure space and $f: X \to [-\infty, \infty]$ is a function such that $\int f d\mu$ is defined. Then

$$\left| \int f d\mu \right| \leq \int |f| d\mu .$$

Proof:

Because $\int f d\mu$ is defined, $f$ is an $\mathcal{S}$-measurable function and at least one of $\int f^+ d\mu$ and $\int f^- d\mu$ is finite. Thus

$$
\begin{aligned}
\left| \int f d\mu \right| 
    &= \left| \int f^+ d\mu - \int f^- d\mu \right| \\
    &\leq \int f^+ d\mu + \int f^- d\mu \\
    &= \int (f^+ + f^-) d\mu \\
    &= \int |f| d\mu
\end{aligned}
$$

as desired.





# 3B Limits of Integrals & Integrals of Limits

### 3.24 Definition: integration on a subset
Suppose $(X, \mathcal{S}, \mu)$ is a measure space and $E \in \mathcal{S}$. If $f: X \to [-\infty, \infty]$ is an $\mathcal{S}$-measurable function, then $\int_E f d\mu$ is defined by

$$\int_E f d\mu = \int \chi_E f d\mu$$

if the right side of the equation above is defined; otherwise $\int_E f d\mu$ is undefined.


### 3.25 bounding an integral
Suppose $(X, \mathcal{S}, \mu)$ is a measure space, $E \in \mathcal{S}$, and $f: X \to [\infty, \infty]$ is a function such that $\int_E f d\mu$ is defined. Then

$$\left| \int_E f d\mu \right| \leq \mu(E) \sup_E |f| .$$

Proof:

Let $c = \sup_E |f|$. We have

$$
\begin{aligned}
\left| \int_E f d\mu \right| 
    &= \left| \int \chi_E f d\mu \right| \\
    &\leq \int \chi_E |f| d\mu \\
    &\leq \int c \chi_E d\mu \\
    &= c \mu(E)
\end{aligned}
$$

where the second line comes from 3.23, the third line comes from 3.8, and the fourth line comes from 3.15



### 3.26 Bounded Convergence Theorem
Suppose $(X, \mathcal{S}, \mu)$ is a measure space with $\mu(X) < \infty$. Suppose $f_1, f_2, ...$ is a sequence of $\mathcal{S}$-measurable functions from $X$ to $\mathbb{R}$ that converges pointwise on $X$ to a function $f: X \to \mathbb{R}$. If there exists $c \in (0, \infty)$ such that 

$$|f_k(x) \leq c|$$

for all $k \in Z^+$ and all $x \in X$, then

$$\lim_{k \to \infty} \int f_k d\mu = \int f d\mu .$$

Proof:

The function $f$ is $\mathcal{S}$-measurable by 2.48.

Suppose $c$ satisfies the hypothesis of this theorem. Let $\epsilon > 0$. By Egorov's Theorem (2.85), there exists $E \in \mathcal{S}$ such that $\mu(X \setminus E) < \frac{\epsilon}{4c}$ and $f_1, f_2, ...$ converges uniformly to $f$ on $E$. Now

$$
\begin{aligned}
\left| \int f_k d\mu - \int f d\mu \right| 
    &= \left| \int_{X \setminus E} f_k d\mu - \int_{X \setminus E} f d\mu + \int_E (f_k - f) d\mu \right| \\
    &\leq \int_{X \setminus E} |f_k| d\mu + \int_{X \setminus E} |f| d\mu + \int_E |f_k - f| d\mu \\
    &< \frac{\epsilon}{2} + \mu(E) \sup_E |f_k - f|
\end{aligned}
$$

where the last inequality follows from 3.25.

Because $f_1, f_2, ...$ converges uniformly to $f$ on $E$ and $\mu(E) < \infty$, the right side of the inequality above is less than $\epsilon$ for $k$ sufficiently large, which completes the proof.



### 3.27 Definition: almost every
Suppose $(X, \mathcal{S}, \mu)$ is a measure space. A set $E \in \mathcal{S}$ is said to contain $\mu$-almost every element of $X$ if $\mu(X \ E) = 0$. If the measure $\mu$ is clear from the context, then the phrase almost every can be used (abbreviated by some authors to be a.e.).



## Dominated Convergence Theorem

### 3.28 integrals on small sets are small
Suppose $(X, \mathcal{S}, \mu)$ is a measure space, $g: X \to [0, \infty]$ is $\mathcal{S}$-measurable, and $\int g d\mu < \infty$. Then for every $\epsilon > 0$, there exists $\delta > 0$ such that 

$$\int_B g d\mu < \epsilon$$

for every set $B \in \mathcal{S}$ such that $\mu(B) < \delta$.

Proof:

Suppose $\epsilon > 0$. Let $h: X \to [0, \infty)$ be a simple $\mathcal{S}$-measurable function such that $0 \leq h \leq g$ and

$$\int g d\mu - \int h d\mu < \frac{\epsilon}{2}$$

the existence of a function $h$ with these properties follows from 3.9. Let

$$H = \max \\{ h(x): x \in X \\}$$

and let $\delta > 0$ be such that $H \delta < \frac{\epislon}{2}$.

Suppose $B \in \mathcal{S}$ and $\mu(B) < \delta$. Then

$$
\begin{aligned}
\int_B g d\mu 
    &= \int_B (g - h) d\mu + \int_B h d\mu \\
    &\leq (g - h) d\mu + H \mu(B) \\
    &< \frac{\epsilon}{2} + H \delta \\
    &< \epsilon
\end{aligned}
$$

as desired.



### 3.29 integrable functions live mostly on sets of finite measure
Suppose $(X, \mathcal{S}, \mu)$ is a measure space, $g: X \to [0, \infty]$ is $\mathcal{S}$-measurable, and $\int g d\mu < \infty$. Then for every $\epsilon > 0$, there exists $E \in \mathcal{S}$ such that $\mu(E) < \infty$ and

$$\int_{X \ E} g d\mu < \epsilon .$$

Proof:

Suppose $\epsilon > 0$. Let $P$ be an $\mathcal{S}$-partition $A_1, ..., A_m$ of $X$ such that 

$$(3.30) \int g d\mu < \epsilon + \mathcal{L}(g, P)$$

Let $E$ be the union of those $A_j$ such that $\inf_{A_j} f > 0$. Then $\mu(E) < \infty$ (because otherwise we would have $\mathcal{L}(g, P) = \infty$, which contradicts the hypothesis that $\int g d\mu < \infty$). Now

$$
\begin{aligned}
\int_{X \setminus E} g d\mu 
    &= \int g d\mu - \int \chi_E g d\mu \\
    &< (\epsilon + \mathcal{L}(g, P)) - \int \chi_E g d\mu \\
    &\leq (\epsilon + \mathcal{L}(g, P)) - \mathcal{L}(\chi_E g, P) \\
    &= \epsilon 
\end{aligned}
$$

where the second line follows from 3.30, the third line follows from the definition of the integral of a nonnegative function, and the last line holds because $\inf_{A_j} f = 0$ for each $A_j$ not contained in $E$.



Suppose $(X, \mathcal{S}, \mu)$ is a measure space and $f_1, f_2, ...$ is a sequence of $\mathcal{S}$-measurable functions on $X$ such that 

$$\lim_{k \to \infty} f_k(x) = f(x)$$

for every (or almost every) $x \in X$. In general, it is not true that 

$$\lim_{k \to \infty} \int f_k d\mu = \int f d\mu $$

We already have two good theorems about interchanging limits and integrals. However, both of these theorems have restrictive hypotheses.


### 3.31 Dominated Convergence Theorem
Suppose $(X, \mathcal{S}, \mu)$ is a measure space, $f: X \to [-\infty, \infty]$ is $\mathcal{S}$-measurable, and $f_1, f_2, ...$ are $\mathcal{S}$-measurable functions from $X$ to $[-\infty, \infty]$ such that

$$\lim_{k \to \infty} f_k(x) = f(x)$$

for almost every $x \in X$. If there exists an $\mathcal{S}$-measurable function $g: X \to [0, \infty]$ such that 

$$\int g d\mu < \infty$$

and

$$|f_k(x) \leq g(x)|$$

for every $k \in Z^+$ and almost every $x \in X$, then

$$\lim_{k \to \infty} \int f_k d\mu = \int f d\mu .$$



### 3.34 Riemann integrable $\iff$ continuous almost everywhere
Suppose $a < b$ and $f: [a, b] \to \mathbb{R}$ is a bounded function. Then $f$ is Riemann integrable if and only if 

$$|\\{x \in [a, b]: f \text{ is not continuous at } x \\}| = 0$$

Furthermore, if $f$ is Riemann integrable and $\lambda$ denotes Lebesgue measure on $\mathbb{R}$, then $f$ is Lebesgue measurable and 

$$\int_a^b f = \int_{[a, b]} f d\lambda$$


### 3.40 Definition: $\lVert f \rVert_1$, $\mathcal{L}^1(\mu)$
Suppose $(X, \mathcal{S}, \mu)$ is a measure space. If $f: X \to [-\infty, \infty]$ is $\mathcal{S}$-measurable, then the $\mathcal{L}^1$ norm of $f$ is denoted by $\lVert f \rVert_1$ and is defined by

$$\lVert f \rVert_1 = \int |f| d\mu .$$

The Lebesgue space $\mathcal{L}^1(\mu)$ is defined by

$$
\mathcal{L}^1(\mu) = 
    \\{f: f \text{ is an } \mathcal{S} \text{-measurable function from } X \text{ to } \mathbb{R} \text{ and } \lVert f \rVert_1 < \infty \\}
$$


### 3.41 Example
Suppose $(X, \mathcal{S}, \mu)$ is a measure space and $E_1, ..., E_n$ are disjoint subsets of $X$. Suppose $a_1, ..., a_n$ are distinct nonzero real numbers. Then

$$a_1 \chi_{E_1} + ... + a_n \chi_{E_n} \in \mathcal{L}^1(\mu)$$

if and only if $E_k \in \mathcal{S}$ and $\mu(E_k) < \infty$ for all $k \in \\{1, ..., n\\}$. Furthermore, 

$$\lVert a_1 \chi_{E_1} + ... + a_n \chi_{E_n} \rVert_1 = |a_1| \mu(E_1) + ... + |a_n| \mu(E_n) $$


### 3.42 Example
If $\mu$ is counting measure on $\mathbb{Z}^+$ and $x = x_1, x_2, ...$ is a sequence of real numbers (thought of as a function on $\mathbb{Z}^+$), then 

$$\lVert x \rVert_1 = \sum_{k=1}^\infty |x_k|$$

In this case, $\mathcal{L}^1(\mu)$ is often denoted by $l^1$. In other words, $l^1$ is the set of all sequences $x_1, x_2, ...$ of real numbers such that $\sum_{k=1}^\infty |x_k| < \infty$.


### 3.43 properties of the $\mathcal{L}^1$ norm
Suppose $(X, \mathcal{S}, \mu)$ is a measure space ad $f, g \in \mathcal{L}^1(\mu)$. Then 

- $\lVert f \rVert_1 \geq 0$;

- $\lVert f \rVert_1 = 0$ if and only if $f(x) = 0$ for almost every $x \in X$;

- $\lVert cf \rVert_1 = |c| \lVert f \rVert_1$ for all $c \in \mathbb{R}$;

- $\lVert f + g \rVert_1 \leq \lVert f \rVert_1 + \lVert g \rVert_1$.


### 3.44 approximation by simple functions
Suppose $\mu$ is a measure and $f \in \mathcal{L}^1(\mu)$. Then for every $\epsilon > 0$, there exists a simple function $g \in \mathcal{L}^1(\mu)$ such that 

$$\lVert f - g \rVert_1 < \epsilon .$$

Proof:

Suppose $\epsilon > 0$. Then there exist simple functions $g_1, g_2 \in \mathcal{L}^1(\mu)$ such that $0 \leq g_1 \leq f^+$ and $0 \leq g_2 \leq f^-$ and

$$\int (f^+ - g_1) d\mu < \frac{\epsilon}{2}$$

and

$$\int (f^- - g_2) d\mu < \frac{\epsilon}{2}$$

where we have used 3.9 to provide the existence of $g_1, g_2$ with these properties.

Let $g = g_1 - g_2$. Then $g$ is a simple function in $\mathcal{L}^1(\mu)$ and

$$
\begin{aligned}
\lVert f - g \rVert_1 
    &= \lVert (f^+ - g_1) - (f^- - g_2) \rVert_1 \\
    &= \int \left | (f^+ - g_1) - (f^- - g_2) \right| \\
    &= \int (f^+ - g_1) d\mu + \int (f^- - g_2) d\mu \\
    &< \epsilon
\end{aligned}
$$

The third equality follows from the fact that $(f^+ - g_1)$ and $(f^- - g_2)$ have different supports. If $(f^+ - g_1) \geq 0$ then $(f^- - g_2) = 0$, and vice versa.



### 3.45 Definition: $\mathcal{L}^1(\mathbb{R})$, $\lVert f \rVert_1$
- The notation $\mathcal{L}^1(\mathbb{R})$ denotes $\mathcal{L}^1(\lambda)$, where $\lambda$ is Lebesgue measure on either the Borel subsets of $\mathbb{R}$ or the Lebesgue measurable subsets of $\mathbb{R}$.

- When working with $\mathcal{L}^1(\mathbb{R})$, the notation $\lVert f \rVert_1$ denotes the integral of the absolute value of $f$ with respect to Lebesgue measure on $\mathbb{R}$.


### 3.46 Definition: step function 
A step function is a function $g: \mathbb{R} \to \mathbb{R}$ of the form 

$$g = a_1 \chi_{I_1} + ... + a_n \chi_{I_n}$$

where $I_1, ..., I_n$ are intervals of $\mathbb{R}$ and $a_1, ..., a_n$ are nonzero real numbers.


### 3.47 approximation by step functions
Suppose $f \in \mathcal{L}^1(\mathbb{R})$. Then for every $\epsilon > 0$, there exists a step function $g \in \mathcal{L}^1(\mathbb{R})$ such that 

$$\lVert f - g \rVert_1 < \epsilon$$

Proof:



### 3.48 approximation by continuous functions
Suppose $f \in \mathcal{L}^1(\mathbb{R})$. Then for every $\epsilon > 0$, there exists a continuous function $g: \mathbb{R} \to \mathbb{R}$ such that 

$$\lVert f - g \rVert_1 < \epsilon$$

and $\\{x \in \mathbb{R}: g(x) \neq 0\\}$ is a bounded set.
