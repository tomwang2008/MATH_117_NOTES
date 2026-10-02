---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/matrix-representation/","dg-note-properties":{}}
---

# Matrix Representation

Here we reveal the relation between [[Math/Linear Algebra Done Right/L(V,W)\|L(V,W)]] and [[Math/Linear Algebra Done Right/The matrix representation of L, 𝗙ᵐ,ⁿ\|The matrix representation of L, 𝗙ᵐ,ⁿ]].

>[!info] $\mathcal{L}(V,W)$ and $\mathbf{F}^{m,n}$ are [[Math/Linear Algebra Done Right/Isomorphism\|isomorphic]]
>Suppose $v_{1},v_{2},\dots,v_{n}$ is a [[Math/Linear Algebra Done Right/Basis\|basis]] of [[Math/Linear Algebra Done Right/Vector Space\|$V$]], and $w_{1},w_{2},\dots,w_{m}$ is a basis of $W.$ Then, [[Math/Linear Algebra Done Right/M(T)\|$\mathcal{M}$]] is an isomorphism between $\mathcal{L}(V,W)$ and $\mathbf{F}^{m,n}$.
>
>Proof:
>
>$\mathcal{M}$ is an isomorphism means it's an [[Math/Linear Algebra Done Right/Invertible\|invertible]] [[Math/Linear Algebra Done Right/Linear Map\|linear map]], which means that $\mathcal{M}$ is [[Math/Linear Algebra Done Right/Injectivity\|injective]] and [[Math/Linear Algebra Done Right/Surjectivity\|surjective]]. 
>
>To prove $\mathcal{M}$ is injective, let $T\in \mathcal{L}(V,W)$ such that $\mathcal{M}(T)=0$, we prove that $T=0$. Since $\mathcal{M}(T)=0$, we have $Tv_{k}=0$ where $k=1,\dots,n$. Thus, $T=0$ and $\mathcal{M}$ is injective.
>
>To prove $\mathcal{M}$ is surjective, for every matrix $A$ in $\mathbf{F}^{}$, let 
> $$
>A= \begin{pmatrix}
>A_{1,1} & \dots & A_{1,n}\\ 
>\vdots &  & \vdots \\
>A_{m,1} & \dots & A_{n,m}\\
\end{pmatrix}
>
> $$
> Therefore, we could find a linear map $T$ where $Tv_k = \sum\limits_{i=1}^{m} A_{i,k}w_i$. Thus, $\mathcal{M}$ is surjective.
> 
> $\blacksquare$


 