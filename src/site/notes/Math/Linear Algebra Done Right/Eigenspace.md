---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/eigenspace/","dg-note-properties":{}}
---

# Eigenspace
>[!example] Definition of eigenspace $E(\lambda,T)$
>Suppose [[Math/Linear Algebra Done Right/Linear Map\|$T$]]$\in$[[Math/Linear Algebra Done Right/L(V)\|L(V)]] and $\lambda \in \mathbf{F}$. The eigenspace of $T$ corresponding to $\lambda$, denoted $E(\lambda,T)$, is defined by
> $$
> E(\lambda,T)=\text{null }(T-\lambda I)
> $$

<span style="color:rgb(255, 192, 0)">Notice</span><span style="color:rgb(255, 192, 0)">:</span> Here $\lambda$ is not necessary an [[Math/Linear Algebra Done Right/Eigenvalue\|Eigenvalue]], $\lambda$ can be any number.

>[!info] Sum of eigenspaces is a direct sum
>Suppose [[Math/Linear Algebra Done Right/Vector Space\|$V$]] is [[Math/Linear Algebra Done Right/Finite-dimensional Vector Space\|finite-dimensional]] and $T\in \mathcal{L}(V)$. Suppose also that $\lambda_{1},\dots,\lambda_{m}$ are distinct eigenvalue of $T$. Then 
> $$
> E(\lambda_{1},T)+\dots+E(\lambda_{m},T)
> $$
> is a [[Math/Linear Algebra Done Right/Direct Sum\|Direct Sum]]. Further more, 
>  $$
>  \text{dim }E(\lambda_{1},T)+\dots+\text{dim }E(\lambda_{m},T)\leq \text{dim }V
> $$
> Proof:
> 
> To prove the sum is a direct sum is equivalent to prove
> $$
> u_{1}+\dots+u_{m}=0
> $$
> if and only if $u_{1}=\dots=u_{m}=0$ where $u_{j}\in E(\lambda_{j},T)$. This is true since $\lambda_{j}$ is an eigenvalue of $T$ and therefore, $u_{1},\dots,u_{m}$ are [[Math/Linear Algebra Done Right/Linear Independence\|linearly independent]].
> 
> $E(\lambda_{j},T)=\text{null }(T-\lambda I)=\text{span }(v_{j,1},\dots,v_{j,i})$ where $v_{j,1},\dots,v_{j,i}$ are the corresponding [[Math/Linear Algebra Done Right/Eigenvector\|Eigenvector]] of $\lambda_{j}$. Since $v_{1,.},\dots v_{m,.}$ are linearly independent, and the length of the list of linearly lindependent vectors is smaller than the length of a basis, we have 
> $$
>  \text{dim }E(\lambda_{1},T)+\dots+\text{dim }E(\lambda_{m},T)\leq \text{dim }V
> $$
> $\blacksquare$


