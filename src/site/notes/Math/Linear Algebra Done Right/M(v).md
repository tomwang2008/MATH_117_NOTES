---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/m-v/","dg-note-properties":{"mathLink":"$\\mathcal{M}(v)$"}}
---

# $\mathcal{M}(v)$

>[!example] Definition of the matrix of a vector
>Suppose $v\in V$ and $v_{1},v_{2},\dots,v_{n}$ is a [[Math/Linear Algebra Done Right/Basis\|basis]] of [[Math/Linear Algebra Done Right/Vector Space\|$V$]]. The [[Math/Linear Algebra Done Right/Matrices\|matrix]] of $v$ with respect to the basis is the $n-\text{by}-1$ matrix
> $$
> \mathcal{M}(v)=\begin{pmatrix}
>c_{1} \\
>\vdots \\
>c_{n}
\end{pmatrix}
> $$
> where $c_{1},\dots,c_{n}$ are scalars such that
>  $$
> v=c_{1}v_{1}+\dots+c_{n}v_{n}
> $$

Here we reveal some relationships between [[Math/Linear Algebra Done Right/M(T)\|M(T)]] and $\mathcal{M}(v)$.

>[!info] $\mathcal{M}(T)_{.,k}=\mathcal{M}(Tv_{k})$
>Suppose $T\in$ [[Math/Linear Algebra Done Right/L(V,W)\|L(V,W)]] and $v_{1},\dots,v_{n}$ is a basis of $V$ and $w_{1},\dots,w_{m}$ is a basis of $W$. Let $1\leq k\leq n$. Then the $k^{th}$ column of $\mathcal{M}(T)$ which is denoted $\mathcal{M}(T)_{.,k}$, equals $\mathcal{M}(Tv_{k})$.
>
>Proof:
>
>The desired result follows immediately from the definitions of $\mathcal{M}(T)$ and $\mathcal{M}(v)$.
>
>$\blacksquare$

The next result shows how the notions of the matrix of a linear map, the matrix of a vector, and matrix multiplication fit together.

>[!info] Linear maps act like matrix multiplication
>Suppose $T\in \mathcal{L}(V,W)$ and $v\in V$. Suppose $v_{1},\dots,v_{n}$ is a basis of $V$ and $w_{1},\dots,w_{m}$ is a basis of $W$. Then
> $$
> \mathcal{M}(Tv)=\mathcal{M}(T)\mathcal{M}(v)
> $$
> 
> Proof:
> 
>Let $v=c_{1}v_{1}+\dots+c_{n}v_{n}$. Thus, $Tv=c_{1}Tv_{1}+\dots+c_{n}Tv_{n}$. Therefore, we have
> $$
> \begin{align}
>\mathcal{M}(Tv)&=c_{1}\mathcal{M}(Tv_{1})+\dots+c_{n}\mathcal{M}(Tv_{n})\\
>&=c_{1}\mathcal{M}(T)_{.,1}+\dots+c_{n}\mathcal{M}(T)_{.,n}  \\
>&=\mathcal{M}(T)\mathcal{M}(v)
\end{align}
> $$
> From the second equation to the third, we use the property of [[Math/Linear Algebra Done Right/Matrices\|matrix]] multiplication.
> 
> $\blacksquare$

