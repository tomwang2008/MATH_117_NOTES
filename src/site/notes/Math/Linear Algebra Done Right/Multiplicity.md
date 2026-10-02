---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/multiplicity/","dg-note-properties":{}}
---

# Multiplicity
> [!example] Definition of multiplicity
> Suppose $T\in$[[Math/Linear Algebra Done Right/L(V)\|L(V)]]. The multiplicity of an eigenvalue $\lambda$ of $T$ is defined to be the dimension of the corresponding [[Math/Linear Algebra Done Right/Generalized Eigenspace\|generalized eigenspace]] $G(\lambda,T)$.
> 
> In other words, the multiplicity of an eigenvalue $\lambda$ of $T$ equals $\text{dim null }(T-\lambda I)^{\text{dim }V}$.

> [!info]  Sum of the multiplicities equals $\text{dim }V$
> Suppose $V$ is a complex vector space and $T\in \mathcal{L}(V)$. Then the sum of the multiplicities of all the [[Math/Linear Algebra Done Right/Eigenvalue\|eigenvalues]] of $T$ equals $\text{dim }V$.
> 
> Proof:
> 
> The result follows directly from the conclusion that [[Math/Linear Algebra Done Right/Generalized Eigenspace\|$V=G(\lambda_{1},T)\oplus \dots \oplus G(\lambda _{m},T)$]].
> 
> $\blacksquare$

