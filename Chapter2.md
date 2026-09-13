Measure Integration Real Analysis - Chapter 2 <br>
Measures
================
Rosie Sun <br>
2026-09-05


# 2A Outer Measure on R

### 2.1 Definition: length of open interval
The length $l(I)$ of an open interval $I$ is defined by

$$
l(I) =
\begin{cases}
b - a & \text{if $I = (a, b)$ for some $a, b \in \mathbf{R}$ with $a < b$} \\
0 & \text{if $I = \emptyset$} \\
\infty & \text{if $I = (-\infty, a)$ or $I = (a, \infty)$ for some $a \in mathbb{R}$} \\
\infty & \text{if $I = (-\infty, \infty)$}
\end{cases}
$$


### 2.2 Definition: outer measure
The outer measure $|A|$ of a set $A \subset \mathbf{R}$ is defined by

$$|A| = \text{inf $\{\sum_{k=1}^\infty l(I_k): I_1, I_2, ...$ are open intervals such that $A \subset \cup_{k=1}^\infty I_k$ \} }.$$


### 2.4 countable sets have outer measure 0
Every countable subset of $\mathbf{R}$ has outer measure 0.


### 2.5 outer measure preserves order



### 2.6 Definition: translation

### 2.7 outer measure is translation invariant

### 2.8 countable subadditivity of outer measure

### 2.10 Definition: open cover


### 2.12 Heine-Borel Theorem
Every open cover of a closed bounded subset of $R$ has a finite subcover.

Proof:

Suppose $F$ is a closed bounded subset of $R$ and $C$ is an open cover of $F$.

First consider the case where $F = [a, b]$ for some $a, b \in R$ with $a < b$. Thus $C$ is an open cover of $[a, b]$. Let

$$D = \\{d \in [a, b]: [a, d] has a finite subcover from C \\} .$$


### 2.14 outer measure of a closed interval


### 2.17 nontrivial intervals are uncountable


### 2.18 nonadditivity of outer measure




# 2B Measurable Spaces and Functions

### 2.22 nonexistence of extension of length to all subsets of $R$

### 2.23 Definition: $\sigma$-algebra

### 2.25 $\sigma$-algebras are closed under countable intersection

### 2.26 Definition: measurable space; measurable set

### 2.27 smallest $\sigma$-algebra containing a collection of subsets

### 2.29 Definition: Borel set

### 2.31 Definition: inverse image

### 2.33 algebra of inverse images

### 2.34 inverse image of composition

### 2.35 Definition: measurable function

### 2.37 Definition: characteristic function

### 2.39 condition for measurable function

### 2.40 Definition: Borel measurable function

### 2.41 every continuous function is Borel measurable

### 2.42 Definition: increasing function

### 2.43 every increasing function is Borel measurable

### 2.44 composition of measurable functions

### 2.46 algebraic operations with measurable functions

### 2.48 limit of $\mathcal{S}$-measurable functions



# 2C Measures and Their Properties

### 2.54 Definition: measure

### 2.56 Definition: measure space

### 2.57 measure preserves order; measure of a set difference

### 2.58 countable subadditivity

### 2.59 measure of an increasing union

### 2.60 measure of a decreasing intersection

### 2.61 measure of a union



# 2D Lebesgue Measure

### 2.62 additivity of outer measure if one of the sets is open

### 2.63 additivity of outer measure if one of the sets is closed

### 2.65 approximation of Borel sets from below by closed sets

### 2.66 additivity of outer measure if one of the sets is a Borel set

### 2.67 existence of a subset of $\mathbb{R}$ that is not a Borel set

### 2.68 outer measure is a measure on Borel sets


### 2.69 Definition: Lebesgue measure
Lebesgue measure is the measure on $(\mathbb{R}, \mathcal{B})$, where $\mathcal{B}$ is the $\sigma$-algebra of Borel subsets of $R$, that assigns to each Borel set its outer measure.


### 2.70 Definition: Lebesgue measurable set

### 2.71 equivalences for being a Lebesgue measurable set

### 2.72 outer measure is a measure on Lebesgue measurable sets

### 2.73 Definition: Lebesgue measure




# 2E Convergence of Measurable Functions

### 2.82 Definition: pointwise convergence; uniform convergence
Suppose $X$ is a set, $f_1, f_2$, ... is a sequence of functions from $X$ to $\mathbb{R}$, and $f$ is a function from $X$ to $\mathbb{R}$.

- The sequence $f_1, f_2$, ... converges pointwise on $X$ to $f$ if

$$lim_{k \rightarrow \infty} f_k (x) = f(x)$$

for each $x \in X$.

In other words, $f_1, f_2$, ... converges pointwise on $X$ to $f$ if for each $x \in X$ and every $\epsilon > 0$, there exists $n \in \mathbb{Z}^+$ such that $|f_k(x) - f(x)| < \epsilon$ for all integers $k \geq n$.

- The sequence $f_1, f_2$ ... converges uniformly on $X$ to $f$ if for every $\epsilon > 0$, there exists $n \in \mathbb{Z}^+$ such that $|f_k(x) - f(x)| < \epsilon$ for all integers $k \geq n$ and all $x \in X$.


### 2.84


### 2.88 Definition: simple function
A function is called simple if it takes on only finitely many values.


### 2.89 approximation by simple functions
Suppose $(X, \mathcal{S})$ 