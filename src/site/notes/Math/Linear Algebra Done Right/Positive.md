---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/positive/","dg-note-properties":{}}
---

# Positive
> [!example] Definition of positive operator
> An operator $T\in$[[Math/Linear Algebra Done Right/L(V)\|L(V)]] is called positive if [[Math/Linear Algebra Done Right/Linear Map\|$T$]] is [[Math/Linear Algebra Done Right/Self-Adjoint\|self-adjoint]] and 
> $$
> \langle Tv,v \rangle\geq 0
> $$ 
> for all $v\in$[[Math/Linear Algebra Done Right/Vector Space\|$V$]].


> [!info]  Characterization of positive operators
> (a) $T$ is positive
> 
> (b) $T$ is self-adjoint and all the [[Math/Linear Algebra Done Right/Eigenvalue\|eigenvalues]] of $T$ are non-negative
> 
> (c) $T$ has a positive [[Math/Linear Algebra Done Right/Square Root\|square root]]
> 
> (d) $T$ has a self-adjoint sqaure root
> 
> (e) there exist an operator$R\in \mathcal{L}(V)$ such that $T=R^*R$.
>
>Proof:
>
>(a) and (b): Suppose $T$ is positive, then by definition $T$ is self-adjoint. Suppose $v$ is an eigenvalue of $T$ such that $Tv=\lambda v$, we have $\langle Tv,v \rangle=\langle \lambda v,v \rangle=\lambda \lVert v \rVert^2$. Therefore, we have $\lambda\geq0$ for all eigenvalues of $T$. If (b) holds, by [[Math/Linear Algebra Done Right/Spectral Theorem\|spectral theorem]], there exist a [[Math/Linear Algebra Done Right/Orthonomal\|orthonormal]] [[Math/Linear Algebra Done Right/Basis\|basis]] such that all the vectors in the list are eigenvectors of $T$. Therefore, $\langle Tv,v \rangle=\langle \lambda_{1}a_{1}e_{1}+\dots \lambda_{n}a_{n}e_{n},a_{1}e_{n}+\dots+a_{n}e_{n} \rangle\geq 0$. So (a) holds.
>
>(b) and (c): Suppose (b) holds and $e_{1},\dots,e_{n}$ is the orthornormal basis such that $e_{1},\dots,e_{n}$ are eigenvectors of $T$ guarenteed by the Spectral Theorem. Let $Te_{i}=\lambda_{i}e_{i}$, let $Re_{i}=\sqrt{ \lambda_{i} }e_{i}$. It should be simple that $R^2e_{i}=Te_{i}$ if and only if $R$ is a square root of $T$. Suppose (c) holds, let $R$ be the positive square root of $T$ such that $R^2=T$. Since $R$ is self-adjoint, we have $T$ is also self-adjoint. Suppose $Tv=R^2v=\lambda v$, then we have $(R^2-\lambda I)v=0$, which is $(R-\sqrt{ \lambda }I)(R+\sqrt{ \lambda }I)v=0$. This implies that every the eigenvalue of $T$ is a square of an eigenvalue of $R$. Thus all the eigenvalues of $T$ are non-negative.
>
>(c) and (d): The positive square root is also the self-adjoint sqaure root.
> 
>(d) to (e): Let $R$ be the self-adjoint square root of $T$ and $T=RR ^*$.
>
>(e) to (a): Suppose $T=R^*R$, $\langle R^*Rv,v \rangle=\langle Rv,Rv \rangle=\lVert v \rVert^2$, thus, $T$ is positive. Easy to verify $T$ is self-adjoint.
>
>$\blacksquare$

