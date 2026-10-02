---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/invariant-subspace/","dg-note-properties":{}}
---

 # Invariant Subspace

>[!example] Definition of invariant subspace
>Suppose [[Math/Linear Algebra Done Right/Linear Map\|$T$]] $\in$ [[Math/Linear Algebra Done Right/L(V)\|L(V)]]. A [[Math/Linear Algebra Done Right/Subspace\|subspace]] $U$ of [[Math/Linear Algebra Done Right/Vector Space\|$V$]] is called invariant under $T$ if $u\in U$ implies $Tu\in U$.
>

>[!info] Invariant subspace can have any [[Math/Linear Algebra Done Right/Dimension\|Dimension]].
>Suppose $V$ is a [[Math/Linear Algebra Done Right/Finite-dimensional Vector Space\|finite-demensional]] complex vector space and $T\in \mathcal{L}(V)$. Prove that $T$ has an invariant subspace of dimension $k$ for each $k=1,\dots,\text{dim }V$.
>Proof:
>
>Let $K_{j}$ be the invariant subspace that has a dimension of $\text{dim  }k$. Since $T$ is on a finite-dimensional complex vector space, T has a [[Math/Linear Algebra Done Right/Upper-triangular Matrix\|Upper-triangular Matrix]]. Therefore, let $K_{j}=\text{span }(v_{1},\dots,v_{j})$, where $v_{1},\dots ,v_{n}$ is the [[Math/Linear Algebra Done Right/Basis\|Basis]] of $V$ with respect to the upper-triangular matrix.
>
>$\blacksquare$

> [!info]  The null space and range of $p(T)$ are invariant under $T$
> Suppose $T\in \mathcal{L}(V)$ and $p \in$[[Math/Linear Algebra Done Right/P(F)\|P(F)]]. Then [[Math/Linear Algebra Done Right/Null Spaces\|$\text{null }(p(T))$]] and [[Math/Linear Algebra Done Right/Ranges\|$\text{range }(p(T))$]] are invariant under $T$.
> 
> Proof:
> 
> Suppose $v\in \text{null }p(T)$, we have $p(T)v=0$. Therefore, $p(T)(Tv)=T(p(T)v)=0$ so $Tv\in \text{null }p(T)$. 
> 
> Suppose $v\in \text{range }p(T)$, then we have $p(T)v=u$. Therefore, $Tv=T(p(T)u)=p(T)(Tu)$, which is in $\text{range }p(T)$.
> 
> $\blacksquare$

> [!info]  Every operator has an invariant subspace of dimension 1 or 2
> Every operator on a nonzero finite-dimensional vector space has an invariant subspace of dimension 1 or 2
> 
> Proof:
> 
> On complex number field every operator has at least one [[Math/Linear Algebra Done Right/Eigenvalue\|eigenvalue]] therefore it has an invariant subsapce of dimension 1. 
> 
> On real number field, suppose $T$ doesn't have any eigenvalues, however, $T_{\mathbb{C}}$ has at least one eigenvalue, let it be $\lambda=a+ib$. Therefore we have 
> $$
> T_{\mathbb{C}}(u+iv)=(a+ib)(u+iv)=(au-bv)+i(av+bu)
> $$
> By the definition of $T_{\mathbb{C}}$, we know $Tu=au-bv$ and $Tv=av+bu$. Thus, $\text{span }(u,v)$ is invariant under $T$ so $T$ has a invariant subspace of 2.
> 
> $\blacksquare$


