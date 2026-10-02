---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/transpose/","dg-note-properties":{}}
---

# Transpose

>[!example] Transpose, $A^t$
>The transpose of a [[Math/Linear Algebra Done Right/Matrices\|matrix]] $A$, denoted $A^t$, is obtained by interchanging the rows and columns of $A$. Specifically, if $A$ is an m-by-n matrix, then $A^t$ is the n-by-m matrix whose entries are determined by 
> $$
> (A^t)_{k,j}=A_{j,k}
> $$

>[!info] The transpose of the product of matrix
>If $A$ is an m-by-n matrix and $C$ is an n-by-p matrix, then
> $$
> (AC)^t=C^tA^t
> $$
>
>Proof:
> $$
> \begin{align}
((AC)^t)_{j,k}&=(AC)_{k,j} \\
&=\sum_{r=1}^n A_{k,r}C_{r,j} \\
&=\sum_{r=1}^n C^t_{j,r}A^t_{r,k} \\
&=(C^tA^t)_{j,k}
\end{align}
> $$
> 
> $\blacksquare$

>[!info] The [[Math/Linear Algebra Done Right/M(T)\|matrix]] of [[Math/Linear Algebra Done Right/Dual Map\|$T'$]] is the transpose of the matrix of [[Math/Linear Algebra Done Right/Linear Map\|$T$]].
>Suppose $T\in \mathcal{L}(V,W)$, then $\mathcal{M}(T')=\mathcal{M}(T)^{t}$
>
>Proof:
>
>From the definition of $T'$, we get $T'(\phi)=\phi \circ T$, where $\phi \in W'$. Replace both sides with matrix representation, we get
> $$
> \begin{align}
\mathcal{M}(T')\mathcal{M}(\phi)_{\text{vector}}&=(\mathcal{M}(\phi)_{map}\mathcal{M}(T))^t \\
\iff \mathcal{M}(T')\mathcal{M}(\phi)_{\text{vector}}&=\mathcal{M}(T)^t\mathcal{M}(\phi)_{\text{vector}}
\end{align}
> $$
> Since the equation above holds true for all $\phi$, we get $\mathcal{M}(T')=\mathcal{M}(T)^t$
> 
> $\blacksquare$



