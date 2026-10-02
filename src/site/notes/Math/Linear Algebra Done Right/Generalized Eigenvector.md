---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/generalized-eigenvector/","dg-note-properties":{}}
---

# Generalized Eigenvector
> [!example] Definition of generalized eigenvector
> Suppose $T\in$[[Math/Linear Algebra Done Right/L(V)\|L(V)]] and $\lambda$ is an [[Math/Linear Algebra Done Right/Eigenvalue\|eigenvalue]] of $T$. A vector $v\in$[[Math/Linear Algebra Done Right/Vector Space\|$V$]] is called a generalized eigenvalue of $T$ corresponding to $\lambda$ if $v\neq 0$ and
> $$
> (T-\lambda I)^j=0
> $$
> for some positive integer $j$.

<span style="color:rgb(188, 145, 16)">Notice:</span> The generaliezed eigenvector behaves slightly different from an eigenvector, $T^jv$ does not necessarily equals $\lambda^jv$ nor $\lambda v$.

> [!info]  Linearly independent generalized eigenvectors
> Let $T\in \mathcal{L}(V)$. Suppose $\lambda_{1},\dots,\lambda_{m}$ are distinct eigenvalues fo $T$ and $v_{1},\dots,v_{m}$ are corresponding generalized eigenvectors. Then $v_{1},\dots,v_{m}$ is linearly independent.
> 
> Proof:
> 
> For every $n$ appears in the proof, let $n=\text{dim }V$
> 
> We want to prove that $a_{1}v_{1}+\dots+a_{m}v_{m}=0$ if and only if $a_{i}=0$ for $i=1,\dots,m$. 
> 
> Suppose $j$ which let $(T-\lambda_{1}I)^jv_{1}=0$ is the smallest $j$ that satisfy the equation. Let $(T-\lambda_{1}I)^{j-1}v=w$. Therefore we have $Tw=\lambda_{1}w$ and $(T-\lambda I)^jw=(\lambda_{1}-\lambda)^jw$.
> 
> Consider the operator below,
> $$
> (T-\lambda_{1}I)^{j-1}(T-\lambda_{2}I)^n \cdot\dots \cdot(T-\lambda_{m}I)^n
> $$
> Apply this operator on $a_{1}v_{1}+\dots+a_{m}v_{m}$ and suppose it equals $0$. We have 
> $$
> a_{1}(\lambda_{1}-\lambda_{2})^n\cdot\dots \cdot(\lambda_{1}-\lambda_{m})^nw=0
> $$
> Therefore, we have $a_{1}=0$. Repeat this fashion, we can get $a_{i}=0$ for $i=1,\dots,m$
> 
> $\blacksquare$
> 

> [!info]  A basis of generalized eigenvectors
> Suppose $V$ is a complex [[Math/Linear Algebra Done Right/Vector Space\|vector space]] and $T\in \mathcal{L}(V)$. Then there is a basis of $V$ consisting of generalized eigenvectors of $T$.
> 
> Proof:
> 
> Because the direct sum of all [[Math/Linear Algebra Done Right/Generalized Eigenspace\|genearlized eigenspaces]] equals the vector space, pick a basis for every eigespace and put them together to form a basis of $V$.


