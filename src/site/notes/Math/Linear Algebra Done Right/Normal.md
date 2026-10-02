---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/normal/","dg-note-properties":{}}
---

# Normal
> [!example] Definition of normal
> An [[Math/Linear Algebra Done Right/Operator\|operator]] on an [[Math/Linear Algebra Done Right/Inner Product\|inner product]] space is called normal if it commutes with its [[Math/Linear Algebra Done Right/Adjoint\|adjoint]].
> 
> In other words, $T\in$[[Math/Linear Algebra Done Right/L(V)\|L(V)]] is normal if 
> $$
> TT^*=T^*T
> $$

> [!info]  $T$ is normal if and only if $\lVert Tv \rVert=\lVert T^*v \rVert$ for all $v$
> An operator $T\in \mathcal{L}(V)$ is normal if and only if
> $$
> \lVert Tv \rVert =\lVert T^*v \rVert 
> $$
> for all $v\in V$.
> 
> Proof:
> 
> If $T$ is normal, then we have $\langle TT^*v,v \rangle=\langle T^*Tv,v \rangle$. Which is $\langle Tv,Tv \rangle=\langle T^*v,T^*v \rangle\iff \lVert Tv \rVert=\lVert T^*v \rVert$.
> 
>  If $\lVert Tv \rVert=\lVert T^*v \rVert$, we have $\langle TT^*v,v \rangle=\langle T^*Tv,v \rangle$. Which is $\langle (TT^*-T^*T)v,v \rangle=0$. From the conclusion above, we have $TT^*=T^*T$. (For sure $TT^*-T^*T$ is [[Math/Linear Algebra Done Right/Self-Adjoint\|self-adjoint]])
>  
>  $\blacksquare$

> [!info]  For $T$ normal, $T$ and $T^*$ have the same [[Math/Linear Algebra Done Right/Eigenvector\|eigenvectors]].
> Suppose $T\in \mathcal{L}(V)$ is normal and $v\in V$ is an eigenvector of $T$ with [[Math/Linear Algebra Done Right/Eigenvalue\|eigenvalue]] $\lambda$. Then $v$ is also an eigenvector of $T^*$ with eigenvalue of $\overline{\lambda}$.
> 
> Proof:
> $$
> \lVert (T-\lambda I)v \rVert =\lVert (T-\lambda I)^*v \rVert =\lVert (T^*-\overline{\lambda}I)v \rVert =0
> $$
> $\blacksquare$



> [!info]  [[Math/Linear Algebra Done Right/Orthogonal\|Orthogonal]] [[Math/Linear Algebra Done Right/Eigenvector\|eigenvectors]] for normal operators
> 
> Suppose $T\in \mathcal{L}(V)$  is normal. Then eigenvectors of T corresponding to distinct eigenvalues are [[Math/Linear Algebra Done Right/Orthogonal\|orthogonal]].
> 
> Proof:
> 
> Let $Tv_{j}=\lambda_{j}v_{j}$ for all $j=1,\dots,n$. Therefore, we have $T^*v_{j}=\overline{\lambda _{j}}v_{j}$. 
> $$
\langle Tv_{j},v_{i} \rangle = \langle \lambda_{j}v_{j},v_{i} \rangle=\langle v_{j},\overline{\lambda_{i}}v_{i}\rangle
> $$ 
> Now we have $(\lambda_{j}-\overline{\lambda_{i}})\langle v_{j},v_{i} \rangle=0$. Since $\lambda_{j}\neq \overline{\lambda_{i}}$, we have $\langle v_{j},v_{i} \rangle=0$, which leads to $v_{j},v_{i}$ are orthogonal.
> 
>$\blacksquare$

> [!info]  Normal but not sel-adjoint operators
> Suppose $V$ is a 2-dimensional real [[Math/Linear Algebra Done Right/Inner Product Space\|inner product space]] and $T\in \mathcal{L}(V)$. Then the followings are equivalent.
> 
> (a) $T$ is normal but not self-adjoint
> 
> (b) The matrix of $T$ with respect to every orthonormal basis of $V$  has the form
> $$
> \begin{pmatrix}
a & b \\
-b & a
\end{pmatrix}
> $$
> with $b\neq0$
>
>(c) The matrix of $T$ with respect to some orthonormal basis of $V$ has the form
> $$
> \begin{pmatrix}
a & b \\
-b & a
\end{pmatrix}
> $$
> with $b>0$
> 
> Proof:
> 
> (b) and (c) are trivially equivalent, therefore, we prove (a) and (b) are equivalent.
> 
> Suppose (a) holds, we have a normal operator $T$. Since $T$ is normal, we have $\lVert Te_{1} \rVert^2=\lVert T^*e_{1} \rVert^2$, where $e_{1},e_{2}$ is a orthonormal basis of $V$. Suppose 
> $$
> \mathcal{M}(T)=\begin{pmatrix}
a & b \\
c & d
\end{pmatrix}
> $$
> and
> $$
> \mathcal{M}(T^*)=\begin{pmatrix}
a & c \\
b & d 
\end{pmatrix}
> $$
> We have $a^2+b^2=a^2+c^2$. Therefore, we have $\lvert b \rvert=\lvert c \rvert$. 
> 
> If $b=c$ then $T$ is self-adjoint, which does not satisfy our condition, therefore $b=c$. To satisfy the condition that $T$ is normal, by computation we get $a=d$. Therefore
> $$
> \mathcal{M}(T)=\begin{pmatrix}
a & b \\
-b & a 
\end{pmatrix}
> $$
> Suppose (b) holds, (a) obviously holds.
> 
> $\blacksquare$




> [!info]  Normal operators and and invariant subspaces
>  Suppose $V$ is an inner product space, $T\in \mathcal{L}(V)$ is normal, and $U$ is a invariant under $T$. Then
>  
>  (a) $T$ is invariant under $U^\perp$
>  
>  (b) $T^*$ is invariant under $U$
>  
>  (c) $(T\big|_{U})^*=T^*\big|_{U}$
>
> (d) $T\big|_{U}\in \mathcal{L}(U)$ and $T\big|_{U^\perp}\in \mathcal{L}(U^\perp)$ are normal operators.
> 
> Proof:
> 
> We prove (a) first. 
> 
> Suppose $V$ is an inner product space, $T$ is normal, and $U$ is a subspace of $V$ that is invariant under $T$.
>
Let $e_1, \dots, e_m$ be an orthonormal basis of $U$, and extend it to an orthonormal basis $e_1, \dots, e_m, e_{m+1}, \dots, e_n$ of $V$. Since $U$ is invariant under $T$, mapping any basis vector of $U$ results only in a linear combination of vectors in $U$. Suppose the block matrix representation is
>
$$\mathcal{M}(T) = \begin{pmatrix} A & B \\ 0 & C \end{pmatrix}$$
>
where $A$ represents the action on $U$, and $C$ represents the action on $U^\perp$. By taking the conjugate transpose, we have
>
$$\mathcal{M}(T^*) = \begin{pmatrix} A^* & 0 \\ B^* & C^* \end{pmatrix}$$
>
Since $T$ is normal, $TT^* = T^*T$, which implies $\mathcal{M}(T)\mathcal{M}(T^*) = \mathcal{M}(T^*)\mathcal{M}(T)$. By computation of the top-left block of both matrix products, we get
>
$$AA^* + BB^* = A^*A$$
>
Taking the trace of both sides, we have $\text{tr}(AA^*) + \text{tr}(BB^*) = \text{tr}(A^*A)$. Since $\text{tr}(AA^*) = \text{tr}(A^*A)$ for any square matrix $A$, we get $\text{tr}(BB^*) = 0$.
>
The trace of $BB^*$ is the sum of the absolute squares of all entries in $B$. To satisfy $\text{tr}(BB^*) = 0$, we must have $B = 0$. Therefore
>
$$\mathcal{M}(T) = \begin{pmatrix} A & 0 \\ 0 & C \end{pmatrix}$$
>
Because the top-right block is $0$, applying $T$ to any basis vector in $U^\perp$ (which correspond to the rightmost columns) yields only a linear combination of basis vectors in $U^\perp$. Therefore, $U^\perp$ is invariant under $T$.
>
>The others should be trivial.
>
$\blacksquare$

> [!info]  Characterization of normal operators when $\mathbf{F}=\mathbb{R}$
> Suppose $V$ is a real inner product spaec and $T\in \mathcal{L}(V)$. Then the following are equivalent.
> 
> (a) $T$ is normal
> 
> (b) There is an orthonormal basis of $V$ with respect to which $T$ has a [[Math/Linear Algebra Done Right/Block Diagonal Matrix\|block diagonal matrix]] such that each block is a 1-by-1 matrix or a 2-by-2 matrix of the form 
> $$
> \begin{pmatrix}
a & -b \\
b & a 
\end{pmatrix}
> $$
> with $b>0$.
> 
> Proof:
> 
> Suppose (a) holds. Let $U$ be the invariant subspace of $T$ which has a [[Math/Linear Algebra Done Right/Dimension\|dimension]] of 1 or 2. Therefore, $U^\perp$ is also invariant under $T$. Consider the smaller vector spaec $U^\perp$ and the new operator $T\big|_{U^\perp}\in \mathcal{L}(U^\perp)$. $T\big|_{U^\perp}$ has a invariant subspace $U_{1}$ which is also invariant under $T$. Continuing this fashion, we have $V=U\oplus U_{1}\oplus U_{2}\oplus\dots \oplus U_{i}$. Each of the $U_{j}'s$ has a dimension of 1 or 2. Therefore $T$ has a block diagonal matrix which each block is either 1-by-1 or 2-by-2. Because $T$ is normal, all of the 2-by-2 matrix are of the form of the desired.
> 
> Suppose (b) holds, as you should verify, $T$ is indeed normal.
> 
> $\blacksquare$


 

