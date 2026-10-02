---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/jordan-basis/","dg-note-properties":{}}
---

# Jordan Basis
> [!example] Definition of jordan basis
> Suppose $T\in$[[Math/Linear Algebra Done Right/L(V)\|L(V)]]. A basis of $V$ is called a jordan [[Math/Linear Algebra Done Right/Basis\|basis]] for $T$ if with respect to this basis [[Math/Linear Algebra Done Right/Operator\|$T$]] if with respect to this basis $T$ has a [[Math/Linear Algebra Done Right/Block Diagonal Matrix\|block diagonal matrix]] 
> $$
> \begin{pmatrix}
A_{1} &  & 0 \\
 & \ddots &  \\
0 &  & A_{p}
\end{pmatrix}
> $$
> where each $A_{j}$ is an [[Math/Linear Algebra Done Right/Upper-triangular Matrix\|upper=triangular matrix]] of the form
> $$
> A_{j}=\begin{pmatrix}
\lambda_{j} & 1 &  & 0 \\
 & \ddots & \ddots &  \\
 &  & \ddots & 1 \\
0 &  &  & \lambda_{j}
\end{pmatrix}
> $$


> [!info]  Jordan Form
> Suppose $V$ is a complex vector space. If $T\in \mathcal{L}(V)$, then there is a basis of [[Math/Linear Algebra Done Right/Vector Space\|$V$]] that is a Jordan basis for $T$.
> 
> Proof:
> 
> Every operator on a complex vector spaee can be restricted to its [[Math/Linear Algebra Done Right/Generalized Eigenspace\|general eigenspaces]], which on every general eigenspaec $T$ is [[Math/Linear Algebra Done Right/Nilpotent\|nilpotent]]. Since we have a Jordan basis for every nilpotent oeprator, and every general eigenspace is [[Math/Linear Algebra Done Right/Invariant Subspace\|invariant]] under $T$, putting the Jordan bases together gives us a Jordan basis of $T$.
> 
>$\blacksquare$
>
