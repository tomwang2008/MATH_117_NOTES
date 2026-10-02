---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/rank-of-a-matrix/","dg-note-properties":{}}
---

# Rank of a Matrix

>[!example] Definition of column rank and row rank
>Suppose $A$ is an m-by-n [[Math/Linear Algebra Done Right/Matrices\|matrix]] with entries in $\mathbf{F}$. 
>The row rank is defined as the dimension of span of the rows of $A$. 
>The column rank is defined as the dimension of span of column of $A$.

>[!info] Dimension of $\text{range }T$ equals column rank of $\mathcal{M}(T)$.
>Suppose [[Math/Linear Algebra Done Right/Vector Space\|$V$]] and $W$ are [[Math/Linear Algebra Done Right/Finite-dimensional Vector Space\|finite-dimensional]], and [[Math/Linear Algebra Done Right/Linear Map\|$T$]]$\in$[[Math/Linear Algebra Done Right/L(V,W)\|L(V,W)]]. Then the $\text{dim range }T$ equals the column rank of $\mathcal{M}(T)$.
>
>Proof:
>
>Let $(v_{1},v_{2},\dots,v_{n})$ be a basis of $V$ and $(Tv_{1},Tv_{2},\dots,Tv_{n})$ be the list of vectors after applying $T$ to the basis
>
>From note [[Math/Linear Algebra Done Right/M(v)\|M(v)]] we have $\mathcal{M}(Tv_{k})=\mathcal{M}(T)_{.,k}$, Also since $W$ is [[Math/Linear Algebra Done Right/Isomorphism\|isomorphic]] to $\mathbf{F}^{m,1}$ , we have 
> $$
> \begin{align}
\text{dim span }(\mathcal{M}(T)_{., })&=\text{dim span }(\mathcal{M}(Tv)) \\
&=\text{dim span }(Tv) \\ 
&=\text{dim range }T
\end{align}
> $$
> 
> $\blacksquare$

>[!info] The column rank equals the row rank
>Suppose $A\in \mathbf{F}^{m,n}$ then the row rank of $A$ equals the column rank
>
>Proof:
>
>We know that $\mathcal{M}(T')=\mathcal{M}(T)^{t}$, therefore we have 
> $$
> \text{column rank of }\mathcal{M}(T')=\text{row rank of }\mathcal{M}(T)
> $$
> Also, from the conclusion above, we also know that 
> $$
> \begin{align}
\text{column rank of }\mathcal{M}(T')&=\text{dim range }T' \\
&=\text{dim range }T \\
&=\text{column rank of }\mathcal{M}(T)
\end{align}
> $$
> Therefore, combining the two equations above we have
> $$
> \text{row rank of }\mathcal{M}(T)=\text{column rank of}\mathcal{M}(T)
> $$
> $\blacksquare$

