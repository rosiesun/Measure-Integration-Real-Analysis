Measure Integration Real Analysis - Chapter 7 <br>
$L^p$ Spaces
================
Rosie Sun <br>
2026-09-30


# 7A $\mathcal{L}^p(\mu)$

### 7.1 Definition: $\lVert f \rVert_p$
Suppose $(X, \mathcal{S}, \mu)$ is a measure space, $0 < p < \infty$, and $f: X \to F$ is $\mathcal{S}$-measurable. Then the p-norm of $f$ is denoted by $\lVert f \rVert_p$ and is defined by

$$\lVert f \rVert_p = \left( \int |f|^p d\mu \right)^{1/p} .$$

Also, $\lVert f \rVert_\infty$, which is called the essential supremum of $f$, is defined by

$$\lVert f \rVert = inf \\{ t > 0: \mu(\\{x \in X: |f(x)| > t\\}) = 0 \\} .$$


### 7.2 Example: $p$-norm for counting measure



### 7.3 Definition: $\mathcal{L}^p(\mu)$
Suppose $(X, \mathcal{S}, \mu)$ is a measure space and $0 < p \leq \infty$. The Lebesgue space $\mathcal{L}^p(\mu)$, sometimes denoted $\mathcal{L}^p(X, \mathcal{S}, \mu)$, is defined to be the set of $\mathcal{S}$-measurable functions $f: X \to F$ such that $\lVert f \rVert_p < \infty$.


### 7.5 $\mathcal{L}^p(\mu)$ is a vector space
Suppose $(X, \mathcal{S}, \mu)$ is a measure space and $0 < p < \infty$. Then

$$\lVert f + g \rVert_p^p \leq 2^p (\lVert f \rVert_p^p + \lVert g \rVert_p^p)$$

and

$$\lVert \alpha f \rVert_p = |\alpha| \lVert f \rVert_p$$

for all $f, g \in \mathcal{L}^p(\mu)$ and all $\alpha \in F$. Furthermore, with the usual operations of addition and scalar multiplication of functions, $\mathcal{L}^p(\mu)$ is a vector space.

Proof:

Suppose $f, g \in \mathcal{L}^p(\mu)$. If $x \in X$, then 

$$
\begin{aligned}
|f(x) + g(x)|^p 
    &\leq (|f(x)| + |g(x)|)^p \\
    &\leq (2 max \\{ |f(x)|, |g(x)| \\})^p \\
    &\leq 2^p (|f(x)|^p + |g(x)|^p) 
\end{aligned}
$$

Integrating 