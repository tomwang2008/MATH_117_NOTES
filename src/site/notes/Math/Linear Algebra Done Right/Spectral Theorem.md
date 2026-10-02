---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/spectral-theorem/","dg-note-properties":{}}
---

# Spectral Theorem
Now we present probably the most useful theorem in the study of [[Math/Linear Algebra Done Right/Operator\|operators]] in [[Math/Linear Algebra Done Right/Inner Product Space\|inner product space]] —— spectral theorem.

> [!info]  Complex Spectral Theorem
> Suppose $\mathbf{F}=\mathbb{C}$ and $T\in$[[Math/Linear Algebra Done Right/L(V)\|L(V)]]. Then the following are equivalent:
> 
> (a) $T$ is [[Math/Linear Algebra Done Right/Normal\|normal]]
> 
> (b) [[Math/Linear Algebra Done Right/Vector Space\|$V$]] has an [[Math/Linear Algebra Done Right/Orthonomal\|orthonormal]] basis consisting of [[Math/Linear Algebra Done Right/Eigenvector\|eigenvectors]] of $T$
> 
> (c) $T$ has a [[Math/Linear Algebra Done Right/Diagonal Matrix\|diagonal matrix]] with respect to some orhonormal [[Math/Linear Algebra Done Right/Basis\|basis]] of $V$
> 
> Proof:
> 
> (c) and (b) should be trival without a proof, therefore, we only prove (a) and (c) are equivalent.
> 
> Suppose (c) holds, because the [[Math/Linear Algebra Done Right/Conjugate Transpose\|conjugate transpose]] of $T$ is the [[Math/Linear Algebra Done Right/Adjoint\|adjoint]] operator of $T$ and $T$ has a diagonal matrix. We have both $T$ and $T^*$ have a diagonal matrix. Since diagonal [[Math/Linear Algebra Done Right/Matrices\|matrices]] commute, (a) holds.
> 
> Now we show that (a) implies (c). Suppose we have an [[Math/Linear Algebra Done Right/Upper-triangular Matrix\|upper-triangular matrix]] with respect to some orthonormal basis of $T$. 
> $$\mathcal{M}(T)=
> \begin{pmatrix}
a_{1,1} & \dots & a_{1,n} \\
  & \ddots & \vdots \\
0 &  & a_{n.n}
\end{pmatrix}
> $$
> Since $T$ is normal
> $$
> \lVert Te_{1} \rVert ^2=\lVert T^*e_{1} \rVert^2
> $$
> which implies that:
> $$
> \lVert a_{1,1}e_{1} \rVert^2 =\lVert a_{1,1}e_{1}+a_{1,2}e_{2}+\dots+a_{1,n}e_{n} \rVert
{ #2}

> $$
> Since $e_{1},\dots,e_{n}$ is orthonormal, by applying the Pythagorean Theorem, we have 
> $$
> \lVert a_{1,1} \rVert ^2=\lVert a_{1,1} \rVert^2+\lVert a_{1,2} \rVert ^2+\dots+\lVert a_{1,n} \rVert
{ #2}

> $$
> which is 
> $$
> 0=\lVert a_{1,2} \rVert ^2+\lVert a_{1,3} \rVert ^2+\dots+\lVert a_{1,n} \rVert
{ #2}

> $$
> Since sum of squares is always greater than 0, we now know that $\lVert a_{1,2} \rVert=\dots=\lVert a_{1,n} \rVert=0$.
> Continuing in this fashion, we see that all the nondiagonal entries in the matrix equal $0$. Thus (c) holds.
> 
> $\blacksquare$


We may wonder, if this theorem applies in real number field. The answer is yes, but before we prove if, we need some preliminary results.


> [!info]  Invertible quadratic expressions
> Suppose $T\in \mathcal{L}(V)$ is [[Math/Linear Algebra Done Right/Self-Adjoint\|self-adjoint]] and $b,c\in \mathbb{R}$ are such that $b-4c^2$. Then
> $$
> T^2+bT+cI
> $$
> is invertible.
> 
> Proof:
> 
> Let $v$ is a non-zero vector in $V$. Then 
> $$
> \begin{align}
\langle (T^2+bT+c)v,v \rangle & =\langle T^2v,v \rangle+\langle bTv,v \rangle+\langle cv,v \rangle \\
 & =\langle Tv,Tv \rangle+b\langle Tv,v \rangle+c\langle v,v \rangle \\
 & \geq \lVert Tv \rVert^2+b\lVert Tv \rVert\lVert v \rVert+c\lVert v \rVert^2 \\
 & =\left( Tv-\frac{b\lvert v \rvert }{2} \right) ^2+\left( c-\frac{b^2}{4} \right) \lvert v \rvert^2 \\
 & \geq 0 
\end{align}
> $$
> This implies that $T^2+bT+c$ is [[Math/Linear Algebra Done Right/Injectivity\|injective]], in this condition it also implies that $T$ is [[Math/Linear Algebra Done Right/Invertible\|invertible]].
> 
> $\blacksquare$


> [!info] Self-adjoint operators have eigenvalues
> Suppose $V\neq \{ 0 \}$ and $T\in \mathcal{L}(V)$ is a self-adjoint operator. Then $T$ has an eigenvalue.
> 
>Proof:
>
>Suppose $v\neq_{0}$ and $\text{dim }V=0$. Then we have $v,Tv,T^2v,\dots,T^nv$ can not be [[Math/Linear Algebra Done Right/Linear Independence\|linearly indepdent]]. Therefore, there exist $a_{0},\dots,a_{n}\in \mathbf{F}$ such that 
> $$
> a_{0}v+a_{1}Tv+\dots+a_{n}T^nv=0
> $$
> Factor the polynomial above we get
> $$
>  (a_{0}v+a_{1}Tv+\dots+a_{n}T^n)v=\prod(T-\lambda_{i}I)\prod(T^2+b_{j}T+c_{j})v=0
> $$
> From the result above we know $\prod (T+b_{j}T+c_{j})$is injective, therefore $\prod (T+b_{j}T+c_{j})v \neq0$. Thus $\prod(T-\lambda_{i}I)v=0$ for some $\lambda_{i}\in \mathbf{F}$. This implies that at least one $\lambda_{i}$ is an eigenvalue of $T$.
> 
> $\blacksquare$

> [!info]  Self-adjoint oeprators and invariant subspaces
> Suppose $T\in \mathcal{L}(V)$ is self-adjoint and $U$ is a subspace of $V$ that is [[Math/Linear Algebra Done Right/Invariant Subspace\|invariant]] under $T$. Then 
> 
> (a) [[Math/Linear Algebra Done Right/Orthogonal Complement\|$U^{\perp}$]] is invarinat under $T$
> 
> (b) [[Math/Linear Algebra Done Right/Restiction Operator\|Restiction Operator]]$\in \mathcal{L}(U)$ is self-adjoint
> 
> (c) $T\big|_{U^\perp}\in \mathcal{L}(U^\perp)$ is self-adjoint
> 
> Proof:
> 
> For (a), we have $\langle Tu,w \rangle=\langle u,Tw \rangle=0$, where $u\in U$ and $w\in U^\perp$. This implies (a).
> 
> For (b), we have $\langle T\big|_{U}u,u_{1} \rangle=\langle Tu,u_{1} \rangle=\langle u,Tu_{1} \rangle=\langle u,T\big|_{U}u_{1} \rangle$. This impies (b).
> 
> For (c), repeat the fashion for (b) again and we get the desired.
> 
> $\blacksquare$

Now we can finally prove the spectral theorem on real number field.

> [!info] Real Spectral Theorem
> Suppose $\mathbf{F}=\mathbb{R}$ and $T\in \mathcal{L}(V)$. Then the followings are equivalent.
> 
> (a) $T$ is self-adjoint
> 
> (b) $V$ has an orthonormal basis consisting of eigenvectors of $T$.
> 
> (c) $T$ has a diagonal matrix with respect to some orthonormal basis of $V$.
> 
> Proof:
> 
> Suppose (a) holds.
> 
> $T$ at least has one eigenvector $e_{1}$ corresponding to the eigenvalue of $\lambda_{1}$. Then $T$ is invariant under the subspace $U=\text{span }(e_{1})$. Thus $T\big|_{U^\perp}$ is self-adjoint under $U^\perp$. Therefore, we have another eigenvalue $\lambda_{2}$ such that $T\big|_{U\perp}e_{2}=\lambda_{2}e_{2}=Te_{2}$. Repeat the fashion, and notice the vector space shrinks one dimension every time. Therefore, we get $n$ different eigenvectors. These eigenvectors should be orthonormal, since every time we split the vector space into two subspaces which one is the orthogonal completment of the other. Thus (b) holds. 
> 
> The rest should be trival.
> 
> $\blacksquare$

