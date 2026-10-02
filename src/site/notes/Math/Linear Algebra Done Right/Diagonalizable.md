---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/diagonalizable/","dg-note-properties":{}}
---

# Diagonalizable
>[!example] Definition of diagonalizable
>An operator [[Math/Linear Algebra Done Right/Linear Map\|$T$]]$\in$[[Math/Linear Algebra Done Right/Vector Space\|$V$]] is called diagonalizable if the operator has a [[Math/Linear Algebra Done Right/Diagonal Matrix\|Diagonal Matrix]] with respect to some [[Math/Linear Algebra Done Right/Basis\|Basis]] of V.

>[!info] Conditions equivalent to diagonalizability
>Suppose  $V$ is [[Math/Linear Algebra Done Right/Finite-dimensional Vector Space\|finite-dimensional]] and $T\in \mathcal{L}(V)$. Let $\lambda_{1},\dots,\lambda_{m}$ denote the distinct [[Math/Linear Algebra Done Right/Eigenvalue\|eigenvalues]] of $T$. Then the followings are equivalent:
>
>(a) $T$ is diagonalizable
>(b) $V$ has a basis consisting [[Math/Linear Algebra Done Right/Eigenvector\|eigenvectors]] of $T$
>(c) There exist 1-dimensional subspace $U_{1},\dots,U_{n}$ of $V$, each invariant under $T$, such that 
> $$
> V=U_{1}\oplus\dots \oplus U_{n}
> $$ 
> (d) $V=E(\lambda_{1},T)\oplus\dots \oplus E(\lambda_{m},T)$
> (e) $\text{dim }V=\text{dim }E(\lambda_{1},T)+\dots+\text{dim }E(\lambda_{m},T)$
> 
>Proof:
>
>If $T$ is diagonalizable, then the basis corresponding to the diagonal matrix satisfy (b) and vice versa. Thus (a) and (b) are equivalent.
>
>If (b) holds, then let the basis be $v_{1},\dots,v_{n}$. Let $U_{j}=\text{span }(v_{j})$ and this satisfy (c). If (c) holds, then  for each $T\big|_{U_{j}}(v_{j})=\lambda_{j}v_{j}$ $v_{1},\dots,v_{n}$ are [[Math/Linear Algebra Done Right/Linear Independence\|linearly independent]], since the sum $U_{j}$ is a [[Math/Linear Algebra Done Right/Direct Sum\|Direct Sum]], . Therefore, $v_{1},\dots,v_{n}$ is a basis of $V$.
>
If (d) holds, because the direct sum of [[Math/Linear Algebra Done Right/Eigenspace\|Eigenspace]] adds up to $V$, there exists a basis $v_{1},\dots v_{n}$ such that $v_{j,.}\in E(\lambda_{j},T)$. Therefore, (b) holds. Vice versa.
>
Obviously (d) and (e) are equivalent.
>
>$\blacksquare$

>[!info] Enough eigenvalues implies diagonalizability
>If $T\in \mathcal{L}(V)$ has $\text{dim }V$ distinct eigenvalues, then $T$ diagonalizable.
>
>Proof:
>
>Let $v_{1},\dots,v_{n}$ be the eigenvectors corresponding to the eigenvalues. Then let $\mathcal{M}(v_{j})=\mathcal{M}(T)_{.,j}$, easy to verify that $\mathcal{M}(T)$ is the diagonal matrix of $T$.
>
>$\blacksquare$

<span style="color:rgb(188, 145, 16)">Notice:</span> The conlusion above is only one situation where an [[Math/Linear Algebra Done Right/Operator\|Operator]] is diagonalizable. 
