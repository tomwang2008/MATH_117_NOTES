---
{"dg-publish":true,"permalink":"/math/principles-of-mathematical-analysis/euclidean-space/","dg-note-properties":{}}
---

# Euclidean Space
> [!example] Definition of eculidean space
> For each positive integer $k$, let $\mathbb{R}^k$ be the set of all ordered $k$-tuples
> $$
> \mathbf{x}=(x_{1},\dots,x_{k})
> $$
> where $x_{1},\dots,x_{k}$ are real numbers, called the coordinates of $\mathbf{x}$. The elements of $\mathbb{R}^k$ are called points, or vectors, especially when $k>1$. We shall denote vectors by boldfaced letters. If $\mathbf{y}=(y_{1},\dots,y_{k})$ and if $\alpha$ is a real number, put 
> $$
> \begin{align}
\mathbf{x}+\mathbf{y} & =(x_{1}+y_{1},\dots,x_{k}+y_{k}) \\
\alpha x & =(\alpha x_{1},\dots,\alpha x_{k})
\end{align}
> $$
> so that $\mathbf{x}+\mathbf{y}\in \mathbb{R}^k$ and $\alpha \mathbf{x}\in \mathbb{R}^k$. This defines addition of vectors, as well as multiplication of a vector by a scalar. These two operations satisfy the commutative, associative, and distributive laws and make $\mathbb{R}^k$ into a [[Math/Linear Algebra Done Right/Vector Space\|vector space]] over the real [[Math/Principles of Mathematical Analysis/Fields\|field]]. The zero element of $\mathbb{R}^k$ is the point $\mathbf{0}$, all of whose coordinates are $0$.
> 
> We also define the so-called "[[Math/Linear Algebra Done Right/Inner Product\|inner product]]" of $\mathbf{x}$ and $\mathbf{y}$ by
> $$
> \mathbf{x}\cdot \mathbf{y}=\sum_{i=1}^kx_{i}y_{i}
> $$
> and the [[Math/Linear Algebra Done Right/Norm\|norm]] of $\mathbf{x}$ by 
> $$
> \lvert \mathbf{x} \rvert =(\mathbf{x}\cdot \mathbf{x})^{1/2}=\left( \sum_{1}^k x_{i}^2\right)^{1/2}
> $$
> The sructure now defined is called euclidiean $k$-space.
> 

> [!info]  Properties of euclidean space
> Suppose $\mathbf{x},\mathbf{y},\mathbf{z}\in \mathbb{R}^k$, and $\alpha$ is real. Then
> (a) $\lvert \mathbf{x} \rvert\geq 0$;
> (b) $\lvert \mathbf{x}\rvert=0$ if and only if $\mathbf{x}=0$;
> (c) $\lvert \alpha \mathbf{x} \rvert=\lvert \alpha \rvert\cdot \lvert \mathbf{x} \rvert$;
> (d) $\lvert \mathbf{x}\cdot \mathbf{y} \rvert\leq \lvert \mathbf{x} \rvert\cdot \lvert \mathbf{y} \rvert$;
> (e) $\lvert \mathbf{x}+\mathbf{y} \rvert\leq \lvert \mathbf{x} \rvert+\lvert \mathbf{y} \rvert$:
> (f) $\lvert \mathbf{x}-\mathbf{z} \rvert\leq \lvert \mathbf{x}-\mathbf{y} \rvert+\lvert \mathbf{y}_{\mathbf{}}-\mathbf{z} \rvert$.
> 
> Proof:
> 
> The prove is almost the same as we did in [[Math/Principles of Mathematical Analysis/Complex Field\|complex field]].

