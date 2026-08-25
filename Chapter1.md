Measure Integration Real Analysis - Chapter 1 <br>
Riemann Integration
================
Rosie Sun <br>
2026-08-24



# 1A Review: Riemann Integral

### 1.1 Definition: partition
Suppose $a, b \in R$ with $a < b$. A partition of $[a, b]$ is a finite list of the form $x_0, x_1, ..., x_n$, where 

$$a = x_0 < x_1 < ... < x_n = b.$$



### 1.2 Definition: notation for infimum and supremum of a function
If $f$ is a real-valued function and $A$ is a subset of the domain of $f$, then 

$$inf_A f = inf \\{f(x): x \in A \\}, sup_A f = sup \\{f(x): x \in A \\} .$$



### 1.3 Definition: lower and upper Riemann sums
Suppose $f: [a, b] \rightarrow R$ is a bounded function and $P$ is a partition $x_0, ..., x_n$ of $[a, b]$. The lower Riemann sum $L(f, P, [a, b])$ and the upper Riemann sum $U(f, P, [a, b])$ are defined by

$$L(f, P, [a, b]) = \sum_{j=1}^n (x_j - x_{j-1}) inf_{[x_{j-1}, x_j]} f$$

and

$$U(f, P, [a, b]) = sum_{j=1}^n (x_j - x_{j-1}) sup_{[x_{j-1}, x_j]} f .$$



### 1.5 Inequalities with Riemann sums
Suppose $f: [a, b] \rightarrow R$ is a bounded function and $P, P'$ are partitions of $[a, b]$ such that the list defining $P$ is a sublist of the list defining $P'$. Then

$$L(f, P, [a, b]) \leq L(f, P', [a, b]) \leq U(f, P', [a, b]) \leq U(f, P, [a, b]).$$



### 1.6 lower Riemann sums $\leq$ upper Riemann sums
Suppose $f: [a, b] \rightarrow R$ is a bounded function and $P, P'$ are partitions of $[a, b]$. Then

$$L(f, P, [a, b]) \leq U(f, P, [a, b]) .$$



### 1.7 Definition: lower and upper Riemann integrals
Suppose $f: [a, b] \rightarrow R$ is a bounded function. The lower Riemann integral $L(f, [a, b])$ and the upper Riemann integral $U(f, [a, b])$ of $f$ are defined by

$$L(f, [a, b]) = sup_P L(f, P, [a, b])$$

and

$$U(f, [a, b]) = inf_P U(f, P, [a, b]),$$

where the supremum and infimum above are taken over all partitions $P$ of $[a, b]$.



### 1.8 lower Riemann integral $\leq$ upper Riemann integral
Suppose $f: [a, b] \rightarrow R$ is a bounded function. Then

$$L(f, [a, b]) \leq U(f, [a, b]) .$$



### 1.9 Definition: Riemann integrable; Riemann integral
A bounded function on a closed bounded interval is called Riemann integrable if its lower Riemann integral equals its upper Riemann integral.

If $f: [a, b] \rightarrow R$ is Riemann integrable, then the Riemann integral $\int_a^b f$ is defined by 

$$\int_a^b f = L(f, [a, b]) = U(f, [a, b]) .$$



### 1.11 continuous functions are Riemann integrable
Every continuous real-valued function on each closed bounded interval is Riemann integrable.



### 1.13 bounds on Riemann integral
Suppose $f: [a, b] \rightarrow R$ is Riemann integrable. Then

$$(b - a) inf_{[a, b]} f \leq \int_a^b f \leq (b - a) sup_{[a, b]} f .$$





# 1B Riemann Integral Is Not Good Enough

