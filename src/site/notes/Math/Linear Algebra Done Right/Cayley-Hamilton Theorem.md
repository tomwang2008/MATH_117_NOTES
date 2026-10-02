---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/cayley-hamilton-theorem/","dg-note-properties":{}}
---

# Cayley-Hamilton Theorem
> [!info]  Cayley-Hamilton Theorem
> Suppose $V$ is a complex vector space and $T\in$[[Math/Linear Algebra Done Right/L(V)\|L(V)]]. Let $q$ denote the [[Math/Linear Algebra Done Right/Characteristic Polynomial\|characteristic polynomial]] of $T$. Then $q(T)=0$.
> 
> Proof:
> 
> Suppose $\lambda_{1},\dots,\lambda_{m}$ are all the [[Math/Linear Algebra Done Right/Eigenvalue\|eigenvalues]] of $T$. Consider the operator $(T-\lambda_{j}I)^{d_{j}}\big|_{{G(\lambda_{j},T)}}$, the operator $(T-\lambda_{j}I)\big|_{G(\lambda_{j},T)}$ is [[Math/Linear Algebra Done Right/Nilpotent\|nilpotent]]. Therefore, $(T-\lambda_{j}I)^{d_{j}}\big|_{{G(\lambda_{j},T)}}=0$. 
> 
> Since [[Math/Linear Algebra Done Right/Generalized Eigenspace\|$V=G(\lambda_{1},T)\oplus\dots \oplus G(\lambda_{m},T)$]], we only need to prove $p(T)\big|_{G(\lambda_{j},T)}=0$ for every $j=1,\dots,m$. This should be trival.
> 
> $\blacksquare$

<span style="color:rgb(188, 145, 16)">Note</span>, the theorem also works in real vector spaces. 

Because the characterisitc polynomial of a real operator is defined as the characterisitc polynomial of [[Math/Linear Algebra Done Right/Complexification\|$T_{\mathbb{C}}$]].

