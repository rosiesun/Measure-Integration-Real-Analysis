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
Suppose $(X, S, \mu)$ is a measure space and $f:  X \rightarrow [0, \infty]$ is an $S$-measurable function. The integral of $f$ with respect to $\mu$, denoted $\int f d \mu$, is defined by

$$\int f d \mu = sup \{L(f, P): P \text{is an} S \text{-partition of} X\} .$$


### 3.4 integral of a characteristic function
Suppose $(X, S, \mu)$ is a measure space and $E \in S$. Then

$$\int \chi_E d \mu = \mu(E) .$$


### 3.7 integral of a simple function
Suppose $(X, S, \mu)$ is a measure space, $E_1, ..., E_n$ are disjoint sets in $S$, and $c_1, ..., c_n \in [0, \infty]$. Then

$$\int (\sum_{k=1}^n c_k \chi_{E_k} d \mu = \sum_{k=1}^n c_k \mu(E_k) .$$


### 3.8 integration is order-preserving
Suppose $(X, S, \mu)$ is a measure space and $f, g: X \rightarrow [0, \infty]$ are $S$-measurable functions such that $f(x) \leq g(x)$ for all $x \in X$. Then $\int f d \mu \leq \int g d \mu$.


### 3.9 integrals via simple functions
Suppose $(X, S, \mu)$ is a measure space and $f: X \rightarrow [0, \infty]$ is $S$-measurable. Then

$$\int f d \mu = sup \{\sum_{j=1}^m c_j \mu(A_j): A_1, ..., A_m \text{are disjoint sets in} S, c_1, ..., c_m \in [0, \infty), f(x) \geq \sum_{j=1}^m c_j \chi_{A_j}(x) \forall x \in X \}$$


