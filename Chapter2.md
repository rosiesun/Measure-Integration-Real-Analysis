Measure Integration Real Analysis - Chapter 2 <br>
Measures
================
Rosie Sun <br>
2026-09-05


# 2A Outer Measure on \mathbb{R}

## Motivation and Definition of Outer Measure

### 2.1 Definition: length of open interval
The length $l(I)$ of an open interval $I$ is defined by

$$
l(I) =
\begin{cases}
    b - a & \text{ if } 
        I = (a, b) \text{ for some } a, b \in \mathbb{R} \text{ with } a < b \\
    
    0 & \text{ if } 
        I = \emptyset \\

    \infty & \text{ if } 
        I = (-\infty, a) \text{ or } I = (a, \infty) \text{ for some } a \in \mathbb{R} \\

    \infty & \text{ if } 
        I = (-\infty, \infty)
\end{cases}
$$


### 2.2 Definition: outer measure
The outer measure $|A|$ of a set $A \subset \mathbb{R}$ is defined by

$$
|A| = \inf
    \left\\{
        \sum_{k=1}^\infty l(I_k): 
            I_1, I_2, ... \text{ are open intervals such that } 
            A \subset \bigcup_{k=1}^\infty I_k
    \right\\} 
$$


The definition of outer measure involves an infinite sum. The infinite sum $\sum_{k=t}^\infty t_k$ of a sequence $t_1, t_2, ...$ of elements of $[0, \infty]$ is defined to be $\infty$ if some $t_k = \infty$. Otherwise, $\sum_{k=1}^\infty t_k$ is defined to be the limit (possibly $\infty$) of the increasing sequence $t_1, t_1 + t_2, t_1 + t_2 + t_3, ...$ of partial sums; thus

$$\sum_{k=1}^\infty t_k = \lim_{n \to \infty} \sum_{k=1}^n t_k$$


### 2.3 Example finite sets have outer measure 0
Suppose $A = \\{a_1, ..., a_n\\}$ is a finite set of real numbers. Suppose $\epsilon > 0$. Define a sequence $I_1, I_2, ...$ of open intervals by

$$
I_k = 
\begin{cases}
    (a_k - \epsilon, a_k + \epsilon) & \text{ if } k \leq n \\
    \emptyset & \text{ if } k > n
\end{cases}
$$

Then $I_1, I_2, ...$ is a sequence of open intervals whose union contains $A$. Clearly 

$$\sum_{k=1}^\infty l(I_k) = 2 \epsilon n$$

Hence $|A| \leq 2 \epsilon n$. Because $\epsilon$ is an arbitrary positive number, this implies that $|A| = 0$.



### 2.4 countable sets have outer measure 0
Every countable subset of $\mathbb{R}$ has outer measure 0.


### 2.5 outer measure preserves order
Suppose $A$ and $B$ are subsets of $\mathbb{R}$ with $A \subset B$. Then $|A| \leq |B|$.


### 2.6 Definition: translation
If $t \in \mathbb{R}$ and $A \in \mathbb{R}$, then the translation $t + A$ is defined by

$$t + A = \{ t + a: a \in A \} .$$


### 2.7 outer measure is translation invariant
Suppose $t \in \mathbb{R}$ and $a \in \mathbb{R}$. Then $|t + A| = |A| .$


### 2.8 countable subadditivity of outer measure
Suppose $A_1, A_2, ...$ is a sequence of subsets of $\mathbb{R}$. Then

$$|\bigcup_{k=1}^\infty A_k| \leq \sum_{k=1}^\infty |A_k| .$$


### 2.10 Definition: open cover
Suppose $A \subset \mathbb{R}$.

- A collection $C$ of open subsets of $\mathbb{R}$ is called an open cover of $A$ if $A$ is contained in the union of all the sets in $C$.

- An open cover $C$ of $A$ is said to have a finite subcover if $A$ is contained in the union of some finite list of sets in $C$.


### 2.12 Heine-Borel Theorem
Every open cover of a closed bounded subset of $\mathbb{R}$ has a finite subcover.

Proof:

Suppose $F$ is a closed bounded subset of $\mathbb{R}$ and $C$ is an open cover of $F$.

First consider the case where $F = [a, b]$ for some $a, b \in \mathbb{R}$ with $a < b$. Thus $C$ is an open cover of $[a, b]$. Let

$$D = \\{d \in [a, b]: [a, d] \text{ has a finite subcover from } C \\} .$$



### 2.14 outer measure of a closed interval
Suppose $a, b \in \mathbb{R}$, with $a < b$. Then $|[a, b]| = b - a$.


### 2.17 nontrivial intervals are uncountable
Every interval in $\mathbb{R}$ that contains at least two distinct elements is uncountable.


### 2.18 nonadditivity of outer measure
There exist disjoint subsets $A$ and $B$ of $\mathbb{R}$ such that 

$$|A \cup B| \neq |A| + |B|.$$





# 2B Measurable Spaces and Functions

### 2.22 nonexistence of extension of length to all subsets of $\mathbb{R}$
There does not exist a function $\mu$ with all the following properties:

(a) $\mu$ is a function from the set of subsets of $\mathbb{R}$ to $[0, \infty]$.

(b) $\mu(I) = l(I)$ for every open interval $I$ of $\mathbb{R}$.

(c) $\mu(\cup_{k=1}^\infty A_k) = \sum_{k=1}^\infty \mu(A_k)$ for every disjoint sequence $A_1, A_2$, ... of subsets of $\mathbb{R}$.

(d) $\mu(t + A) = \mu(A)$ for every $A \subset \mathbb{R}$ and every $t \in \mathbb{R}$.


### 2.23 Definition: $\sigma$-algebra
Suppose $X$ is a set and $\mathcal{S}$ is a set of subsets of $X$. Then $\mathcal{S}$ is called a $\sigma$-algebra on $X$ if the following three conditions are satisfied:

- $\emptyset \in \mathcal{S}$;

- if $E \in \mathcal{S}$, then $X \ E \in \mathcal{S}$;

- if $E_1, E_2$, ... is a sequence of elements of $\mathcal{S}$, then $\cup_{k=1}^\infty E_k \in \mathcal{S}$.


### 2.25 $\sigma$-algebras are closed under countable intersection
Suppose $\mathcal{S}$ is a $\sigma$-algebra on a set $X$. Then

(a) $X \in \mathcal{S}$;

(b) if $D, E \in \mathcal{S}$, then $D \cup E \in \mathcal{S}$ and $D \cap E \in \mathcal{S}$ and $D \ E \in \mathcal{S}$;

(c) if $E_1, E_2$, ... is a sequence of elements of $\mathcal{S}$, then $\cap_{k=1}^\infty E_k \in \mathcal{S}$.


### 2.26 Definition: measurable space; measurable set
- A measurable space is an ordered pair $(X, \mathcal{S})$, where $X$ is a set and $\mathcal{S}$ is a $\sigma$-algebra on $X$.

- An element of $\mathcal{S}$ is called an $\mathcal{S}$-measurable set, or just a measurable set if $\mathcal{S}$ is clear from the context.


### 2.27 smallest $\sigma$-algebra containing a collection of subsets
Suppose $X$ is a set and $A$ is a set of subsets of $X$. Then the intersection of all $\sigma$-algebras on $X$ that contain $A$ is a $\sigma$-algebra on $X$.


### 2.29 Definition: Borel set
The smallest $\sigma$-algebra on $\mathbb{R}$ containing all open subsets of $\mathbb{R}$ is called the collection of Borel subsets of $\mathbb{R}$. An element of this $\sigma$-algebra is called a Borel set.


### 2.30 Example: Borel sets
- Every closed subset of $\mathbb{R}$ is a Borel set because every closed subset of $\mathbb{R}$ is the complement of an open subset of $\mathbb{R}$.

- Every countable subset of $\mathbb{R}$ is a Borel set because if $B = \\{x_1, x_2, ...\\}$, then $B = \cup_{k=1}^\infty \\{x_k\\}$, which is a Borel set because each $\\{x_k\\}$ is a closed set.

- Every half-open interval $[a, b)$ where $a, b \in mathbb{R}$ is a Borel set because 

$$[a, b) = \bigcap_{k=1}^\infty (a - \frac{1}{k}, b) .$$

- If $f: \mathbb{R} \to \mathbb{R}$ is a function, then the set of points at which $f$ is continuous is the intersection of a sequence of open sets and thus is a Borel set. 


### 2.31 Definition: inverse image
If $f: X \rightarrow Y$ is a function and $A \subset Y$, then the set $f^{-1}(A)$ is defined by

$$f^{-1}(A) = \\{x \in X: f(x) \in A\\} .$$


### 2.33 algebra of inverse images
Suppose $f: X \rightarrow Y$ is a function. Then

(a) $f^{-1}(Y \ A) = X \ f^{-1}(A)$ for every $A \subset Y$;

(b) $f^{-1}(\cup_{E \in A} E) = \cup$


### 2.34 inverse image of composition



## Measurable Functions

### 2.35 Definition: measurable function
Suppose $(X, \mathcal{S})$ is measurable space. A function $f: X \to \mathbb{R}$ is called $\mathcal{S}$-measurable (or just measurable if $\mathcal{S}$ is clear from the context) if $f^{-1}(B) \in \mathcal{S}$ for every Borel set $B \in \mathbb{R}$.


### 2.37 Definition: characteristic function
Suppose $E$ is a subset of a set $X$. The characteristic function of $E$ is the function $\chi_E: X \to \mathbb{R}$ defined by

$$
\chi_E(x) =
\begin{cases}
    1 & \text{ if } x \in E \\
    0 & \text{ if } x \notin E
\end{cases}
$$


Note that if $f: X \to \mathbb{R}$ is a function and $a \in \mathbb{R}$, then 

$$f^{-1}((a, \infty)) = \\{x \in X: f(x) > a\\} .$$


### 2.39 condition for measurable function
Suppose $(X, \mathcal{S})$ is a measurable space and $f: X \to \mathbb{R}$ is a function such that 

$$f^{-1}((a, \infty)) \in \mathcal{S}$$

for all $a \in \mathbb{R}$. Then $f$ is an $\mathcal{S}$-measurable function.

Proof:

Let 

$$\mathcal{T} = \\{A \in \mathbb{R}: f^{-1}(A) \in \mathcal{S} \\} .$$

We want to show that every Borel subset of $\mathbb{R}$ is in $\mathcal{T}$. To do this, we will first show that $\mathcal{T}$ is a $\sigma$-algebra on $\mathbb{R}$.

Certainly $\emptyset \in \mathcal{T}$, because $f^{-1}(\emptyset) = \emptyset \in \mathcal{S}$. 

If $A \in \mathcal{T}$, then $f^{-1}(A) \in \mathcal{S}$; hence

$$f^{-1}(\mathbb{R} \setminus A) = X \setminus f^{-1}(A) \in \mathcal{S}$$

by 2.33(a), and thus $R \setminus A \in \mathcal{T}$. In other words, $\mathcal{T}$ is closed under complementation. 

If $A_1, A_2, ... \in \mathcal{T}$, then $f^{-1}(A_1), f^{-1}(A_2), ... \in \mathcal{S}$; hence

$$f^{-1} \left(\bigcup_{k=1}^\infty A_k \right) = \bigcup_{k=1}^\infty f^{-1}(A_k) \in \mathcal{S}$$

by 2.33(b), and thus $\cup_{k=1}^\infty A_k \in \mathcal{T}$. In other words, $\mathcal{T}$ is closed under countable unions. 

Thus $\mathcal{T}$ is a $\sigma$-algebra on $\mathbb{R}$ by 2.23.

By hypothesis, $\mathcal{T}$ contains $\\{(a, \infty): a \in \mathbb{R} \\} .$ Because $\mathcal{T}$ is closed under complementation, $\mathcal{T}$ also contains $\\{(-\infty, b]: b \in \mathbb{R} \\}$. Because $\mathcal{T}$ is closed under finite intersections by 2.25, we see that $\mathcal{T}$ contains $\\{(a, b]: a, b \in mathbb{R} \\}$. 

Because

$$(a, b) = \bigcup_{k=1}^\infty \left(a, b - \frac{1}{k} \right]$$

and

$$(-\infty, b) = \bigcup_{k=1}^\infty \left(-k, b - \frac{1}{k} \right]$$

and $\mathcal{T}$ is closed under countable unions, we can conclude that $\mathcal{T}$ contains every open subset of $\mathbb{R}$.

Thus the $\sigma$-algebra $\mathcal{T}$ contains the smallest $\sigma$-algebra on $\mathbb{R}$ that contains all open subsets of $\mathbb{R}$. In other words, $\mathcal{T}$ contains every Borel subset of $\mathbb{R}$. Thus $f$ is an $\mathcal{S}$-measurable function.



### 2.40 Definition: Borel measurable function
Suppose $X \subset \mathbb{R}$. A function $f: X \to \mathbb{R}$ is called Borel measurable if $f^{-1}(B)$ is a Borel set for every Borel set $B \subset \mathbb{R}$. 


### 2.41 every continuous function is Borel measurable
Every continuous real-valued function defined on a Borel subset of $\mathbb{R}$ is a Borel measurable function.

Proof:

Suppose $X \subset \mathbb{R}$ is a Borel set and $f: X \to \mathbb{R}$ is continuous. To prove that $f$ is Borel measurable, fix $a \in \mathbb{R}$.

If $x \in X$ and $f(x) > a$, then by the continuity of $f$, there exists $\delta_x > 0$ such that $f(y) > a$ for all $y \in (x - \delta_x, x + \delta_x) \bigcap X$. Thus

$$f^{-1}((a, \infty)) = \left ( \bigcup_{x \in f^{-1}((a, \infty))} (x - \delta_x, x + \delta_x) \right) \bigcap X$$

The union inside the large parentheses above is an open subset of $\mathbb{R}$; hence its intersection with $X$ is a Borel set. Thus we can conclude that $f^{-1}((a, \infty))$ is a Borel set.

Now 2.39 implies that $f$ is a Borel measurable function.



### 2.42 Definition: increasing function



### 2.43 every increasing function is Borel measurable
Every increasing function defined on a Borel subset of $\mathbb{R}$ is a Borel measurable function.

Proof:

Suppose $X \subset \mathbb{R}$ is a Borel set and $f: X \to \mathbb{R}$ is increasing. To prove that $f$ is Borel measurable, fix $a \in \mathbb{R}$.

Let $b = \inf f^{-1}((a, \infty))$. Then it is easy to see that 

$$f^{-1}((a, \infty)) = (b, \infty) \bigcap X$$

or

$$f^{-1}((a, \infty)) = [b, \infty) \bigcap X .$$

Either way, we can conclude that $f^{-1}((a, \infty))$ is a Borel set.

Now 2.39 implies that $f$ is a Borel measurable function.



### 2.44 composition of measurable functions
Suppose $(X, \mathcal{S})$ is a measurable space and $f: X \to \mathbb{R}$ is an $\mathcal{S}$-measurable function. Suppose $g$ is a real-valued Borel measurable function defined on a subset of $\mathbb{R}$ that includes the range of $f$. Then $g \cir f: X \to R$ is an $\mathcal{S}$-measurable function.

Proof:

Suppose $B \subset \mathbb{R}$ is a Borel set. Then by 2.34, 

$$(g \circ f)^{-1}(B) = f^{-1}(g^{-1}(B)) .$$

Because $g$ is a Borel measurable function, $g^{-1}(B)$ is a Borel subset of $\mathbb{R}$. Because $f$ is an $\mathcal{S}$-measurable function, $f^{-1}(g^{-1}(B)) \in \mathcal{S}$. 

Thus the equation above implies that $(g \circ f)^{-1}(B) \in \mathcal{S}$. Thus $g \circ f$ is an $\mathcal{S}$-measurable function.



### 2.46 algebraic operations with measurable functions
Suppose $(X, \mathcal{S})$ is a measurable space and $f, g: X \to \mathcal{R}$ are $\mathcal{S}$-measurable. Then

(a) $f+g$, $f-g$, and $fg$ are $\mathcal{S}$-measurable functions;

(b) if $g(x) \neq 0$ for all $x \in X$, then $\frac{f}{g}$ is an $\mathcal{S}$-measurable function.

Proof:

(a)

Suppose $a \in \mathbb{R}$. We will show that

$$(2.47) \quad (f+g)^{-1}((a, \infty)) = \bigcup_{r \in \mathbb{Q}} \left( f^{-1}((r, \infty)) \bigcap g^{-1}((a - r, \infty)) \right)$$

which implies that $(f+g)^{-1}((a, \infty)) \in \mathcal{S}$.

To prove 2.47, first suppose 

$$x \in (f+g)^{-1}((a, \infty)) .$$

Thus $f(x) + g(x) > a$. Hence the open interval $(a - g(x), f(x))$ is nonempty, and thus it contains some rational number $r$. 

This implies that $f(x) > r$, which means that $x \in f^{-1}((r, \infty))$; and $a - g(x) < r$, or $g(x) > a-r$, which implies that $x \in g^{-1}((a-r, \infty))$. We have 

$$x \in f^{-1}((r, \infty)) \bigcap g^{-1}((a-r, \infty)) .$$

Thus $x$ is an element of the right side of 2.47, completing the proof that 

$$(f+g)^{-1}((a, \infty)) \subseteq \bigcup_{r \in \mathbb{Q}} \left( f^{-1}((r, \infty)) \bigcap g^{-1}((a - r, \infty)) \right)$$

To prove the inclusion in the other direction, suppose 

$$x \in f^{-1}((r, \infty)) \bigcap g^{-1}((a-r, \infty))$$

for some $r \in \mathbb{Q}$. Thus we have

$$f(x) > r \text{ and } g(x) > a - r .$$

Adding these two inequalities, we see that $f(x) + g(x) > a$. Thus $x \in (f+g)^{-1}((a, \infty))$, completing the proof of 2.47. 

Hence $f + g$ is an $\mathcal{S}$-measurable function.

Example 2.45 tells us that $-g$ is an $\mathcal{S}$-measurable function. Thus $f - g$, which equals $f + (-g)$ is an $\mathcal{S}$-measurable function.

The easiest way to prove that $fg$ is an $\mathcal{S}$-measurable function uses the equation 

$$fg = \frac{(f + g)^2 - f^2 - g^2}{2}$$

The operation of squaring an $\mathcal{S}$-measurable function produces an $\mathcal{S}$-measurable function, as does the operation of multiplication by $\frac{1}{2}$. Thus the equation above implies that $fg$ is an $\mathcal{S}$-measurable function, completing the proof of (a).

(b)

Suppose $g(x) \neq 0$ for all $x \in X$. 

The function defined on $\mathbb{R} \setminus \\{0\\}$ (a Borel subset of $\mathbb{R}$) that takes $x$ to $\frac{1}{x}$ is continuous and thus is a Borel measurable function by 2.41. Now 2.44 implies that $\frac{1}{g}$ is an $\mathcal{S}$-measurable function. 

Combining this result with what we have already proved about the product of $\mathcal{S}$-measurable functions, we conclude that $\frac{f}{g}$ is an $\mathcal{S}$-measurable function, proving (b).



### 2.48 limit of $\mathcal{S}$-measurable functions
Suppose $(X, \mathcal{S})$ is a measurable space and $f_1, f_2, ...$ is a sequence of $\mathcal{S}$-measurable functions from $X$ to $\mathbb{R}$. Suppose $\lim_{k \to \infty} f_k(x)$ exists for each $x \in X$. Define $f: X \to \mathbb{R}$ by

$$f(x) = \lim_{k \to \infty} f_k(x) .$$

Then $f$ is an $\mathcal{S}$-measurable function.

Proof:

Suppose $a \in \mathbb{R}$. We will show that 

$$
(2.49) \quad 
f^{-1}((a, \infty)) = 
    \bigcup_{j=1}^\infty \bigcup_{m=1}^\infty \bigcap_{k=m}^\infty f_k^{-1} 
        \left((a + \frac{1}{j}, \infty) \right)
$$

which implies that $f^{-1}((a, \infty)) \in \mathcal{S}$.

First suppose $x \in f^{-1}((a, \infty))$. Thus there exists $j \in \mathbb{Z}^+$ such that $f(x) > a + \frac{1}{j}$. 

The definition of limit now implies that there exists $m \in \mathbb{Z}^+$ such that $f_k(x) > a + \frac{1}{j}$ for all $k \geq m$. Thus x is in the right side of 2.49, and

$$
f^{-1}((a, \infty)) \subseteq 
    \bigcup_{j=1}^\infty \bigcup_{m=1}^\infty \bigcap_{k=m}^\infty 
        f_k^{-1} \left((a + \frac{1}{j}, \infty) \right)
$$

To prove the inclusion in the other direction, suppose 

$$
x \in \bigcup_{j=1}^\infty \bigcup_{m=1}^\infty \bigcap_{k=m}^\infty 
    f_k^{-1} \left((a + \frac{1}{j}, \infty) \right)
$$

Thus there exist $j, m \in \mathbb{Z}^+$ such that $f_k(x) > a + \frac{1}{j}$ for all $k \geq m$. 

Taking the limit as $k \to \infty$, we see that $f(x) \geq a + \frac{1}{j} > a$. Thus $x \in f^{-1}((a, \infty)$, completing the proof of 2.49.

Thus $f$ is an $\mathcal{S}$-measurable function.





# 2C Measures and Their Properties

### 2.54 Definition: measure
Suppose $X$ is a set and $\mathcal{S}$ is a $\sigma$-algebra on $X$. A measure on $(X, \mathcal{S})$ is a function $\mu: \mathcal{S} \to [0, \infty]$ such that $\mu(\emptyset) = 0$ and 

$$\mu \left( \bigcup_{k=1}^\infty E_k \right) = \sum_{k=1}^\infty \mu(E_k) $$

for every disjoint sequence $E_1, E_2, ...$ of sets in $\mathcal{S}$.


### 2.56 Definition: measure space
A measure space is an ordered triple $(X, \mathcal{S}, \mu)$, where $X$ is a set, $\mathcal{S}$ is a $\sigma$-algebra on $X$, and $\mu$ is a measure on $(X, \mathcal{S})$.


### 2.57 measure preserves order; measure of a set difference
Suppose $(X, \mathcal{S}, \mu)$ is a measure space and $D, E \in \mathcal{S}$ are such that $D \subset E$. Then

(a) $\mu(D) \leq \mu(E)$;

(b) $\mu(E \setminus D) = \mu(E) - \mu(D)$ provided that $\mu(D) < \infty$.

Proof:


### 2.58 countable subadditivity
Suppose $(X, \mathcal{S}, \mu)$ is a measure space and $E_1, E_2, ... \in \mathcal{S}$. Then

$$\mu \left( \bigcup_{k=1}^\infty E_k \right) \leq \sum_{k=1}^\infty \mu(E_k) .$$


### 2.59 measure of an increasing union
Suppose $(X, \mathcal{S}, \mu)$ is a measure space and $E_1 \subset E_2 \subset ...$ is an increasing sequence of sets in $\mathcal{S}$. Then

$$\mu \left( \bigcup_{k=1}^\infty E_k \right) = \lim_{k \to \infty} \mu(E_k) .$$


### 2.60 measure of a decreasing intersection
Suppose $(X, \mathcal{S}, \mu)$ is a measure space and $E_1 \supset E_2 \supset ...$ is a decreasing sequence of sets in $\mathcal{S}$, with $\mu(E_1) < \infty$. Then

$$\mu \left(\bigcap_{k=1}^\infty E_k \right) = \lim_{k \to \infty} \mu(E_k) .$$


### 2.61 measure of a union
Suppose $(X, \mathcal{S}, \mu)$ is a measure space and $D, E \in \mathcal{S}$, with $\mu(D \cap E) < \infty$. Then

$$\mu(D \cup E) = \mu(D) + \mu(E) - \mu(D \cap E) .$$






# 2D Lebesgue Measure

### 2.62 additivity of outer measure if one of the sets is open

### 2.63 additivity of outer measure if one of the sets is closed

### 2.65 approximation of Borel sets from below by closed sets

### 2.66 additivity of outer measure if one of the sets is a Borel set

### 2.67 existence of a subset of $\mathbb{R}$ that is not a Borel set

### 2.68 outer measure is a measure on Borel sets


### 2.69 Definition: Lebesgue measure
Lebesgue measure is the measure on $(\mathbb{R}, B)$, where $B$ is the $\sigma$-algebra of Borel subsets of $\mathbb{R}$, that assigns to each Borel set its outer measure.


### 2.70 Definition: Lebesgue measurable set

### 2.71 equivalences for being a Lebesgue measurable set

### 2.72 outer measure is a measure on Lebesgue measurable sets

### 2.73 Definition: Lebesgue measure




# 2E Convergence of Measurable Functions

### 2.82 Definition: pointwise convergence; uniform convergence
Suppose $X$ is a set, $f_1, f_2$, ... is a sequence of functions from $X$ to $\mathbb{R}$, and $f$ is a function from $X$ to $\mathbb{R}$.

- The sequence $f_1, f_2$, ... converges pointwise on $X$ to $f$ if

$$\lim_{k \to \infty} f_k (x) = f(x)$$

for each $x \in X$.

In other words, $f_1, f_2$, ... converges pointwise on $X$ to $f$ if for each $x \in X$ and every $\epsilon > 0$, there exists $n \in \mathbb{Z}^+$ such that $|f_k(x) - f(x)| < \epsilon$ for all integers $k \geq n$.

- The sequence $f_1, f_2$ ... converges uniformly on $X$ to $f$ if for every $\epsilon > 0$, there exists $n \in \mathbb{Z}^+$ such that $|f_k(x) - f(x)| < \epsilon$ for all integers $k \geq n$ and all $x \in X$.


### 2.84 uniform limit of continuous functions is continuous
Suppose $B \subset \mathbb{R}$ and $f_1, f_2, ...$ is a sequence of functions from $B$ to $\mathbb{R}$ that converges uniformly on $B$ to a function $f: B \to \mathbb{R}$. Supopse $b \in B$ and $f_k$ is continuous at $b$ for each $k \in \mathbb{Z}^+$. Then $f$ is continuous at $b$.

Proof:


### 2.85 Egorov's Theorem
Suppose $(X, \mathcal{S}, \mu)$ is a measure space with $\mu(X) < \infty$. Suppose $f_1, f_2, ...$ is a sequence of $\mathcal{S}$-measurable functions from $X$ to $\mathbb{R}$ that converges pointwise on $X$ to a function $f: X \to \mathbb{R}$. Then for every $\epsilon > 0$, there exists a set $E \in \mathcal{S}$ such that $\mu(X \setminus E) < \epsilon$ and $f_1, f_2, ...$ converges uniformly to $f$ on $E$.

Proof:


### 2.88 Definition: simple function
A function is called simple if it takes on only finitely many values.

Suppose $(X, \mathcal{S})$ is a measurable space, $f: X \to \mathbb{R}$ is a simple function, and $c_1, ..., c_n$ are the distinct nonzero values of $f$. Then

$$f = c_1 \chi_{E_1} + ... + c_n \chi_{E_n} $$

where $E_k = f^{-1}(\\{c_k\\})$. Thus this function $f$ is an $\mathcal{S}$-measurable function if and only if $E_1, ..., E_n \in \mathcal{S}$.


### 2.89 approximation by simple functions
Suppose $(X, \mathcal{S})$ is a measure space and $f: X \to [-\infty, \infty]$ is $\mathcal{S}$-measurable. Then there exists a sequence $f_1, f_2, ...$ of functions from $X$ to $\mathbb{R}$ such that

(a) each $f_k$ is a simple $\mathcal{S}$-measurable function;

(b) $|f_k(x)| \leq |f_{k+1}(x)| \leq |f(x)|$ for all $k \in \mathbb{Z}^+$ and all $x \in X$;

(c) $lim_{k \to \infty} f_k(x) = f(x)$ for every $x \in X$;

(d) $f_1, f_2, ...$ converges uniformly on $X$ to $f$ if $f$ is bounded.

Proof:

The idea of the proof is that for each $k \in \mathbb{Z}^+$ and $n \in \mathbb{Z}$, the interval $[n, n+1)$ is divided into $2^k$ equally sized half-open subintervals. 

If $f(x) \in [0, k)$, we define $f_k(x)$ to be the left endpoint of the subinterval into which $f(x)$ falls; if $f(x) \in (-k, 0)$, we define $f_k(x)$ to be the right endpoint of the subinterval into which $f(x)$ falls; and if $|f(x)| \geq k$, we define $f_k(x)$ to be $\plusminus k$. Specifically, let

$$
f_k(x) =
\begin{cases}
    \frac{m}{2^k} & \text{ if } 0 \leq f(x) < k \text{ and } m \in mathbb{Z} \text{ is such that } f(x) \in [\frac{m}{2^k}, \frac{m+1}{2^k}) \\
    \frac{m+1}{2^k} & \text{ if } -k < f(x) < 0 \text{ and } m \in mathbb{Z} \text{ is such that } f(x) \in [\frac{m}{2^k}, \frac{m+1}{2^k}) \\
    k & \text{ if } f(x) \geq k \\
    -k & \text{ if } f(x) \leq -k
\end{cases}
$$

Each 

$$f^{-1}([\frac{m}{2^k}, \frac{m+1}{2^k})) \in \mathcal{S}$$

because $f$ is an $\mathcal{S}$-measurable function. Thus each $f_k$ is an $\mathcal{S}$-measurable simple function; in other words, (a) holds.

Also, (b) holds because of how we have defined $f_k$.

The definition of $f_k$ implies that 

$$(2.90) |f_k(x) - f(x)| \leq \frac{1}{2^k} \forall x \in X \text{ such that } f(x) \in [-k, k]$$

Thus we see that (c) holds.

Finally 2.90 shows that (d) holds.



### 2.91 Luzin's Theorem
Suppose $g: \mathbb{R} \to \mathbb{R}$ is a Borel measurable function. Then for every $\epsilon > 0$, there exists a closed set $F \subset \mathbb{R}$ such that $|R \setminus F| < \epsilon$ and $g|_F$ is a continuous function on $F$.

Proof:



### 2.93 Luzin's Theorem, second version
Suppose $E \subset \mathbb{R}$ and $g: E \to \mathbb{R}$ is a Borel measurable function. Then for every $\epsilon > 0$, there exists a closed set $F \subset E$ and a continuous function $h: \mathbb{R} \to \mathbb{R}$ such that $|E \setminus F| < \epsilon$ and $h|_F = g|_F$.
