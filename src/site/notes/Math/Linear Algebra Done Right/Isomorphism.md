---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/isomorphism/","dg-note-properties":{}}
---

# Isomorphism

>[!example] Definition of isomorphism and isomorphic
>**Isomorphism**
>
>An isomorphism is an [[Math/Linear Algebra Done Right/Invertible\|invertible]] [[Math/Linear Algebra Done Right/Linear Map\|linear map]].
>
>**Isomorphic**
>
>Two [[Math/Linear Algebra Done Right/Vector Space\|vector spaces]] are called isomorphic if there is an isomorphism from one vector space onto the other one.
>


Isomorphism means "same shape" so when there is an isomorphism the two vector spaces are essentially the same. This leads to the conclusion:

>[!info] Dimension shows whether vector spaces are isomorphic.
>Two finite-dimensional vector spaces over $\mathbf{F}$ are isomorphic if and only if they have the same dimension.
>
>Proof:
>
>Suppose $V$ and $W$ are isomorphic finite-dimensional vector spaces. Then there exists $T\in \mathcal{L}(V,W)$ such that $T$ is an isomorphism. Therefore, $T$ is injective and surjective. By the [[Math/Linear Algebra Done Right/Fundamental Theorem of Linear Maps\|fundamental theorem of linear maps]],
> $$
> \dim V=\dim \text{null T}+\dim \text{Range T}
> $$
>Since $T$ is injective and surjective $\dim\text{null T}=0$ and $\dim \text{Range T}=\dim W$. So we get $\dim V=\dim W$.
>
>Suppose $V$ and $W$ are two finite-dimensional vector spaces that have the same dimension. Let $v_{1},v_{2}\dots v_{n}$ be a basis of $V$, $w_{1},w_{2},\dots,w_{n}$ be a basis of $W$ and a linear map $T:V\to W$ such that $T(v_{i})=w_{i}$ where $i=1,2,\dots,n$.
>
>Now we verify that $T$ is injective and surjective. Let $u\in \text{null T}$ and $u=a_{1}v_{1}+a_{2}v_{2}+\dots+a_{n}v_{n}$
> $$
> \begin{align}
T(u)&=a_{1}w_{1}+a_{2}w_{2}+\dots+a_{n}w_{n} \\
&=0\\
\end{align}
> $$ 
> Since $w_{1},w_{2},\dots,w_{n}$ is a basis of $W$ all the coefficient has to be 0. Therefore, $u=0$.
> Thus, $T$ is injective. Also because $V$ and $W$ have the same dimension, by the fundamental theorem of linear maps, $T$ is surjective.
> 
> $\blacksquare$


