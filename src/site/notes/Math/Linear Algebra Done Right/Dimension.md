---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/dimension/","dg-note-properties":{}}
---

# Dimension

>[!example] Definition of dimension
>
>The dimension of a [[Math/Linear Algebra Done Right/Finite-dimensional Vector Space\|finite-dimensional vector space]] $V$ is the length of any basis of the vector space.
>
>The dimension of $V$ is denoted $\dim V$

Since every [[Math/Linear Algebra Done Right/Subspace\|subspace]] of a finite-dimensional vector space is finite-dimensional. We should expect the following inequality.

>[!info] Dimension of subspace
>
>If $U$ is a subspace of $V$, then $\dim U\leq\dim V$
>
>Proof:
>
>Let $B$ be a basis of $U$ and $B'$ be a basis of $V$.  Since $U$ is a subspace of $V$, $B$ is a linearly independent list of $V$. By the [[Math/Linear Algebra Done Right/Linear Independence\|linear independence lemma]], $|B|\leq\ |B'|$. Thus, by the definition of dimension, $\dim U\leq \dim V$.
>
>$\blacksquare$

The next result gives us the formula to calculate the dimension of the [[Math/Linear Algebra Done Right/Sum of Subspace\|sum of subspace]]. 

>[!info] Dimension of a sum
>If $U_1,U_2$ are two subspaces of the vector space, then $$\dim(U_1+U_2)=\dim U_1+\dim U_2-\dim(U_1\cap U_2)$$
>
>Proof:
>
>Let $W=U_1\cap U_2$ and $(v_1,\dots,v_k)$ be a basis of the subspace $W$. Since $W\subseteq U_1$ we could extend the list $(v_1,\dots,v_k)$ to be a basis of $U_1$, let the basis be $(v_1,\dots,v_k,u_1\dots,u_m)$. By symmetry, we could also extend the list to be a basis of $U_2$. Let the basis be $(v_1,\dots,v_k,w_1,\dots,w_n)$. 
>
>Therefore, the dimension of $U_1+U_2$ is $(k+m)+(k+n)-n$ that is $\dim U_1+\dim U_2-\dim(U_1\cap U_2)$.
>
>$\blacksquare$


>[!abstract] Notice
>Although the formula looks similar to the formula in set theory. They are not the same thing. The formula above does not work for three or more subspaces.



