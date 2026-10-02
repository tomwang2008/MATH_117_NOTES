---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/p-f/","dg-note-properties":{"mathLink":"$\\mathcal P (\\mathbf F)$"}}
---


# $\mathcal{P}(\mathbf F)$

>[!example] Definition of $\mathcal P(\mathbf F)$
>$\mathcal P(\mathbf F)$ is the set of all [[Math/Linear Algebra Done Right/Polynomial\|Polynomial]]s in $\mathbf F$

Based on the definition above, it's natural to wonder what if there is a maximum degree in the set.

>[!example] Definition of $\mathcal P_n (\mathbf F)$
>For a non negative integer $n$, $\mathcal P_n (\mathbf F)$ denotes all the polynomials with coefficients in $\mathbf F$ which have a degree of at most $n$


The following two statements should be intuitive:

>[!info] $\mathcal P_n (\mathbf F)$ is a [[Math/Linear Algebra Done Right/Finite-dimensional Vector Space\|Finite-dimensional Vector Space]]
>Proof:
>
>Notice that span$(1,z,\dots,z^m)=\mathcal P_m (\mathbf F)$. Thus by definition, $\mathcal P_m (\mathbf F)$ is a finite-dementional vector space
>
>$\blacksquare$

>[!info] $\mathcal{P}(\mathbf F)$ is a [[Math/Linear Algebra Done Right/Infinite-dimensional Vector Space\|Infinite-dimensional Vector Space]]
>
>Proof:
>
>For any list of vectors that has a highest degree of n, there will always be a vector $v^{n+1}$ that this vector is not in the span of 
>vectors.
>
>$\blacksquare$


