Measure Integration Real Analysis - Chapter 6 <br>
Banach Spaces
================
Rosie Sun <br>
2026-08-24


# 6C Normed Vector Spaces

### 6.33 Definition: norm, normed vector space

### 6.36 normed vector spaces are metric spaces

### 6.37 Definition: Banach space

### 6.40 Definition: infinite sum in a normed vector space


### 6.42 Definition: linear map
Suppose $V$ and $W$ are vector spaces. A function $T: V \to W$ is called linear if 

- $T(f + g) = Tf + Tg \forall f, g \in V$;

- $T(\alpha f) = \alpha Tf \forall \alpha \in F, f \in V$.

A linear function is often called a linear map.


### 6.43 Definition: bounded linear map; $\lVert T \rVert$; $B(V, W)$
Suppose $V$ and $W$ are normed vector spaces and $T: V \to W$ is a linear map.

- The norm of $T$, denoted $\lVert T \rVert$, is defined by

$$\lVert T \rVert = sup \\{\lVert Tf \rVert : f \in V, \lVert f \rVert \leq 1 \\} .$$

- $T$ is called bounded if $\lVert T \rVert < \infty$.

- The set of bounded linear maps from $V$ to $W$ is denoted $B(V, W)$.


### 6.44 Example: bounded linear map
Let $C([0, 3])$ be the normed vector space of continuous functions from [0, 3] to $F$, with 

$$\lVert f \rVert = sup_{[0, 3]} |f|.$$

Define $T: C([0,3]) \to C([0,3])$ by

$$(Tf)(x) = x^2 f(x) .$$

Then $T$ is a bounded linear map and $\lVert T \rVert = 9$.


### 6.45 Example: linear map that is not bounded
Let $V$ be the normed vector space of sequences $(a_1, a_2, ...)$ of elements of $F$ such that $a_k = 0$ for all but finitely many $k \in Z^+$, with 

$$\lVert (a_1, a_2, ...) \rVert = max_{k \in Z^+} |a_k| .$$

Define $T: V \to V$ by

$$T(a_1, a_2, a_3, ...) = (a_1, 2a_2, 3a_3, ...)$$

Then $T$ is a linear map that is not bounded.


### 6.46 $\lVert \cdot \rVert$ is a norm on $B(V, W)$
Suppose $V$ and $W$ are normed vector spaces. Then 

$$\lVert S + T \rVert \leq \lVert S \rVert + \lVert T \rVert$$

and 

$$\lVert \alpha T \rVert = |\alpha| \lVert T \rVert$$

for all $S, T \in B(V, W)$ and all $\alpha \in F$. Furthermore, the function $\lVert \cdot \rVert$ is a norm on $B(V, W)$.



# 6D Linear Functionals

### 6.53 Definition: family


