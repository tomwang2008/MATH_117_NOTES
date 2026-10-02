---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/sum-of-subspace/","dg-note-properties":{}}
---

# Sum of Subspaces

When we are dealing with vector spaces, we are more interested in subspaces. Therefore it's important for us to understand the operations on subspaces

> [!example] Sum of subsets
> Suppose $U_1 \dots U_n$ are subsets of $V$, the sum of $U_1 \dots U_n$ denoted $U_1 + \dots U_n$ is the set of all posible sums of elements in $U_1 \dots U_n$
> $$ U_1+\dots+U_n=\lbrace u_1+\dots+u_n\ :\ u_1\in U_1 \dots u_n\in U_n\rbrace$$

Notice that a subspace is also a subset of the vector space, therefore the definition above works for subspace too.

The following property reveals that the sum of subspace is in fact the smallest subspace that contains all the summands

> [!info] $U_1+\dots +U_n$ is the smallest subspace that contains $U_1\dots U_n$
> Proof:
> Say we want to construct the smallest subspace that contains $U_1\dots U_n$. It has to contian the additive identity and closed under addition and scalar multiplication.
> 
> Simply taking the union of all subspaces will satisfy additive identity and closed under scalar multiplication.
> 
> But to let the subset become a subspace, we also need to ensure this subset is closed under addition. Thus, all the possible sum of elements in $U_1\dots U_n$ has to be in the subset.
> 
> Thus the subspace we have is exactly $U_1+\dots +U_n$
> $\blacksquare$
> 



