Measure Integration Real Analysis - Chapter 8 <br>
Hilbert Spaces
================
Rosie Sun <br>
2026-09-27


# 8A Inner Product Spaces

### 8.1 Definition inner product; inner product space

### 8.3 basic properties of an inner product

### 8.4 Definition norm associated with an inner product

### 8.6 homogeneity of the norm

### 8.7 Definition orthogonal 

### 8.9 Pythagorean Theorem

### 8.10 orthogonal decomposition

### 8.11 Cauchy-Schwartz inequality 

### 8.15 triangle inequality 

### 8.19 $\lvert \rvert$ is a norm

### 8.20 parallelogram equality 



# 8B Orthogonality 

### 8.21 Definition: Hilbert space

### 8.24 Definition: distance from a point to a set

### 8.25 Definition: convex set

### 8.28 distance to a closed convex set is attained in a Hilbert space

### 8.34 Definition: orthogonal projection

### 8.37 orthogonal projection onto closed subspace

### 8.38 Definition: orthogonal complement

### 8.40 properties of orthogonal complement

### 8.41 orthogonal complement of the orthogonal complement

### 8.42 necessary and sufficient condition for a subspace to be dense

### 8.43 orthogonal decomposition

### 8.44 Definition: identity map

### 8.45 range and null space of orthogonal projections

### 8.47 Riesz Representation theorem
Suppose $\phi$ is a bounded linear functional on a Hilbert space $V$. Then there exists a unique $h \in V$ such that 

$$\phi(f) = \langle f, h \rangle$$

for all $f \in V$. Furthermore, $\lVert \phi \rVert = \lVert h \rVert$.



# 8C Orthonormal Bases

### 8.50 Definition: orthonormal family
A family $\\{e_k\\}_{k \in \Gamma}$ in an inner product space is called an orthonormal family if 

$$
\langle e_j, e_k \rangle
=
\begin{cases}
0 & \text{ if } j \neq k \\
1 & \text{ if } j = k
\end{cases}
$$

for all $j, k \in \Gamma$.

In other words, a family $\\{e_k\\}_{k \in \Gamma}$ is an orthonormal family if $e_j$ and $e_k$ are orthogonal for all distinct $j, k \in Gamma$ and $\lVert e_k \rVert = 1$ for all $k \in \Gamma$.




### 8.74 orthonormal bases as maximal elements

### 8.75 existence of orthonormal bases for all Hilbert spaces


### 8.76 Riesz Representation Theorem
Suppose $\phi$ is a bounded linear functional on a Hilbert space $V$ and $\\{e_k\\}_{k \in \Gamma}$ is an orthonormal basis of $V$. Let 

$$h = \sum_{k \in \Gamma} \overline{\phi(e_k)} e_k .$$

Then

$$\phi(f) = \langle f, h \rangle$$

for all $f \in V$. Furthermore, 

$$\lVert \phi \rVert = \left( \sum_{k \in \Gamma} |\phi(e_k)|^2 \right)^{1/2}$$