---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/invertible/","dg-note-properties":{}}
---

# Invertible

>[!example] Definition of invertible and inverse
>Invertible
>
>A [[Math/Linear Algebra Done Right/Linear Map\|linear map]] $T\in$[[Math/Linear Algebra Done Right/L(V,W)\|L(V,W)]] is called invertible if there exist a linear map $S\in \mathcal{L}(W,V)$ such that $ST$ equals the identity map on $W$ and $TS$ equals the identity map on $V$.
>
>Inverse
>
>A linear map $S\in \mathcal{L}(W,V)$ satisfying $ST=I$ and $TS=I$ is called an inverse of $T$.

>[!info] Inverse is unique.
>An invertible linear map has a unique inverse.
>
>Proof:
>
>Let $S_{1}$ and $S_{2}$ be the two inverse of $T$.
> $$
>  S_{1}=S_{1}(TS_{2})=(S_{1}T)S_{2}=IS_{2}=S_{2}
> $$
>Thus, $S_{1}=S_{2}$.
> $\blacksquare$

Since we know inverse is unique, we give the definition below,

>[!example] $T^{-1}$
>If $T$ is invertible, then the inverse of $T$ is denoted by $T^{-1}$. In other words, $T^{-1}$ is the unique element in $\mathcal{L}_(W,V)$ such that $TT^{-1}=I$ and $T^{-1}T=I$.

The following character of invertible linear map is important.

>[!info] Invertibility is equivalent to [[Math/Linear Algebra Done Right/Injectivity\|injectivity]] and [[Math/Linear Algebra Done Right/Surjectivity\|surjectivity]].
>
>A linear map is invertible if and only if it is injective and surjective.
>
>Proof:
>
>Suppose $T\in \mathcal{L}(V,W)$ is invertible. We want to prove that $T$ is also injective and surjective.
>
>First, suppose $Tu=Tv$ then we have $T^{-1}Tu=T^{-1}Tv$, therefore $u=v$. Thus, T is injective. Also, for every $w\in W$, $TT^{-1}(w)=w$. Therefore, there exists $v\in V$ that maps to $w$. Thus, $T$ is surjective.
>
>Second, suppose $T$ is injective and surjective, we define $S:W \to V$ by $S(w)=v$ where $T(v)=w$. Easy to verify $S$ is a linear map and also $S$ is well-defined because $T$ is both injective and surjective.
>
>$\blacksquare$


> [!example] Definition of invertible for a [[Math/Linear Algebra Done Right/Matrices\|matrix]]
> A square matrix $A$ is called invertible if there is a square matrix $B$ of the same size such that $AB=BA=I$; we call $B$ the inverse of $A$ and denote it by $A^{-1}$.

 