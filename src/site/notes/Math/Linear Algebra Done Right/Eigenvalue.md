---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/eigenvalue/","dg-note-properties":{}}
---

# Eigenvalue

>[!example] Definition of eigenvalue
>Suppose [[Math/Linear Algebra Done Right/Linear Map\|$T$]] $\in$ [[Math/Linear Algebra Done Right/L(V)\|L(V)]]. A number $\lambda \in \mathbf{F}$ is called an eigenvalue of $T$ if there exist a vector $v\in$ [[Math/Linear Algebra Done Right/Vector Space\|$V$]] such that $v \neq 0$ and $Tv=\lambda v$.

>[!info] Equivalent conditions to be an eigenvalue
>Suppose $V$ is [[Math/Linear Algebra Done Right/Finite-dimensional Vector Space\|finite-dimensional]], $T\in \mathcal{L}(V)$, and $\lambda \in \mathbf{F}$. Then the followings are equivalent.
> 
>(a) $\lambda$ is an eigenvalue of $T$.
>(b) $T-\lambda I$ is not [[Math/Linear Algebra Done Right/Injectivity\|injective]].
>(c) $T-\lambda I$ is not [[Math/Linear Algebra Done Right/Surjectivity\|surjective]].
>(d) $T-\lambda I$ is not [[Math/Linear Algebra Done Right/Invertible\|inverible]].
>
>Proof:
>
> Firstly, if $\lambda$ is an eigenvalue of $T$, then, $T-\lambda I$ is not injective, since $v\in \text{null }T-\lambda I$. Because $T-\lambda I$ is not injective, it's also not surjective and invertible.
> 
> If $T-\lambda I$ is not injective, then there exist $v\in \text{null }T-\lambda I$, where $v\neq 0$. Now we have $(T-\lambda I)(v)=0$, which is $Tv=\lambda v$. Therefore, $\lambda$ is an eigenvalue of $T$. Also, $T-\lambda I$ is not injective implies it's not surjective and invertible.
> 
> For (c) and (d), they are the same as (b) since they all imply each other.
> 
> $\blacksquare$


>[!info] Numbers of eigenvalues
>Suppose $V$ is finite-dimensional. Then each operator on $V$ has at most $\text{dim }V$ distinct eigenvalues.
>
>Proof:
>
>Every distinct eigenvalue of the operator has a unique [[Math/Linear Algebra Done Right/Eigenvector\|eigenvector]], and these vectors are [[Math/Linear Algebra Done Right/Linear Independence\|linearly independent]]. Since the length of lists of linearly independent vectors are smaller than the length of the list of spanning list. We get the desired.
>
>$\blacksquare$


>[!info] Every operator on a complex vector space has an eigenvalue
>Every operator on a [[Math/Linear Algebra Done Right/Finite-dimensional Vector Space\|finite-dimensional]], nonzero, complex [[Math/Linear Algebra Done Right/Vector Space\|vector space]] has at least one eigenvalue.
>
>Proof:
>
>Let $V$ be the vector space that has a dimension of $n$ and $v\in V$, $T\in \mathcal{L}(V)$. Consider a list of vectors $(v,Tv,T^2v,\dots,T^nv)$. Since the list has $n+1$ vectors inside, so this list has to be [[Math/Linear Algebra Done Right/Linear Dependence\|linearly dependent]]. Therefore, there exist $a_{j}\in \mathbf{F}$,not all $0$, such that 
> $$
> 0=(a_{0}I+a_{1}T+a_{2}T^2+\dots+a_{n}T^n)v
> $$
> By the fundamental theorem of algebra, we could rewrite the equation above into 
> $$
> (T-\lambda_{1}I)(T-\lambda_{2}I)\dots(T-\lambda_{n}I)(v)=0
> $$
> Thus, among all the $\lambda_{j}'s$, there exist at least one $\lambda_{i}$ such that $T-\lambda_{i}I$ is not injective. Thus, $\lambda_{i}$ is an eigenvalue of $T$
> 
> $\blacksquare$

>[!info] Determination of eigenvalues from [[Math/Linear Algebra Done Right/Upper-triangular Matrix\|Upper-triangular Matrix]]
>Suppose $T\in \mathcal{L}(V)$, and has an upper-triangular matrix with respect to some [[Math/Linear Algebra Done Right/Basis\|Basis]] of $V$. Then the eigenvalues of $T$ are precisely all the entries on the [[Math/Linear Algebra Done Right/Diagonal of a Matrix\|diagonal]] of the matrix.
>
>Proof:
>
>Let $A$ be the upper-trigonal matrix of $T$, $I$ is the identity matrix and $\lambda_{1},\dots,\lambda_{n}$ are the entries on the diagonal. 
>
>Consider every $M_{j}=A-\lambda_{j}I$. Since now there is at least one $0$ on the entries on the diagonal of the matrix $M$. The new linear map represented by $M$ is not surjective (see [[Math/Linear Algebra Done Right/Upper-triangular Matrix\|Upper-triangular Matrix]]), therefore, every $\lambda_{j}$ is an eigenvalue.
>
>If there exists a new eigenvalue $\Lambda$ that is not on the diagonal, then $A-\Lambda I$ should not be surjective. However, since $\Lambda$ is different than any $\lambda_{j}$, $\Lambda-\lambda_{j}\neq0$ for $j=1,\dots,n$. This implies that $T-\Lambda I$ is invertible. The conclusion contradicts our assumption. 
>
>Therefore, all the entries on the diagonal of the matrix are precisely all the eigenvalues.
>
>$\blacksquare$

>[!info] Eigenvalue of an operator is also an eigenvalue of the polynomial
>Suppose $\mathbf{F}=\mathbb{C}$, $p \in \mathcal{P}(\mathbf{F})$ and $\alpha \in \mathbb{C}$. Prove that $\alpha$ is an eigenvalue of $p(T)$ if and only if $\alpha=p(\lambda)$ for some eigenvalue $\lambda$ of $T$.
>
>Proof:
>Any $v$ appears in the prove is claimed non-zero.
>
>If $\lambda$ is an eigenvalue of $T$, obviously, $\alpha=p(\lambda)$ is an eigenvalue of $p(T)$.
>
>If $\alpha$ is an eigenvalue of $p(T)$, then, we have $(p(T)-\alpha I)v=0$. For an operator $T$ and its eigenvalues $\lambda_{1},\dots ,\lambda_{m}$, there exists a unique polynomial $q=\prod_{j\in S}(z-\lambda_{j})^i$ for every $v\in V$ where $S$ is a subset of $\{ 1,\dots,m \}$ and $i\in \{ 1,\dots,n \}$  such that $q(T)v=0$. 
>
>Therefore, in the polynomial ring, $p(z) - \alpha$ is divisible by $q(z)$, which means **$p(z) - \alpha = n(z)q(z)$**. Substitute the scalar $z = \lambda_j$. Since $q(\lambda_j) = 0$, we get **$p(\lambda_j) - \alpha = 0$**, which means $\alpha = p(\lambda_j)$.
>
>$\blacksquare$

<span style="color:rgb(255, 192, 0)">Notice:</span> The conclusion above only works when $\mathbf{F}=\mathbb{C}$, when $\mathbf{F}=\mathbb{R}$ the conclusion does not hold.



> [!info]  Operator on odd-dimension vector space has eigenvalue
> Every operator on an odd-dimensional real vector space has an eigenvalue.
> 
> Proof:
> 
> See the note [[Math/Linear Algebra Done Right/Complexification\|complexification]], we know that every [[Math/Linear Algebra Done Right/Operator\|operator]] $T$ has am [[Math/Linear Algebra Done Right/Invariant Subspace\|invariant subspace]] with a dimension of 1 or 2. Let the subspace be $U$, we have $V=U\oplus V_{1}$. $V_{1}$ is invariant undet $T$, therefore, we can find a new subspace $U_{1}$ that is invariant under $T$ with a dimension 1 or 2. 
> 
> Continuing this fashion, we get $V$ being rewritten as a seireis of direct sum with dimension 1 or 2. Because $V$ is odd, the subspaces cannot be all ever, therefore, there exists a subspace $U_{j}$ that is 1-dimensional. Thus, $T$ has an eigenvalue. 
> 
> $\blacksquare$



