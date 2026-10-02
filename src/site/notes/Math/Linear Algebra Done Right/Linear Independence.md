---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/linear-independence/","dg-note-properties":{}}
---

# Linear Independence

> [!example] Definition of Linear Independence
> A list of vectors $v_1, \dots, v_n$ is called **linearly independent** if the only choice of scalars $a_1, \dots, a_n \in \mathbf{F}$ that makes $a_1 v_1 + \dots + a_n v_n = 0$ is $a_1 = \dots = a_n = 0$.

Also, the empty list $( \ )$ is declared to be **linearly independent**.

The following statement is extremely useful, it reveals the relationship between the length of linearly independence list and the length of spanning list (which is the list that [[Math/Linear Algebra Done Right/Span\|spans]] the [[Math/Linear Algebra Done Right/Vector Space\|vector space]]).

>[!info] Linear Independence Lemma
>
>Length of Linearly Independent list $\leq$ Length of Spanning List
>
>Proof:
>First, we prove the lemma: If $B=(v_1,\dots,v_n)$ is a list of vectors and span$(B)=V$, then adding vectors into B will cause the new list $B'$ to be linearly dependent.
>
>If $B$ spans the vector space, then that means any vector in the vector space can be expressed by some linear combination of the vectors in $B.$
>
>Thus, for $v\in V$,where $v=a_1v_1+\dots+a_nv_n$. Now if $B'=(v_1,\dots,v_n,v)$, this list will be linearly dependent because ${0=a_1v_1+\dots+a_nv_n+(-1)v}$, since we have none zero coefficient so the list is linearly dependent.
>
>Let $(u_1,\dots,u_n)$ be a linearly independent list and let $(w_1,\dots,w_m)$ be a list that spans the vector space. We want to prove that $n\leq m$.
>We add $u_1$ into the list $(w_1,\dots,w_m)$ and we have a new list $(u_1,w_1,\dots,w_m)$ from the lemma above this list is linearly dependent. The [[Math/Linear Algebra Done Right/Linear Dependence\|linear dependence lemma]] tells us that we can remove one vector in the list and guarantee the list still spans the vector space. Because $u_1\notin \text{span}(\emptyset)$, thus, the vector we removed must be in $(w_1,\dots,w_m)$.
>
>For the $j^{\text{th}}$ turn, we add $u_j$ in the list and remove one of the remaining $w's$ in the list because $u_j\notin \text{span}(u_1,\dots,u_{j-1})$.
>
>There must be more $w's$ than $u's$ because if we've replaced every $w$ with $u$ and we have $u's$ left, then we could add another $u$ into the list, from the lemma the new we formed has to be linearly dependent,but the list $(u_1,\dots,u_n)$ is linearly independent. 
>
>$\blacksquare$









