---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/upper-triangular-matrix/","dg-note-properties":{}}
---

# Upper-triangular Matrix

>[!example] Definition of upper-triangular matrix
>A [[Math/Linear Algebra Done Right/Matrices\|matrix]] is called upper-triangular if all the entries below the [[Math/Linear Algebra Done Right/Diagonal of a Matrix\|diagonal]] equal $0$.

>[!info] Conditions for upper-triangular matrix
>Suppose [[Math/Linear Algebra Done Right/Linear Map\|$T$]]$\in$[[Math/Linear Algebra Done Right/L(V)\|L(V)]], and $v_{1},\dots,v_{n}$ is a [[Math/Linear Algebra Done Right/Basis\|basis]] of [[Math/Linear Algebra Done Right/Vector Space\|$V$]]. Then the followings are equivalent.
>
>(a) the matrix of $T$ with respect to $v_{1},\dots,v_{n}$ is upper-triangular
>
>(b) $Tv_{j}\in \text{span}(v_{1},\dots,v_{j}), \text{for each } j=1,\dots n$
>
>(c) $\text{span }(v_{1},\dots,v_{j})$ is [[Math/Linear Algebra Done Right/Invariant Subspace\|invariant]] under $T$ for each $j=1\dots n$
>
>Proof:
>
>It's clear to see that (a) and (b) are equivalent and (c) implies (b). Since $T$ is a linear map, $v\in \text{span }(v_{1},\dots,v_{j})$ can be written in a [[Math/Linear Algebra Done Right/Linear Combination\|linear combination]] under $v_{1},\dots,v_{j}$. Thus, (b) implies (c)
>
>$\blacksquare$

>[!info] Over $\mathbb{C}$, every [[Math/Linear Algebra Done Right/Operator\|operator]] has an upper-triangular matrix.
>Suppose $V$ is a [[Math/Linear Algebra Done Right/Finite-dimensional Vector Space\|finite-dimensional]] complex vector space and $T\in \mathcal{L}(V)$. Then $T$ has an upper-triangular matrix with respect to some [[Math/Linear Algebra Done Right/Basis\|basis]] of $V$.
>
>Proof:
>
>Because $T$ is on a complex vector space, it's guaranteed to have at least one eigenvalue. Let it be $\lambda_{1}$ and $v_{1}$ is the corresponding eigenvector.
>
>Now consider the [[Math/Linear Algebra Done Right/Quotient Space\|quotient space]] $V/\text{span }(v_{1})$. The [[Math/Linear Algebra Done Right/Quotient operator\|quotient operator]] will have a new eigenvalue on this new quotient space. Let it be $\lambda_{2}$ and $v_{2}$ is the corresponding eigenvalue.
>
>Since $v_{2}$ is an eigenvector on $V/\text{span }(v_{1})$, we have $Tv_{2}=\lambda_{2}v_{2}+cv_{1}$, where $c\in \mathbf{F}$. 
>
>The process can keep continuing, because $V$ is finite-dimensional, the process ends after a finite-number of steps.
>
>$\blacksquare$


>[!info] Determination of [[Math/Linear Algebra Done Right/Invertible\|invertiblilty]] from upper-triangular matrix
>Suppose $T\in \mathcal{L}(V)$ has an upper-triangular matrix with respect to some basis of $V$. Then $T$ is invertible if and only if all the entries on the [[Math/Linear Algebra Done Right/Diagonal of a Matrix\|diagonal]] of the upper-matrix are nonzero.
>
>Proof:
>
>Suppose all the entries on the [[Math/Linear Algebra Done Right/Diagonal of a Matrix\|diagonal]] on the upper-matrix are nonzero. Then, for every  $Tv_{j}=a_{0}+a_{1}v_{1}+\dots+a_{j}v_{j}$, we have  $Tv_{j}\not\in \text{span }(v_{1},\dots,v_{j-1})$. Thus, the list of vector $(Tv_{1},\dots,Tv_{n})$ are [[Math/Linear Algebra Done Right/Linear Independence\|linearly independent]]. So $T$ is [[Math/Linear Algebra Done Right/Surjectivity\|surjective]], which leads to invertible
>
>Suppose $T$ is invertible, if some entries on the diagonal of the upper-matrix are zero. Then we have $Tv_{j}\in \text{span }(v_{1},\dots,v_{j-1})$. Thus, $(Tv_{1},\dots Tv_{j})$ is linearly independent and therefore $(Tv_1,\dots Tv_{n})$ is linearly independent. So $\text{dim span }(Tv_{1},\dots Tv_{n})<\text{dim }V$. This contradicts the condition that $T$ is invertible.
>
>$\blacksquare$



