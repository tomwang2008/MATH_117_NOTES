---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/block-diagonal-matrix/","dg-note-properties":{}}
---

# Block Diagonal Matrix
> [!example] Definition of block diagonal matrix
> A block [[Math/Linear Algebra Done Right/Diagonal Matrix\|diagonal matrix]] is a sqaure [[Math/Linear Algebra Done Right/Matrices\|matrix]] of the form 
> $$
> \begin{pmatrix}
A_{1} &  & 0 \\
 & \ddots &   \\
0 &  & A_{m}
\end{pmatrix}
> $$
> where $A_{1},\dots,A_{m}$ are square matrices lying along the [[Math/Linear Algebra Done Right/Diagonal of a Matrix\|diagonal]] and all the other entries of the matrix equal $0$.



> [!info]  Block diagonal matrix with [[Math/Linear Algebra Done Right/Upper-triangular Matrix\|upper-triangular matrix]].
> Suppose $V$ is a complex [[Math/Linear Algebra Done Right/Vector Space\|vector space]] and $T\in \mathcal{L}(V)$. Let $\lambda_{1},\dots,\lambda_{m}$ be the distinct eigenvalues of $T$, with multiplicities $d_{1},\dots,d_{m}$. Then there is a basis of $V$ with respect to which $T$ has a block diagonal matrix of the form 
> $$
> \begin{pmatrix}
A_{1} &  & 0 \\
 & \ddots &  \\
0 &  & A_{m}
\end{pmatrix}
> $$
> where each $A_{j}$ is a $d_{j}$ -by- $d_{j}$ upper-triangular matrix of the form
> $$
> A_{j}=\begin{pmatrix}
\lambda_{j} &  & * \\
 & \ddots &  \\
0 &  & \lambda_{j}
\end{pmatrix}
> $$
> Proof:
> 
> For each generalized eigenspace $G(\lambda_{j},T)$, easy to see that, there exists a basis such that  $A_{j}$ is the matrix representation of $T\big|_{G(\lambda_{j},T)}$. Since every generalized eigenspace is invariant under $T$, we have 
> $$
> G(\lambda_{j},T\big|_{G(\lambda_{j},T)})=G(\lambda_{j},T)
> $$
> Because the direct sum of generalized eigenspace equals the whole vector space, putting $A_{1},\dots,A_{m}$ together gives us the matrix representation of $T$.
> 
> $\blacksquare$



