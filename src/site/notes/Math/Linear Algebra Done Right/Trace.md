---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/trace/","dg-note-properties":{}}
---

# Trace
> [!example] Definition of trace of an operator
> Suppose $T\in$[[Math/Linear Algebra Done Right/L(V)\|L(V)]].
> 
>  - If $\mathbf{F}=\mathbb{C}$, then the trace of $T$ is the sum of the [[Math/Linear Algebra Done Right/Eigenvalue\|eigenvalues]] of $T$, with each eigenvalue repeated according to its [[Math/Linear Algebra Done Right/Multiplicity\|multiplicity]].
> 
> - If $\mathbf{F}=\mathbb{R}$, then the trace of $T$ is the sum of the eigenvalues of [[Math/Linear Algebra Done Right/Complexification\|$T_{\mathbb{C}}$]], with each eigenvalue repeated according to its multiplicity.
>   
> The trace of $T$ is denoted by $\text{trace }T$.

> [!info]  Trace and characteristic polynomial
> Suppose $T\in \mathcal{L}(V)$. Let $n=\text{dim }V$. Then $\text{trace }T$ equals the negative of the coefficient of $z^{n-1}$ in the [[Math/Linear Algebra Done Right/Characteristic Polynomial\|characteristic polynomial]] of $T$.
> 
> Proof:
> 
> By Vieta's formulas, we get the desired.
> 
> $\blacksquare$


> [!example] Definition of trace of a [[Math/Linear Algebra Done Right/Matrices\|matrix]]
> The trace of a square matrix $A$, denoted $\text{trace }A$, is defined to be the sum of the diagonal entries of $A$.
> 
 
> [!info]  Trace of $AB$ equals trace of $BA$
> If $A$ and $B$ are square matrices of the same size, then
> $$
> \text{trace }(AB)=\text{trace }(BA)
> $$
> Proof:
> 
> Suppose the $A_{\mathbf{j}k}$ is the entry of matrix $A$ on row $j$ and column $k$ and $B_{j,k}$ is the entry of matrxi $B$ on row $j$ and column $k$. We have 
> $$
> \begin{align}
\text{trace }AB & =\sum^n_{j=1}\sum^n_{k=1}A_{j,k}B_{k,j} \\
 & =\sum_{k=1}^n\sum_{j=1}^n B_{k,j}A_{j,k} \\
\ & =\text{trace }(BA)
\end{align}
> $$
> $\blacksquare$

Therefore, we have

> [!info]  Trace of matrix of operator does not depend on basis
> Let $T\in \mathcal{L}(V)$. Suppose $u_{1},\dots,u_{n}$ and $v_{1},\dots,v_{n}$ are bases of $V$. Then
> $$
> \text{trace }\mathcal{M}(T,(u_{1},\dots,u_{n}))=\text{trace }\mathcal{M}(T,(v_{1},\dots,v_{n}))
> $$
> Proof:
> 
> We start with the fact that $\mathcal{M}(T,(u_{1},\dots,u_{n}))=A^{-1}\mathcal{M}(T,(v_{1},\dots,v_{n}))A$, where $A=\mathcal{M}(I,(u_{1},\dots,u_{n}),(v_{1},\dots,v_{n}))$. Then we have
> $$
> \begin{align}
\text{trace }\mathcal{M}(T,(u_{1},\dots,u_{n}) & =\text{trace }(A^{-1}\mathcal{M}(T,(v_{1},\dots,v_{n}))A) \\
 & =\text{trace }(\mathcal{M}(T,(v_{1},\dots,v_{n}))A^{-1}A)  \\
 & =\text{trace }\mathcal{M}(T,(v_{1},\dots,v_{n}))
\end{align}
> $$
> $\blacksquare$


> [!info]  Trace of an operator equals trace of its matrix
> Suppose $T\in \mathcal{L}(V)$. Then $\text{trace }T=\text{trace }\mathcal{M}(T)$.
> 
> Proof:
> 
> This should be trivial as the trace of the matrix can be an [[Math/Linear Algebra Done Right/Upper-triangular Matrix\|upper-triangular matrix]].
> 
> $\blacksquare$

> [!info]  The identity is not the difference of $ST$ and $TS$
> There do not exist operators $S, T \in \mathcal{L}(V)$ such that $ST - TS = I$.
> 
> Proof:
> 
> Suppose $S, T \in \mathcal{L}(V)$. Choose a basis of $V$. Then
> $$
> \begin{align}
>\text{trace }(ST-TS) & =\text{trace }ST-\text{trace }TS \\
 & =\text{trace }\mathcal{M}(ST)-\text{trace }\mathcal{M}(TS) \\
 & =\text{trace }(\mathcal{M}(S)\mathcal{M}(T))-\text{trace }(\mathcal{M}(T)\mathcal{M}(S)) \\
 & =0
\end{align}
> $$
> Since the trace of $I$ cannot be $0$, there does not exists such operators like $S$ and $T$
> 
> $\blacksquare$

