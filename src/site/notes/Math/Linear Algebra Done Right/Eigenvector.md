---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/eigenvector/","dg-note-properties":{}}
---

# Eigenvector

>[!example] Definition of eigenvector
>Suppose [[Math/Linear Algebra Done Right/Linear Map\|$T$]] $\in$ [[Math/Linear Algebra Done Right/L(V)\|L(V)]] and $\lambda \in \mathbf{F}$ is an [[Math/Linear Algebra Done Right/Eigenvalue\|eigenvalue]] of $T$. A vector $v\in V$ is called an eigenvector of $T$ corresponding to $\lambda$ if $v\neq 0$ and $Tv=\lambda v$.
>

>[!info] Linearly independent eigenvectors
>Let $T\in \mathcal{L}(V)$. Suppose $\lambda_{1},\dots,\lambda_{m}$ are distinct [[Math/Linear Algebra Done Right/Eigenvalue\|eigenvalues]] of $T$ and $v_{1},\dots,v_{m}$ are corresponding eigenvectors. Then $v_{1},\dots,v_{m}$ are [[Math/Linear Algebra Done Right/Linear Independence\|linearly independent]].
>
>Proof:
>
>Suppose that $v_{1},\dots,v_{m}$ are linearly dependent. Then we have 
> $$
> v_{1}=a_{2}v_{2}+\dots+a_{m}v_{m}
> $$ 
> Without losing of generality, we may assume $a_{j}\neq 0$. Since not all $a_{j}$ are $0$.
>  
> Apply $T$ on both sides of the equation, we get 
> $$
> \lambda_{1}v_{1}=\lambda_{2}a_{2}v_{2}+\dots+\lambda_{m}a_{m}v_{m}
> $$
> Substituting the left-hand side with the linear combination and simplifying the equation, we get
> $$
> (\lambda_{1}-\lambda_{2})a_{2}v_{2}+\dots+(\lambda_{1}-\lambda_{m})a_{m}v_{m}=0
> $$
> Since $\lambda_{1},\dots \lambda_{m}$ are distinct values, we could repeat the process above over and over, until there are only two vectors left. Apply the process above again we get
> $$
> \lambda_{m-1}y_{m}v_{m}=\lambda_{m}y_{m}v_{m}
> $$
> Therefore, not all $\lambda_{j}$ are distinct which contradicts the condition in the problem.
> 
> $\blacksquare$

<span style="color:rgb(188, 145, 16)">Notice:</span>  This only mean that eigenvectors corresponding to different eigenvalues are linearly independent, eigenvetors corresponding to the same eigenvalue can also be linearly independent.
