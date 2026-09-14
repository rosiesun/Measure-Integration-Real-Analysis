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
b - a & \text{if $I = (a, b)$ for some $a, b \in R$ with $a < b$} \\
0 & \text{if $I = \emptyset$} \\
\infty & \text{if $I = (-\infty, a)$ or $I = (a, \infty)$ for some $a \in R$} \\
\infty & \text{if $I = (-\infty, \infty)$}
\end{cases}
$$


### 2.2 Definition: outer measure
The outer measure $|A|$ of a set $A \subset R$ is defined by

$$|A| = 
\text{
    inf $\{\sum_{k=1}^\infty l(I_k): I_1, I_2, ...$ are open intervals such that $A \subset \cup_{k=1}^\infty I_k$ \} 
    }
$$


### 2.4 countable sets have outer measure 0
Every countable subset of $R$ has outer measure 0.


### 2.5 outer measure preserves order
Suppose $A$ and $B$ are subsets of $R$ with $A \subset B$. Then $|A| \leq |B|$.


### 2.6 Definition: translation
If $t \in R$ and $A \in R$, then the translation $t + A$ is defined by

$$t + A = \{ t + a: a \in A \} .$$


### 2.7 outer measure is translation invariant
Suppose $t \in R$ and $a \in R$. Then $|t + A| = |A| .$


### 2.8 countable subadditivity of outer measure
Suppose $A_1, A_2, ...$ is a sequence of subsets of $R$. Then

$$|\cup_{k=1}^\infty A_k| \leq \sum_{k=1}^\infty |A_k| .$$


### 2.10 Definition: open cover
Suppose $A \subset R$.

- A collection $C$ of open subsets of $R$ is called an open cover of $A$ if $A$ is contained in the union of all the sets in $C$.

- An open cover $C$ of $A$ is said to have a finite subcover if $A$ is contained in the union of some finite list of sets in $C$.


### 2.12 Heine-Borel Theorem
Every open cover of a closed bounded subset of $R$ has a finite subcover.

Proof:

Suppose $F$ is a closed bounded subset of $R$ and $C$ is an open cover of $F$.

First consider the case where $F = [a, b]$ for some $a, b \in R$ with $a < b$. Thus $C$ is an open cover of $[a, b]$. Let

$$D = \\{d \in [a, b]: [a, d] has a finite subcover from C \\} .$$


### 2.14 outer measure of a closed interval
Suppose $a, b \in R$, with $a < b$. Then $|[a, b]| = b - a$.


### 2.17 nontrivial intervals are uncountable
Every interval in $R$ that contains at least two distinct elements is uncountable.


### 2.18 nonadditivity of outer measure
There exist disjoint subsets $A$ and $B$ of $R$ such that 

$$|A \cup B| \neq |A| + |B|.$$





# 2B Measurable Spaces and Functions

### 2.22 nonexistence of extension of length to all subsets of $R$
There does not exist a function $\mu$ with all the following properties:

(a) $\mu$ is a function from the set of subsets of $R$ to $[0, \infty]$.

(b) $\mu(I) = l(I)$ for every open interval $I$ of $R$.

(c) $\mu(\cup_{k=1}^\infty A_k) = \sum_{k=1}^\infty \mu(A_k)$ for every disjoint sequence $A_1, A_2$, ... of subsets of $R$.

(d) $\mu(t + A) = \mu(A)$ for every $A \subset R$ and every $t \in R$.


### 2.23 Definition: $\sigma$-algebra
Suppose $X$ is a set and $S$ is a set of subsets of $X$. Then $S$ is called a $\sigma$-algebra on $X$ if the following three conditions are satisfied:

- $\emptyset \in S$;

- if $E \in S$, then $X \ E \in S$;

- if $E_1, E_2$, ... is a sequence of elements of $S$, then $\cup_{k=1}^\infty E_k \in S$.


### 2.25 $\sigma$-algebras are closed under countable intersection
Suppose $S$ is a $\sigma$-algebra on a set $X$. Then

(a) $X \in S$;

(b) if $D, E \in S$, then $D \cup E \in S$ and $D \cap E \in S$ and $D \ E \in S$;

(c) if $E_1, E_2$, ... is a sequence of elements of $S$, then $\cap_{k=1}^\infty E_k \in S$.


### 2.26 Definition: measurable space; measurable set
- A measurable space is an ordered pair $(X, S)$, where $X$ is a set and $S$ is a $\sigma$-algebra on $X$.

- An element of $S$ is called an $S$-measurable set, or just a measurable set if $S$ is clear from the context.


### 2.27 smallest $\sigma$-algebra containing a collection of subsets
Suppose $X$ is a set and $A$ is a set of subsets of $X$. Then the intersection of all $\sigma$-algebras on $X$ that contain $A$ is a $\sigma$-algebra on $X$.


### 2.29 Definition: Borel set
The smallest $\sigma$-algebra on $R$ containing all open subsets of $R$ is called the collection of Borel subsets of $R$. An element of this $\sigma$-algebra is called a Borel set.


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

### 2.48 limit of $S$-measurable functions



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

### 2.67 existence of a subset of $R$ that is not a Borel set

### 2.68 outer measure is a measure on Borel sets


### 2.69 Definition: Lebesgue measure
Lebesgue measure is the measure on $(R, B)$, where $B$ is the $\sigma$-algebra of Borel subsets of $R$, that assigns to each Borel set its outer measure.


### 2.70 Definition: Lebesgue measurable set

### 2.71 equivalences for being a Lebesgue measurable set

### 2.72 outer measure is a measure on Lebesgue measurable sets

### 2.73 Definition: Lebesgue measure




# 2E Convergence of Measurable Functions

### 2.82 Definition: pointwise convergence; uniform convergence
Suppose $X$ is a set, $f_1, f_2$, ... is a sequence of functions from $X$ to $R$, and $f$ is a function from $X$ to $R$.

- The sequence $f_1, f_2$, ... converges pointwise on $X$ to $f$ if

$$lim_{k \rightarrow \infty} f_k (x) = f(x)$$

for each $x \in X$.

In other words, $f_1, f_2$, ... converges pointwise on $X$ to $f$ if for each $x \in X$ and every $\epsilon > 0$, there exists $n \in Z^+$ such that $|f_k(x) - f(x)| < \epsilon$ for all integers $k \geq n$.

- The sequence $f_1, f_2$ ... converges uniformly on $X$ to $f$ if for every $\epsilon > 0$, there exists $n \in Z^+$ such that $|f_k(x) - f(x)| < \epsilon$ for all integers $k \geq n$ and all $x \in X$.


### 2.84


### 2.88 Definition: simple function
A function is called simple if it takes on only finitely many values.


### 2.89 approximation by simple functions
Suppose $(X, S)$ 