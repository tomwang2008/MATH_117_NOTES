---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/ranges/","dg-note-properties":{}}
---

$\def\range{\text{range} }$
# Ranges

>[!example] Ranges
>For $T$ a function from [[Math/Linear Algebra Done Right/Vector Space\|$V$]] to $W$, the range of $T$ is a subset of $W$ consisting of those vectors that are of the form $Tv$ for some $v\in V$.
>Mathematically, range is expressed as:
>$$ \text{range T}  =\set{Tv\ :\ v\in V}$$ 

Similar to [[Math/Linear Algebra Done Right/Null Spaces\|null space]], range is a [[Math/Linear Algebra Done Right/Subspace\|subspace]] of $W$.

>[!info] The range is a subspace
>If $T\in$ [[Math/Linear Algebra Done Right/L(V,W)\|L(V,W)]] then $\text{range T}$ is a subspace of $W$.
>
>Proof:
>
>Let $u,v\in \text{range T}$ where $u=Tv_1,v=Tv_2$. $u+v=T(v_1+v_2)$, therefore, $(u+v)\in \text{range} T$.
>
>Let $u\in \text{range T}$ and $\lambda \in\mathbf F$, where $u=Tv_1$. $\lambda u=\lambda T(v_1)=T(\lambda v_1)$, therefore, $\lambda u\in \text{range T}$.
>
>$\blacksquare$

