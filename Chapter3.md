Measure Integration Real Analysis - Chapter 3 <br>
Integration
================
Rosie Sun <br>
2026-09-13


# 3A Integration with Respect to a Measure

### 3.1 Definition: S-partition
Suppose $S$ is a $\sigma$-algebra on a set $X$. An $S$-partition of $X$ is a finite collection $A_1, ..., A_m$ of disjoint sets in $S$ such that $A_1 \cup ... \cup A_m = X$.


### 3.2 Definition: lower Lebesgue sum
Suppose $(X, S, \mu)$ is a measure space, $f: X \rightarrow [0, \infty]$ is an $S$-measurable function, and $P$ is an $S$-partition $A_1, ..., A_m$ of $X$. The lower Lebesgue sum $L(f, P)$ is defined by

$$L(f, P) = \sum_{j=1}^m \mu(A_j) inf_{A_j} f .$$


### 3.3 Definition: integral of a nonnegative function
Suppose $(X, S, \mu)$ is a measure space and $f:  X \rightarrow [0, \infty]$ is an $S$-measurable function. The integral of $f$ with respect to $\mu$, denoted $\int f d\mu$, is defined by

$$\int f d\mu = sup \\{L(f, P): P \text{ is an } S \text{-partition of } X \\} .$$


### 3.4 integral of a characteristic function
Suppose $(X, S, \mu)$ is a measure space and $E \in S$. Then

$$\int \chi_E d\mu = \mu(E) .$$


### 3.7 integral of a simple function
Suppose $(X, S, \mu)$ is a measure space, $E_1, ..., E_n$ are disjoint sets in $S$, and $c_1, ..., c_n \in [0, \infty]$. Then

$$\int \left( \sum_{k=1}^n c_k \chi_{E_k} \right) d\mu = \sum_{k=1}^n c_k \mu(E_k) .$$


### 3.8 integration is order-preserving
Suppose $(X, S, \mu)$ is a measure space and $f, g: X \rightarrow [0, \infty]$ are $S$-measurable functions such that $f(x) \leq g(x)$ for all $x \in X$. Then $\int f d\mu \leq \int g d\mu$.


### 3.9 integrals via simple functions
Suppose $(X, S, \mu)$ is a measure space and $f: X \rightarrow [0, \infty]$ is $S$-measurable. Then

$$\int f d\mu = sup \left\\{\sum_{j=1}^m c_j \mu(A_j): A_1, ..., A_m \text{ are disjoint sets in } S, c_1, ..., c_m \in [0, \infty), f(x) \geq \sum_{j=1}^m c_j \chi_{A_j}(x) \forall x \in X \right\\}$$


### 3.11 Monotone Convergence Theorem
Suppose $(X, S, \mu)$ is a measure space and $0 \leq f_1 \leq f_2 \leq ...$ is an increasing sequence of $S$-measurable functions. Define $f: X \rightarrow [0, \infty]$ by

$$f(x) = lim_{k \rightarrow \infty} f_k(x) .$$

Then

$$lim_{k \rightarrow \infty} \int f_k d\mu = \int f d\mu .$$


### 3.13 integral-type sums for simple functions
Suppose $(X, S, \mu)$ is a measure space. Suppose $a_1, ..., a_m, b_1, ..., b_n \in [0, \infty]$ and $A_1, ..., A_m, B_1, ..., B_n \in S$ are such that 

$$\sum_{j=1}^m a_j \chi_{A_j} = \sum_{k=1}^n b_k \chi_{B_k} .$$

Then

$$\sum_{j=1}^m a_j \mu(A_j) = \sum_{k=1}^n b_k \mu(B_k).$$


### 3.15 integral of a linear combination of characteristic functions
Suppose $(X, S, \mu)$ is a measure space, $E_1, ..., E_n \in S$, and $c_1, ..., c_n \in [0, \infty]$. Then

$$\int \left( \sum_{k=1}^n c_k \chi_{E_k} \right) d\mu = \sum_{k=1}^n c_k $$


### 3.16 additivity of integration 
Suppose $(X, S, \mu)$ is a measure space and $f, g: X \rightarrow [0, \infty]$ are $S$-measurable functions. Then

$$\int (f + g) d\mu = \int f d\mu + \int g d\mu .$$


### 3.23 absolute value of integral $\leq$ integral of absolute value
Suppose $(X, S, \mu)$ is a measure space and $f: X \rightarrow [-\infty, \infty]$ is a function such that $\int f d\mu$ is defined. Then

$$\left| \int f d\mu \right| \leq \int |f| d\mu .$$






# 3B Limits of Integrals & Integrals of Limits

### 3.24 Definition: integration on a subset
Suppose $(X, S, \mu)$ is a measure space and $E \in S$. If $f: X \rightarrow [-\infty, \infty]$ is an $S$-measurable function, then $\int_E f d\mu$ is defined by

$$\int_E f d\mu = \int \chi_E f d\mu$$

if the right side of the equation above is defined; otherwise $\int_E f d\mu$ is undefined.


### 3.25 bounding an integral
Suppose $(X, S, \mu)$ is a measure space, $E \in S$, and $f: X \rightarrow [\infty, \infty]$ is a function such that $\int_E f d\mu$ is defined. Then

$$\left| \int_E f d\mu \right| \leq \mu(E) sup_E |f| .$$


### 3.26 Bounded Convergence Theorem
Suppose $(X, S, \mu)$ is a measure space with $\mu(X) < \infty$. Suppose $f_1, f_2, ...$ is a sequence of $S$-measurable functions from $X$ to $R$ that converges pointwise on $X$ to a function $f: X \rightarrow R$. If there exists $c \in (0, \infty)$ such that 

$$|f_k(x) \leq c|$$

for all $k \in Z^+$ and all $x \in X$, then

$$lim_{k \rightarrow \infty} \int f_k d\mu = \int f d\mu .$$


### 3.27 Definition: almost every
Suppose $(X, S, \mu)$ is a measure space. A set $E \in S$ is said to contain $\mu$-almost every element of $X$ if $\mu(X \ E) = 0$. If the measure $\mu$ is clear from the context, then the phrase almost every can be used (abbreviated by some authors to be a.e.).


### 3.28 integrals on small sets are small
Suppose $(X, S, \mu)$ is a measure space, $g: X \rightarrow [0, \infty]$ is $S$-measurable, and $\int g d\mu < \infty$. Then for every $\epsilon > 0$, there exists $\delta > 0$ such that 

$$\int_B g d\mu < \epsilon$$

for every set $B \in S$ such that $\mu(B) < \delta$.


### 3.29 integrable functions live mostly on sets of finite measure
Suppose $(X, S, \mu)$ is a measure space, $g: X \rightarrow [0, \infty]$ is $S$-measurable, and $\int g d\mu < \infty$. Then for every $\epsilon > 0$, there exists $E \in S$ such that $\mu(E) < \infty$ and

$$\int_{X \ E} g d\mu < \epsilon .$$


### 3.31 Dominated Convergence Theorem
Suppose $(X, S, \mu)$ is a measure space, $f: X \rightarrow [-\infty, \infty]$ is $S$-measurable, and $f_1, f_2, ...$ are $S$-measurable functions from $X$ to $[-\infty, \infty]$ such that

$$lim_{k \rightarrow \infty} f_k(x) = f(x)$$

for almost every $x \in X$. If there exists an $S$-measurable function $g: X \rightarrow [0, \infty]$ such that 

$$\int g d\mu < \infty$$

and

$$|f_k(x) \leq g(x)|$$

for every $k \in Z^+$ and almost every $x \in X$, then

$$lim_{k \rightarrow \infty} \int f_k d\mu = \int f d\mu .$$


### 3.40 Definition: $\lvert f \rvert_1$, $L^1(\mu)$
Suppose $(X, S, \mu)$ is a measure space. If $f: X \rightarrow [-\infty, \infty]$ is $S$-measurable, then the $L^1$ norm of $f$ is denoted by $\lvert f \rvert_1$ and is defined by

$$\lvert f \rvert_1 = \int |f| d\mu .$$

The Lebesgue space $L^1(\mu)$ is defined by

$$L^1(\mu) = \\{f: f \text{ is an } S \text{-measurable function from } X \text{ to } R \text{ and } \lvert f \rvert_1 < \infty \\}$$


### 3.43 properties of the $L^1$ norm
Suppose $(X, S, \mu)$ is a measure space ad $f, g \in L^1(\mu)$. Then 

- $\lvert f \rvert_1 \geq 0$;

- $\lvert f \rvert_1 = 0$ if and only if $f(x) = 0$ for almost every $x \in X$;

- $\lvert cf \rvert_1 = |c| \lvert f \rvert_1$ for all $c \in R$;

- $\lvert f + g \rvert_1 \leq \lvert f \rvert_1 + \lvert g \rvert_1$.


### 3.44 approximation by simple functions
Suppose $\mu$ is a measure and $f \in L^1(\mu)$. Then for every $\epsion > 0$, there exists a simple function $g \in L^1(\mu)$ such that 

$$\lvert f - g \rvert_1 < \epsilon .$$


### 3.45 Definition: $L^1(R)$, $\lvert f \rvert_1$
- The notation $L^1(R)$ denotes $L^1(\lambda)$, where $\lambda$ is Lebesgue measure on either the Borel subsets of $R$ or the Lebesgue measurable subsets of $R$.

- When working with $L^1(R)$, the notation $\lvert f \rvert_1$ denotes the integral of the absolute value of $f$ with respect to Lebesgue measure on $R$.


### 3.46 Definition: step function 
A step function is a function $g: R \rightarrow R$ of the form 

$$g = a_1 \chi_{I_1} + ... + a_n \chi_{I_n}$$

where $I_1, ..., I_n$ are intervals of $R$ and $a_1, ..., a_n$ are nonzero real numbers.


### 3.47 approximation by step functions
Suppose $f \in L^1(R)$. Then for every $\epsilon > 0$, there exists a step function $g \in L^1(R)$ such that 

$$\lvert f - g \rvert_1 < \epsilon$$


### 3.48 approximation by continuous functions
Suppose $f \in L^1(R)$. Then for every $\epsilon > 0$, there exists a continuous function $g: R \rightarrow R$ such that 

$$\lvert f - g \rvert_1 < \epsilon$$

and $\\{x \in R: g(x) \neq 0\\}$ is a bounded set.
