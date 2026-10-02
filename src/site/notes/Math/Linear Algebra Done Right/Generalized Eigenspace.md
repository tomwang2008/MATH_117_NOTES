---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/generalized-eigenspace/","dg-note-properties":{}}
---

# Generalized Eigenspace
> [!example] Definition of generalized eigenspace
> Suppose $T\in$[[Math/Linear Algebra Done Right/L(V)\|L(V)]] and $\lambda \in \mathbf{F}$. The generalized [[Math/Linear Algebra Done Right/Eigenspace\|eigenspace]] of $T$ corresponding to $\lambda$, denoted $G(\lambda,T)$, is defined to be the set of all [[Math/Linear Algebra Done Right/Generalized Eigenvector\|generalized eigenvectors]] of $T$ corresponding to $\lambda$, along with the $0$ vector.
> 


> [!info]  Description of generalized eigenspaces
> Suppose $T\in \mathcal{L}(V)$ and $\lambda \in \mathbf{F}$. Then $G(\lambda,T)=\text{null }(T-\lambda I)^{\text{dim }V}$.
> 
> Proof:
> 
>Suppose we have the basis of the generalized space $v_{1},\dots,v_{m}$ such that $(T-\lambda I)^{j_{i}}v_{i}=0$ where $i=1,\dots,m$. Among all the $j's$, suppose  $j_{m}$ is the biggest and $j_{1}$ is the smallest. Not hard to see that if $i<m$ we also have $(T-\lambda I)^{j_{m}}v_{i}=0$. And obviously every vector in $\text{null }(T-\lambda I)^{j_{m}}$ is a generalized eigenvector corresponding to $\lambda$. Therefore, we have $G(\lambda ,T)=\text{null }(T-\lambda I)^{j_m}$. 
>
>However, $j_{m}$ might not equal to $\text{dim }V$. Suppose $m$ is smaller than $\text{dim }V$. We have $(T-\lambda I)^{j_{m}}v=(T-\lambda I)^{\text{dim }V}v=0$. So 
> $$
> G(\lambda,T)=\text{null }(T-\lambda I)^{j_{m}}=\text{null }(T-\lambda I)^{\text{dim }V}
> $$
>From the characteristcs of [[Math/Linear Algebra Done Right/Null Spaces\|null space]], we know, $\text{null }(T-\lambda I)^{\text{dim }V}=\text{null }(T-\lambda I)^{\text{dim }V+1}=\dots$ Therefore, for the situation where $j_{m}>\text{dim }V$, The equation above still holds
>
>$\blacksquare$


> [!info]  Description of operators on complex vector spaces
> Suppose [[Math/Linear Algebra Done Right/Vector Space\|$V$]] is a complex vector space and $T\in \mathcal{L}(V)$. Let $\lambda_{1},\dots,\lambda_{m}$ be the distinct eigenvalues of $T$. Then
> 
> (a)$V=G(\lambda_{1},T)\oplus G(\lambda_{2},T)\oplus\dots \oplus G(\lambda_{m},T)$;
> 
> (b) each $G(\lambda j,T)$ is invariant under $T$;
> 
> (c) each $(T-\lambda_{j}I)\big|_{G(\lambda_{j},T)}$ is [[Math/Linear Algebra Done Right/Nilpotent\|nilpotent]];
> 
> Proof:
> 
> (b) and (c) should be trivial, now we prove (a).
> 
> The sum of generalized eigenspaces is a direct sum, suppose $v_{i}\in G(\lambda_{i},T)$ and $v_{j}\in G(\lambda_{j},T)$ are generalized eigenvectors. Then $a_{i}v_{i}+a_{j}v_{j}=0$ if and only if $a_{i}=a_{j}=0$ because generalized eigenvectors are [[Math/Linear Algebra Done Right/Linear Independence\|linearly independent]].
> 
> To prove the sum equals the whole space, we start with 
> $$
> V=\text{null }(T-\lambda_{1}I)^{\text{dim }V}\oplus \text{range }(T-\lambda_{1}I)^{\text{dim }V}
> $$
> We want to prove $G(\lambda_{2},T)\subset \text{range }(T-\lambda_{1}I)^{\text{dim V}}$. Suppose $v\in G(\lambda_{2},T)$ such that $v=u_{1}+u_{2}$ where $u_{1}\in \text{null }(T-\lambda_{1}I)^{\text{dim }V}$ and $u_{2}\in \text{range }(T-\lambda_{1}I)^{\text{dim }V}$. Then 
> $$
> 0=(T-\lambda_{2}I)^{\text{dim }V}u_{1}+(T-\lambda_{2}I)^{\text{dim }V}u_{2}
> $$
> Since both $\text{null }(T-\lambda_{1}I)^{\text{dim }V}$ and $\text{range }(T-\lambda_{1}I)^{\text{dim }V}$ is invariant under $(T-\lambda_{2}I)^{\text{dim V}}$ . We get 
> $$
> 0=w_{1}+w_{2}
> $$
> where $(T-\lambda_{1}I)^{\text{dim V}}u_{1}=w_{1}$ and $(T-\lambda_{1}I)^{\text{dim V}}u_{2}=w_{2}$. Because the sum of range and null space is a direct sum, we know $w_{1}=w_{2}=0$. So $(T-\lambda_{2}I)^{\text{dim }V}u_{1}=w_{1}=0$. Also $(T-\lambda_{2}I)^{\text{dim }V}$ is injective on $\text{null }(T-\lambda_{1}I)^{\text{dim }V}$, we have $u_{1}=0$. Therefore, 
> $$
> G(\lambda_{2},T)\subset \text{range }(T-\lambda_{1}I)^{\text{dim V}}
> $$
> Continue this fashion we will get $V=G(\lambda_{1},T)\oplus G(\lambda_{2},T)\oplus\dots \oplus G(\lambda _{m},T)\oplus U$. Now we prove $U=\{ 0 \}$. Suppose $U\neq \{ 0 \}$. Then $T$ on $U$ has an eigenvalues. Since $\lambda_{1},..,\lambda _m$ is all the eigenvalue that $T$ has, Therefore, this eigenvalue has to be $\lambda_{j}$ where $j\in \{ 1,..,m \}$. Therefore, $U\cap G(\lambda_{j},T)\neq \{ 0 \}$. This contradics the sum between $U$ and $G(\lambda_{j},T)$ is a direct sum. Therefore, $U=\{ 0 \}$ 
> 
> $\blacksquare$


