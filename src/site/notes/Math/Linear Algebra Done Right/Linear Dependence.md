---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/linear-dependence/","dg-note-properties":{}}
---

# Linear Dependence

Similar as we define infinite-dimensional vector space, linear dependence means not [[Math/Linear Algebra Done Right/Linear Independence\|linearly independent]].

>[!example] Definition of Linear Dependence
>A list of vectors $v_1,\dots,v_n$ in V is linearly dependent if there exists $a_1,\dots,a_n\in \mathbf F$ not all 0, such that, $a_1v_1+\dots+a_nv_n=0$

The following lemma will be often useful. It states that given a linearly dependent list of vectors, we can remove some vector in the list without changing the original [[Math/Linear Algebra Done Right/Span\|span]] of the list.

> [!info] Linear Dependence Lemma
> Suppose list $(v_1, \dots, v_n)$ is linearly dependent then there exists $j \in \{1, \dots, n\}$, such that:
>
> 1. $v_j \in \text{span}(v_1, \dots, v_{j-1})$
> 2. If the $j^{th}$ term is removed from the list the span of the remaining list equals $\text{span}(v_1, \dots, v_n)$
>
> **Proof:**
>
> **Step 1:**
> Since $(v_1, \dots, v_n)$ is linearly dependent, there exist scalars $a_1, \dots, a_n \in \mathbf{F}$, not all 0, such that $a_1v_1 + \dots + a_nv_n = 0$.
> Let $j$ be the largest index such that $a_j \neq 0$.
> Then the equation can be rewritten as:
> $$a_j v_j = -a_1 v_1 - \dots - a_{j-1} v_{j-1}$$
> Dividing by $a_j$ (since $a_j \neq 0$), we see that $v_j \in \text{span}(v_1, \dots, v_{j-1})$.
>
> **Step 2:**
> Suppose $u \in \text{span}(v_1, \dots, v_n)$. Then we can write
> $$u = A_1v_1 + \dots + A_n v_n$$
> Substituting the expression for $v_j$ from step 1 into this equation allows us to write $u$ as a linear combination of the list without $v_j$.
> Thus, removing $v_j$ does not change the span.
> 
> $\blacksquare$







>
>