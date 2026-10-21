Measure Integration Real Analysis - Chapter 6 <br>
Banach Spaces
================
Rosie Sun <br>
2026-08-24


# 6D Linear Functionals

### 6.49 Definition: linear functional
A linear functional on a vector space $V$ is a linear map from $V$ to $F$.


### 6.50 Example: linear functional
Let $V$ be the vector space of sequences $(a_1, a_2, ...)$ of elements of $F$ such that $a_k = 0$ for all but finitely many $k \in Z^+$. Define $\phi: V \to F$ by

$$\phi(a_1, a_2, ...) = \sum_{k=1}^\infty a_k .$$

Then $\phi$ is a linear functional on $V$.

- If we make $V$ a normed vector space with the norm 

$$\lVert (a_1, a_2, ...) \rVert_1 = \sum_{k=1}^\infty |a_k| ,$$

then $\phi$ is a bounded linear functional on $V$.

- If we make $V$ a normed vector space with the norm 

$$\lVert (a_1, a_2, ...) \rVert_\infty = max_{k \in Z^+} |a_k| ,$$

then $\phi$ is not a bounded linear functional on $V$.


### 6.51 Definition: null space
Suppose $V$ and $W$ are vector spaces and $T: V \to W$ is a linear map. Then the null space of $T$ is denoted by $null T$ and is defined by

$$null T = \\{f \in V: Tf = 0 \\} .$$


### 6.52 bounded linear functionals
Suppose $V$ is a normed vector space and $\phi: V \to F$ is a linear functional that is not identically 0. The the following are equivalent:

(a) $\phi$ is a bounded linear functional.

(b) $\phi$ is a continuous linear functional.

(c) $null \phi$ is a closed subspace of $V$.

(d) $\overline{null \phi} \neq V$.


## Discontinuous Linear Functionals

We need to extend the notion of a basis of a finite-dimensional vector to an infinite-dimensional context. In a finite-dimensional vector space, we might consider a basis of the form $e_1, ..., e_n$, where $n \in Z^+$ and each $e_k$ is an element of our vector space. We can think of the list $e_1, ..., e_n$ as a function from $\\{1, ..., n\\}$ to our vector space, with the value of this function at $k \in \\{1, ..., n\\}$ denoted by $e_k$ with a subscript $k$ instead of by the usual functional notation $e(k)$. To generalize, in the next definition we allow $\\{1, ..., n\\}$ to be replaced by an arbitrary set that might not be a finite set.


### 6.53 Definition: family
A family $\\{e_k\\}_{k \in \Gamma}$ in a set $V$ is a function $e$ from a set $\Gamma$ to $V$, with the value of the function $e$ at $k \in \Gamma$ denoted by $e_k$.


### 6.54 Definition: linearly independent; span; basis
Suppose $\\{e_k\\}_{k \in \Gamma}$ is a family in a vector space $V$.

- $\\{e_k\\}_{k \in \Gamma}$ is called linearly independent if there does not exist a finite nonempty subset $\Omega$ of $\Gamma$ and a family $\\{\alpha_j\\}_{j \in \Omega}$ in $F \ \\{0\\}$ such that $\sum_{j \in \Omega} \alpha_j e_j = 0$.

- The span of $\\{e_k\\}_{k \in \Gamma}$ is denoted by $span \\{e_k\\}_{k \in \Gamma}$ and is defined to be the set of all sums of the form 

$$\sum_{j \in \Omega} \alpha_j e_j,$$

where $\Omega$ is a finite subset of $\Gamma$ and $\\{\alpha_j\\}_{j \in \Omega}$ is a family in $F$.

- A vector space is called finite-dimensional if there exists a finite set $\Gamma$ and a family $\\{e_k\\}_{k \in \Gamma}$ in $V$ such that $span \\{e_k\\}_{k \in \Gamma} = V$.

- A vector space is called infinite-dimensional if it is not finite-dimensional.

- A family in $V$ is called a basis of $V$ if it is linearly independent and its span equals $V$.


### 6.55

### 6.56

### 6.57

### 6.58

### 6.59

### 6.60

### 6.61

### 6.62



## Hahn-Banach Theorem

### 6.63

### 6.67

### 6.68

### 6.69

### 6.71

### 6.72

### 6.73





# 6E Consequences of Baire's Theorem

## Baire's Theorem

### 6.74

### 6.75

### 6.76

### 6.80



## Open Mapping Theorem and Inverse Mapping Theorem

### 6.81

### 6.83



## Closed Graph Theorem

### 6.84

### 6.85


## Principle of Uniform Boundedness

### 6.86