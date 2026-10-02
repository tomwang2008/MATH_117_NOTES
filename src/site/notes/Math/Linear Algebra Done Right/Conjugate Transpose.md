---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/conjugate-transpose/","dg-note-properties":{}}
---

# Conjugate Transpose
> [!example] Definition of conjugate transpose
> The conjugate [[Math/Linear Algebra Done Right/Transpose\|transpose]] of an m-by-n matrix is the n-by-m [[Math/Linear Algebra Done Right/Matrices\|matrix]] obtained by interchanging the rows and columns and then taking the complex conjugate of each entry.

> [!info]  The matrix of [[Math/Linear Algebra Done Right/Adjoint\|$T^*$]] 
> Let $T\in$[[Math/Linear Algebra Done Right/L(V,W)\|L(V,W)]]. Suppose $e_{1},\dots,e_{n}$ is an [[Math/Linear Algebra Done Right/Orthonomal\|orthonormal]] basis of $V$ and $f_{1},\dots,f_{m}$ is an orthonormal basis of $W$. Then
> $$
> \mathcal{M}(T^*,(f_{1},\dots,f_{m}),(e_{1},\dots,e_{n}))
> $$
> is the conjugate transpose of 
> $$
> \mathcal{M}(T,(e_{1},\dots,w_{n}),(f_{1},\dots,f_{m}))
> $$
> 
> Proof:
> 
> In the proof, we write $\mathcal{M}(T,(e_{1},\dots,w_{n}),(f_{1},\dots,f_{m}))$ as $\mathcal{M}(T)$ and $\mathcal{M}(T^*,(f_{1},\dots,f_{m}),(e_{1},\dots,e_{n}))$ as $\mathcal{M}(T^*)$.
> 
> As readers can verify $\langle Te_{k}, f_{j} \rangle$ represents the entry $A_{j,k}$. Therefore, $\langle Te_{k},f_{j} \rangle=\langle e_{k}, T^*f_{j} \rangle=\overline{\langle T^*f_{j},e_{k} \rangle}$. This shows that the entry $A_{j,k}$ of $\mathcal{M}(T)$ equals the entry $\overline{A_{k,j}}$ of $\mathcal{M}(T^*)$. Thus, we get $\mathcal{M}(T)=\overline{\mathcal{M}(T^*)}$.
> 
> $\blacksquare$



