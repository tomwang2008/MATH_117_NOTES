---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/m-t/","dg-note-properties":{"mathLink":"$\\mathcal{M}(T)$"}}
---

# $\mathcal{M}(T)$

>[!example] Matrix of a Linear Map
>Suppose $T\in\mathcal{L}(V,W)$ and $v_1,\dots,v_n$ is a [[Math/Linear Algebra Done Right/Basis\|basis]] of $V$ and $w_1,\dots,w_m$ is a basis of $W$. The matrix of $T$ with respect to those bases is the $m-\text{by}-n$ matrix $\mathcal{M}(T)$ whose entries $A_{j,k}$ are defined by
>$$Tv_k=A_{1,k}w_1+\dots+A_{m,k}w_m$$
>Perticularly, the matrix $\mathcal{M}(T)$ will look like:
> $$
> \mathcal{M}(T)=\begin{pmatrix}
>A_{1,1} & \dots & A_{1,n} \\
>\vdots &  & \vdots \\
>A_{m,1} & \dots & A_{m,n}
>\end{pmatrix}
> $$
>If the bases are not clear from the context, then the notation $\mathcal{M}(T,(v_1,\dots,v_n),(w_1,\dots,w_m))$ is used.

Notice that $\mathcal{M}(T)$ of a [[Math/Linear Algebra Done Right/Linear Map\|linear map]] $T\in$ [[Math/Linear Algebra Done Right/L(V,W)\|L(V,W)]] depends on the bases $v_1,\dots,v_n$ of $V$ and $w_1,\dots,w_m$ of $W$, as well as on $T$.

Since [[Math/Linear Algebra Done Right/Matrices\|matrices]] have the properties of addition and scalar multiplication, $\mathcal{M}(T)$ should have the same properties too.

>[!info] The matrix of sum of linear maps
>Suppose $S,T\in \mathcal{L}(V,W)$. Then $\mathcal{M}(S+T)=\mathcal{M}(S)+\mathcal{M}(T)$.
>
>Proof:
>
>By the definition of addition in matrix, it's easy to verify that it is true.
>
>$\blacksquare$

>[!info] The matrix of a scalar times a linear map
>Suppose $\lambda \in \mathbf{F}$ and $T\in \mathcal{L}(V,W)$. Then $\lambda \mathcal{M}(T)=\mathcal{M}(\lambda T)$.
>
>Proof:
>
>By definition $\mathcal{M}(T)$ is a matrix, then by the definition of scalar multiplication of matrix, the statement above is true
>
>$\blacksquare$

>[!info] The matrix of the product of linear maps
>Suppose $T\in \mathcal{L}(U,V)$ and $S\in \mathcal{L}(V,W)$. Then $\mathcal{M}(ST)=\mathcal{M}(S)\mathcal{M}(T)$.
>
>Proof:
>
> $$
> \begin{align}
> (ST)u_{k} &=S\left( \sum_{i=1}^{n}A_{i,k}v_{i} \right)\\
> &=\sum_{i=1}^{n}A_{i,k}S(v_{i}) \\
> &= \sum_{i=1}^{n}A_{i,k}\sum_{j=1}^{m}C_{j,i}w_{j} \\
> &= \sum_{j=1}^{m}\left( \sum_{i=1}^{n}A_{i,k}C_{j,i} \right)w_{j}\\
>\end{align}
> $$
> Thus, by the definition of multiplication of matrices, the statement above is true.
> 
> $\blacksquare$

> [!info]  The matrix of the product of linear maps
> Suppose $u_{1},\dots,u_{n}$ and $v_{1},\dots,v_{n}$ and $w_{1},\dots,w_{n}$ are all bases of $V$. Suppose $S,T\in \mathcal{L}(V)$. Then
> $$
> \begin{align}
>&\mathcal{M}(ST,(u_{1},\dots,u_{n}),(w_{1},\dots,w_{n}))=\\
> &\mathcal{M}(S,(v_{1},\dots,v_{n}),(w_{1},\dots,w_{n}))\mathcal{M}(T,(u_{1},\dots,u_{n}),(v_{1},\dots,v_{n}))
\end{align}
> $$
> Proof:
> 
> Note that the first basis is for input and the second basis is for output, Therefore the first matrix's output matches the second maatrix's input and the cancel out.
> 
> $\blacksquare$


> [!info]  Change of basis formula
> Suppose $T\in \mathcal{L}(V)$. Let $u_{1},\dots,u_{n}$ and $v_{1},\dots,v_{n}$ be bases of $V$. Let $A=\mathcal{M}(I,(u_{1},\dots,u_{n}),(v_{1},\dots,v_{n}))$. Then
> $$
> \mathcal{M}(T,(u_{1},\dots,u_{n}))=A^{-1}M(T,(v_{1},\dots,v_{1}))A
> $$
> Proof:
> 
> This should be trivial according to the conclusion above.
> 
> $\blacksquare$




