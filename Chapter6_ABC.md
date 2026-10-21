Measure Integration Real Analysis - Chapter 6 <br>
Banach Spaces
================
Rosie Sun <br>
2026-08-24


# 6A Metric Spaces

## Open Sets, Closed Sets, and Continuity

### 6.1 Definition: metric space
A metric on a nonempty set $V$ is a function $d: V \times V \to [0, \infty)$ such that 

- $d(f, f) = 0$ for all $f \in V$;

- if $f, g \in V$ and $d(f, g) = 0$, then $f = g$;

- $d(f, g) = d(g, f)$ for all $f, g \in V$;

- $d(f, h) \leq d(f, g) + d(g, h)$ for all $f, g, h \in V$;

A metric space is a pair $(V, d)$, where $V$ is a nonempty set and $d$ is a metric on $V$.


### 6.2 Example: metric spaces
- Suppose $V$ is a nonempty set. Define $d$ on $V \times V$ by setting $d(f, g)$ to be 1 if $f \neq g$ and to be 0 if $f = g$. Then $d$ is a metric on $V$.

- Define $d$ on $\mathbb{R} \times \mathbb{R}$ by $d(x, y) = |x - y|$. Then $d$ is a metric on $\mathbb{R}$.

- For $n \in \mathbb{Z}^+$, define $d$ on $\mathbb{R}^n \times \mathbb{R}^n$ by

$$d((x_1, ..., x_n), (y_1, ..., y_n)) = \max \\{|x_1 - y_1|, ..., |x_n - y_n| \\}$$

Then $d$ is a metric on $\mathbb{R}^n$.

- Define $d$ on $C([0, 1]) \times C([0, 1])$ by 

$$d(f, g) = \sup \\{|f(t) - g(t)|: t \in [0, 1] \\}$$

here $C([0, 1])$ is the set of continuous real-valued functions on $[0, 1]$. Then $d$ is a metric on $C([0, 1])$. 

- Define $d$ on $l^1 \times l^1$ by 

$$d((a_1, a_2, ...), (b_1, b_2, ...)) = \sum_{k=1}^\infty |a_k - b_k|$$

Here $l^1$ is the set of sequences $(a_1, a_2, ...)$ of real numbers such that $\sum_{k=1}^\infty |a_k| < \infty$. Then $d$ is a metric on $l^1$.


### 6.3 Definition: open ball
Suppose $(V, d)$ is a metric space, $f \in V$, and $r > 0$. 

- The open ball centered at $f$ with radius $r$ is denoted $B(f, r)$ and is defined by

$$B(f, r) = \\{g \in V: d(f, g) < r \\}$$

- The closed ball centered at $f$ with radius $r$ is denoted $\overline{B}(f, r)$ and is defined by

$$\overline{B}(f, r) = \\{g \in V: d(f, g) \leq r \\}$$


### 6.4 Definition: open set
A subset $G$ of a metric space $V$ is called open if for every $f \in G$, there exists $r > 0$ such that $B(f, r) \subset G$.


### 6.5 open balls are open
Suppose $V$ is a metric space, $f \in V$, and $r > 0$. Then $B(f, r)$ is an open subset of $V$.



### 6.6 Definition: closed subset
A subset of a metric space $V$ is called closed if its complement in $V$ is open.


### 6.7 Definition: closure
Suppose $V$ is a metric space and $E \subset V$. The closure of $E$, denoted $\overline{E}$, is defined by

$$\overline{E} = \\{g \in V: B(g, \epsilon) \bigcap E \neq \emptyset \text{ for every } \epsion > 0\\}$$


### 6.8 Definition: limit in $V$
Suppose $(V, d)$ is a metric space, $f_1, f_2, ...$ is a sequence in $V$, and $f \in V$. Then

$$\lim_{k \to \infty} f_k = f \text{ means } \lim_{k \to \infty} d(f_k, f) = 0$$


### 6.9 closure
Suppose $V$ is a metric space and $E \subset V$. Then

(a) $\overline{E} = \\{g \in V: \text{ there exist } f_1, f_2, ... \in E \text{ such that } \lim_{k \to \infty} f_k = g \\}$;

(b) $\overline{E}$ is the intersection of all closed subsets of $V$ that contain $E$;

(c) $\overline{E}$ is a closed subset of $V$;

(d) $E$ is closed if and only if $\overline{E} = E$;

(e) $E$ is closed if and only if $E$ contains the limit of every convergent sequence of elements of $E$.


### 6.10 Definition: continuity
Suppose $(V, d_V)$ and $(W, d_W)$ are metric spaces and $T: V \to W$ is a function. 

- For $f \in V$, the function $T$ is called continuous at $f$ if for every $\epsilon > 0$, there exists $\delta > 0$ such that 

$$d_W(T(f), T(g)) < \epsilon$$

for all $g \in V$ with $d_V(f, g) < \delta$.

- The function $T$ is called continuous if $T$ is continuous at $f$ for every $f \in V$.


### 6.11: equivalent conditions for continuity
Suppose $V$ and $W$ are metric spaces and $T: V \to W$ is a function. Then the following are equivalent:

(a) $T$ is continuous.

(b) $\lim_{k \to \infty} f_k = f$ implies $\lim_{k \to \infty} T(f_k) = T(f)$ in $W$.

(c) $T^{-1}(G)$ is an open subset of $V$ for every open set $G \subset W$.

(d) $T^{-1}(F)$ is a closed subset of $V$ for every closed set $F \subset W$. 


## Cauchy Sequences and Completeness

### 6.12 Definition: Cauchy sequence
A sequence $f_1, f_2, ...$ in a metric space $(V, d)$ is called. Cauchy sequence if for every $\epsilon > 0$, there exists $n \in \mathbb{Z}^+$ such that $d(f_j, f_k) < \epsilon$ for all integers $j \geq n$ and $k \geq n$.


### 6.13 every convergent sequence is a Cauchy sequence
Every convergent sequence in a metric space is a Cauchy sequence.


### 6.14 Definition: complete metric space
A metric space $V$ is called complete if every Cauchy sequence in $V$ converges to some element of $V$.


### 6.16 connection between complete and closed
(a) A complete subset of a metric space is closed.

(b) A closed subset of a complete metric space is complete.





# 6B Vector Spaces

## Integration of Complex-Valued Functions

### 6.17 Definition: complex numbers
- A complex number is an ordered pair $(a, b)$, where $a, b \in \mathbb{R}$, but we write this as $a + bi$.

- The set of all complex numbers is denoted by $\mathbb{C}$:

$$\mathbb{C} = \\{a + bi: a, b \in mathbb{R} \\}$$

- Addition and multiplication on $\mathbb{C}$ are defined by

$$(a + bi) + (c + di) = (a + c) + (b + d)i$$

$$(a + bi) (c + di) = (ac - bd) + (ad + bc)i$$

here $a, b, c, d \in \mathbb{R}$.


### 6.18 Definition: $\Re z$; $\Im z$; absolute value; limits
Suppose $z = a + bi$, where $a$ and $b$ are real numbers.

- The real part of $z$, denoted $\Re z$, is defined by $\Re z = a$.

- The imaginary part of $z$, denoted $\Im z$, is defined by $\Im z = b$.

- The absolute value of $z$, denoted $|z|$, is defined by $|z| = \sqrt{a^2 + b^2}$.

- If $z_1, z_2, ... \in \mathbb{C}$ and $L \in \mathbb{C}$, then $\lim_{k \to \infty} z_k = L$ means $\lim_{k \to \infty} |z_k - L| = 0$. 


### 6.19 Definition: measurable complex-valued function
Suppose $(X, \mathcal{S})$ is a measurable space. A function $f: X \to \mathbb{C}$ is called $\mathcal{S}$-measurable if $\Re f$ and $\Im f$ are both $\mathcal{S}$-measurable functions.


### 6.20 $|f|^p$ is measurable if $f$ is measurable
Suppose $(X, \mathcal{S})$ is a measurable space, $f: X \to \mathbb{C}$ is an $\mathcal{S}$-measurable function, and $0 < p < \infty$. Then $|f|^p$ is an $\mathcal{S}$-measurable function.


### 6.21 Definition: integral of a complex-valued function
Suppose $(X, \mathcal{S}, \mu)$ is a measure space and $f: X \to \mathbb{C}$ is an $\mathcal{S}$-measurable function with $\int |f| d\mu < \infty$ [the collection of such functions is denoted $\mathcal{L}^1(\mu)$]. Then $\int f d\mu$ is defined by

$$\int f d\mu = \int (\Re f) d\mu + i \int (\Im f) d\mu$$


### 6.22 bound on the absolute value of an integral
Suppose $(X, \mathcal{S}, \mu)$ is a measure space and $f: X \to \mathbb{C}$ is an $\mathcal{S}$-measurable function such that $\int |f| d\mu < \infty$. Then

$$\left| \int f d\mu \right| \leq \int |f| d\mu$$


### 6.23 Definition: complex conjugate
Suppose $z \in \mathbb{C}$. The complex conjugate of $z \in \mathbb{C}$, denoted $\overline{z}$, is defined by

$$\overline{z} = \Re z - (\Im z) i$$


### 6.24 properties of complex conjugates
Suppose $w, z \in \mathbb{C}$. Then

- product of $z$ and $\overline{z}$
$$z \overline{z} = |z|^2$$

- sum and difference of $z$ and $\overline{z}$
$$z + \overline{z} = 2 \Re z$$

$$z - \overline{z} = 2 (\Im z) i$$

- additivity and multiplicativity of complex conjugate
$$\overline{w + z} = \overline{w} + \overline{z}$$

$$\overline{wz} = \overline{w} \overline{z}$$

- complex conjugate of complex conjugate
$$\overline{\overline{z}} = z$$

- absolute value of complex conjugate
$$|\overline{z}| = |z|$$

- integral of complex conjugate of a function
$$\int \overline{f} d\mu = \overline{\int f d\mu} \text{ for every measure } \mu \text{ and every } f \in \mathcal{L}^1(\mu)$$



## Vector Spaces and Subspaces

### 6.25 Definition: $\mathbb{F}$
From now on, $\mathbb{F}$ stands for either $\mathbb{R}$ or $\mathbb{C}$.


### 6.26 Definition: addition; scalar multiplication
- An addition on a set $V$ is a function that assigns an element $f + g \in V$ to each pair of elements $f, g \in V$.

- A scalar multiplication on a set $V$ is a function that assigns an element $\alpha f \in V$ to each $\alpha \in \mathbb{F}$ and each $f \in V$. 


### 6.27 Definition: vector space
A vector space (over $\mathbb{F}$) is a set $V$ along with an addition on $V$ and a scalar multiplication on $V$ such that the following properties hold:

- commutativity
$f + g = g + f$ for all $f, g \in V$;

- associativity
$(f + g) + h = f + (g + h)$ and $(\alpha \beta) f = \alpha (\beta f)$ for all $f, g, h \in V$ and $\alpha, \beta \in \mathbb{F}$;

- additive identity
there exists an element $0 \in V$ such that $f + 0 = f$ for all $f \in V$;

- additive inverse
for every $f \in V$, there exists $g \in V$ such that $f + g = 0$;

- multiplicative identity
$1f = f$ for all $f \in V$;

- distributive properties
$\alpha (f + g) = \alpha f + \alpha g$ and $(\alpha + \beta) f = \alpha f + \beta f$ for all $\alpha, \beta \in \mathbb{F}$ and $f, g \in V$.


### 6.28 Example: the vector space $\mathbb{F}^X$
Suppose $X$ is a nonempty set. Let $\mathbb{F}^X$ denote the set of functions from $X$ to $\mathbb{F}$. Addition and scalar multiplication on $\mathbb{F}^X$ are defined as expected: for $f, g \in \mathbb{F}^X$ and $\alpha \in \mathbb{F}$, define

$$(f + g)(x) = f(x) + g(x)$$

$$(\alpha f)(x) = \alpha (f(x))$$

for $x \in X$. Then $\mathbb{F}^X$ is a vector space; the additive identity in this vector space is the function $0 \in \mathbb{F}^X$ defined by $0(x) = 0$ for all $x \in X$.


### 6.29 Example: $\mathbb{F}^n$; $\mathbb{F}^{\mathbb{Z}^+}$
Special case of the previous example: if $n \in \mathbb{Z}^+$ and $X = \\{1, ..., n\\}$, then $\mathbb{F}^X$ is the familiar space $\mathbb{R}^n$ or $\mathbb{C}^n$.

Another special case: $\mathbb{F}^{\mathbb{Z}^+}$ is the vector space of all sequences of real numbers or complex numbers.


### 6.30 Definition: subspace
A subset $U$ of $V$ is called a subspace of $V$ if $U$ is also a vector space (using the same addition and scalar multiplication as on $V$).


### 6.31 conditions for a subspace
A subset $U$ of $V$ is a subspace of $V$ if and only if $U$ satisfies the following three conditions:

- additive identity
$0 \in U$;

- closed under addition
$f, g \in U$ implies $f + g \in U$;

- closed under scalar multiplication
$\alpha \in \mathbb{F}$ and $f \in U$ implies $\alpha f \in U$.


### 6.32 Example: subspaces of $\mathbb{F}^X$
- The set $C([0, 1])$ of continuous real-valued functions on $[0, 1]$ is a vector space over $\mathbb{R}$ because the sum of two continuous functions is continuous and a constant multiple of a continuous function is continuous. In other words, $C([0, 1])$ is a subspace of $\mathbb{R}^{[0, 1]}$.

- Suppose $(X, \mathcal{S})$ is a measurable space. Then the set of $\mathcal{S}$-measurable functions from $X$ to $\mathbb{F}$ is a subspace of $\mathbb{F}^X$ because the sum of two $\mathcal{S}$-measurable functions is $\mathcal{S}$-measurable and a constant multiple of an $\mathcal{S}$-measurable function is $\mathcal{S}$-measurable.

- Suppose $(X, \mathcal{S}, \mu)$ is a measure space. Then the set $\mathcal{Z}(\mu)$ of $\mathcal{S}$-measurable functions $f$ from $X$ to $\mathbb{F}$ such that $f = 0$ almost everywhere [meaning that $\mu(\\{x \in X: f(x) \neq 0\\}) = 0$] is a vector space over $\mathbb{F}$ because the union of two sets with $\mu$-measure 0 is a set with $\mu$-measure 0 [which implies that $\mathcal{Z}(\mu)$ is closed under addition]. Note that $\mathcal{Z}(\mu)$ is a subspace of $\mathbb{F}^X$.

- Suppose $(X, \mathcal{S})$ is a measurable space. Then the set of bounded measurable functions from $X$ to $\mathbb{F}$ is a subspace of $\mathbb{F}^X$ because the sum of two bounded $\mathcal{S}$-measurable functions is a bounded $\mathcal{S}$-measurable function and a constant multiple of a bounded $\mathcal{S}$-measurable function is a bounded $\mathcal{S}$-measurable function.

- Suppose $(X, \mathcal{S}, \mu)$ is a measure space. Then the set of $\mathcal{S}$-measurable functions $f$ from $X$ to $\mathbb{F}$ such that $\int f d\mu = 0$ is a subspace of $\mathbb{F}^X$ because of standard properties of integration.

- Suppose $(X, \mathcal{S}, \mu)$ is a measure space. Then the set $\mathcal{L}^1(\mu)$ of $\mathcal{S}$-measurable functions from $X$ to $\mathbb{F}$ such that $\int |f| d\mu < \infty$ is a subspace of $\mathcal{F}^X$. The set $\mathcal{L}^1(\mu)$ is closed under addition and scalar multiplication because 

$$\int |f + g| d\mu \leq \int |f| d\mu + \int |g| d\mu$$

and

$$\int |\alpha f| d\mu = |\alpha| \int |f| d\mu$$

- The set $l^1$ of all sequences $(a_1, a_2, ...)$ of elements of $F$ such that $\sum_{k=1}^\infty a_k < \infty$ is a subspace of $\mathbb{F}^{\mathbb{Z}^+}$. Note that $l^1$ is a special case of the example in the previous bullet point (take $\mu$ to be counting measure on $\mathbb{Z}^+$).





# 6C Normed Vector Spaces

## Norms and Complete Norms

### 6.33 Definition: norm, normed vector space
A norm on a vector space $V$ (over $\mathbb{F}$) is a function $\lVert \cdot \rVert: V \to [0, \infty)$ such that 

- $\lVert f \rVert = 0$ if and only if $f = 0$ (positive definite);

- $\lVert \alpha f \rVert = |\alpha| \lVert f \rVert$ for all $\alpha \in \mathbb{F}$ and $f \in V$ (homogeneity);

- $\lVert f + g \rVert \leq \lVert f \rVert + \lVert g \rVert$ for all $f, g \in V$ (triangle inequality).

A normed vector space is a pair $(V, \lVert \cdot \rVert)$, where $V$ is a vector space and $\lVert \cdot \rVert$ is a norm on $V$.


### 6.34 Example: norms
- Suppose $n \in \mathbb{Z}^+$. Define $\lVert \cdot \rVert_1$ and $\lVert \cdot \rVert_\infty$ on $\mathbb{F}^n$ by

$$\lVert (a_1, ..., a_n) \rVert_1 = |a_1| + ... + |a_n|$$

and

$$\lVert (a_1, ..., a_n) \rVert_\infty = \max \\{|a_1|, ..., |a_n|\\}$$

Then $\lVert \cdot \rVert_1$ and $\lVert \cdot \rVert_\infty$ are norms on $\mathbb{F}^n$.

- On $l^1$, define $\lVert \cdot \rVert_1$ by

$$\lVert (a_1, a_2, ...) \rVert_1 = \sum_{k=1}^\infty |a_k|$$

Then $\lVert \cdot \rVert_1$ is a norm on $l^1$.

- Suppose $X$ is a nonempty set and $b(X)$ is the subspace of $\mathbb{F}^X$ consisting of the bounded functions from $X$ to $\mathbb{F}$. For $f$ a bounded function from $X$ to $\mathbb{F}$, define $\lVert f \rVert$ by

$$\lVert f \rVert = \sup \\{|f(x)|: x \in X\\}$$

Then $\lVert \cdot \rVert$ is a norm on $b(X)$.

- Let $C([0, 1])$ denote the vector space of continuous functions from the interval [0, 1] to $\mathbb{F}$. Define $\lVert \cdot \rVert$ on $C([0, 1])$ by 

$$\lVert f \rVert = \int_0^1 |f|$$

Then $\lVert \cdot \rVert$ is a norm on $C([0, 1])$.


### 6.35 Example: not norms
- Let $\mathcal{L}^1(\mathbb{R})$ denote the vector space of Borel (or Lebesgue) measurable functions $f: \mathbb{R} \to \mathbb{F}$ such that $\int |f| d\lambda < \infty$, whwere $\lambda$ is Lebesgue measure on $\mathbb{R}$. Define $\lVert \cdot \rVert_1$ on $\mathcal{L}^1(\mathbb{R})$ by

$$\lVert f \rVert_1 = \int |f| d\lambda$$

Then $\lVert \cdot \rVert$ satisfies the homogeneity condition and the triangle inequality on $\mathcal{L}^1(\mathbb{R})$. However, $\lVert \cdot \rVert_1$ is not a norm on $\mathcal{L}^1(\mathbb{R})$ because the positive definite condition is not satisfied. 

Specifically, if $E$ is a nonempty Borel subset of $\mathbb{R}$ with Lebesgue measure 0 (for example, $E$ might consist of a single element of $\mathbb{R}$), then $\lVert \chi_E \rVert_1 = 0$ but $\chi_E \neq 0$.

- If $n \in \mathbb{Z}^+$ and $\lVert \cdot \rVert$ is defined on $\mathbb{F}^n$ by

$$\lVert (a_1, ..., a_n) \rVert = |a_1|^{1/2} + ... + |a_n|^{1/2}$$

then $\lVert \cdot \rVert$ satisfies the positive definite condition and the triangle inequality. However, $\lVert \cdot \rVert$ as defined above is not a norm because it does not satisfy the homogeneity condition.

- If $\lVert \cdot \rVert_{1/2}$ is defined on $\mathbb{F}^n$ by

$$\lVert (a_1, ..., a_n) \rVert_{1/2} = (|a_1|^{1/2} + ... + |a_n|^{1/2})^2$$

then $\lVert \cdot \rVert_{1/2}$ satisfies the positive definite condition and the homogeneity condition. However, if $n > 1$ then $\lVert \cdot \rVert_{1/2}$ is not a norm on $\mathbb{F}^n$ because the triangle inequality is not satisfied.


### 6.36 normed vector spaces are metric spaces
Suppose $(V, \lVert \cdot \rVert)$ is a normed vector space. Define $d: V \times V \to [0, \infty)$ by

$$d(f, g) = \lVert f - g \rVert$$

Then $d$ is a metric on $V$.


### 6.37 Definition: Banach space
A complete normed vector space is called a Banach space.


### 6.38 Example: Banach spaces
- The vector space $C([0, 1])$ with the norm defined by 

$$\lVert f \rVert = \sup_{[0, 1]} |f|$$

is a Banach space.

- The vector space $l^1$ with the norm defined by 

$$\lVert (a_1, a_2, ...) \rVert_1 = \sum_{k=1}^\infty |a_k|$$

is a Banach space.


### 6.39 Example: not a Banach space
- The vector space $C([0, 1])$ with the norm defined by 

$$\lVert f \rVert = \int_0^1 |f|$$

is not a Banach space.

- The vector space $l^1$ with the norm defined by

$$\lvert (a_1, a_2, ...) \rVert_\infty = \sup_{k \in \mathbb{Z}^+} |a_k|$$

is not a Banach space.


### 6.40 Definition: infinite sum in a normed vector space
Suppose $g_1, g_2, ...$ is a sequence in a normed vector space $V$. Then $\sum_{k=1}^\infty g_k$ is defined by

$$\sum_{k=1}^\infty g_k = \lim_{n \to \infty} \sum_{k=1}^n g_k$$

if this limit exists, in which case the infinite series is said to converge.


### 6.41
Suppose $V$ is a normed vector space. Then $V$ is a Banach space if and only if $\sum_{k=1}^\infty g_k$ converges for every sequence $g_1, g_2, ...$ in $V$ such that $\sum_{k=1}^\infty \lVert g_k \rVert < \infty$.



## Bounded Linear Maps

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

- The set of bounded linear maps from $V$ to $W$ is denoted $\mathcal{B}(V, W)$.


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


### 6.46 $\lVert \cdot \rVert$ is a norm on $\mathcal{B}(V, W)$
Suppose $V$ and $W$ are normed vector spaces. Then 

$$\lVert S + T \rVert \leq \lVert S \rVert + \lVert T \rVert$$

and 

$$\lVert \alpha T \rVert = |\alpha| \lVert T \rVert$$

for all $S, T \in \mathcal{B}(V, W)$ and all $\alpha \in F$. Furthermore, the function $\lVert \cdot \rVert$ is a norm on $\mathcal{B}(V, W)$.


### 6.47 $\mathcal{B}(V, W)$ is a Banach space if $W$ is a Banach space
Suppose $V$ is a normed vector space and $W$ is a Banach space. Then $\mathcal{B}(V, W)$ is a Banach space.


### 6.48 continuity is equivalent to boundedness for linear maps
A linear map from one normed vector space to another normed vector space is continuous if and only if it is bounded.

