---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/basis/","dg-note-properties":{}}
---

# Basis

>[!example] Definition of Basis
>A basis is a list of vectors in [[Math/Linear Algebra Done Right/Vector Space\|V]] that is [[Math/Linear Algebra Done Right/Linear Independence\|linearly independent]] and [[Math/Linear Algebra Done Right/Span\|spans]] V

>[!info] Criterion for a basis
>A list $(v_1,\dots,v_n)$ is called a basis if every vector in V can be uniquely written in the form of:
>$$v=a_1v_1+\dots+a_nv_n$$
>where $a_1,\dots,a_n\in \mathbf F$


This allows us to see why basis is so important. For every vector in the vector space, there is only one way to write it with a given basis.

Now let's see some examples:

- The list $(1,0,\dots,0),(0,1,\dots,0),\dots,(0,\dots,0,1)$ is called a **standard basis** of [[Math/Linear Algebra Done Right/Dimensional Spaces\|Dimensional Spaces]].
- The list $1,z,\dots,z^n$, is a basis of [[Math/Linear Algebra Done Right/P(F)\|$\mathcal P_n(\mathbf F)$]].

The following statement tells us how to find a basis.

>[!info] Every spanning list can be reduced into a basis.
>Proof:
>Let $B$ be any spanning list in V. If $B$ is linearly independent, then by definition, $B$ is a basis of V.
>
>If $B$ is linearly dependent, by [[Math/Linear Algebra Done Right/Linear Dependence\|linear dependence lemma]], we could remove one vector in the list and leave the span unchanged. 
>
>Then, if the new list $B'$ we have is linearly independent, $B'$ is a basis. If not, repeat the process above.
>
>Since $B$ has a finite length, the process will eventually terminate.
>
>$\blacksquare$
>

An easy corollary from the result above is:

>[!info] Every [[Math/Linear Algebra Done Right/Finite-dimensional Vector Space\|finite-dimensional vector space]] has a basis
>Proof:
>
>Since some list of vectors span the vector space, from the statement above, we could always reduce it to make it become a basis.
>
>$\blacksquare$

A basis could be constructed in many ways, here is another way.

>[!info] Linearly independent list extends to a basis.
>Let $(v_1,\dots,v_m)$ be a linearly independent list, if span$(v_1,\dots,v_m)\not = V$, we could pick $v_{m+1} \notin \text{span}(v_1,\dots,v_m)$ and add $v_{m+1}$ into the list. The new list is still linearly independent.
>
>The process above will eventually terminate because the length of the linearly independent list is smaller than the length of spanning list. When the process terminates, the new list we have must be a spanning list because we cannot add another $v$ into the list. This means that any vector could be written in the form of some [[Math/Linear Algebra Done Right/Linear Combination\|linear combination]] of the list.
>
>$\blacksquare$


From the statement above, we could infer that every subspace could be paired with another subspace to form the whole vector space.

>[!info] Every subspace of a finite-dimensional vector space is part of the [[Math/Linear Algebra Done Right/Direct Sum\|direct sum]] equal to $V$
>Suppose $V$ is a finite-dimensional vector space and $U$ is a subspace of $V$, then there exists a subspace $W$ such that $U\bigoplus W=V$
>
>Proof:
>
>Because $U$ is subspace of a $V$, $U$ is finite-dimensional. Thus, $U$ has a basis. 
>
>Let the basis be $B=(v_1,\dots,v_m)$. Since the list $B$ is linearly independent, from the statement above, $B$ can be extended to a basis of $V$. 
>
>Let the extended list be $B'=(v_1,\dots,v_m,\dots,v_n)$ we pick $(v_{m+1}, \dots,v_n)$ and let $W=\text{span}(v_{m+1}, \dots,v_n)$. 
>
>Easy to verify $U+W=V$. Also, because the list $(v_1,\dots,v_m,\dots,v_n)$ is linearly independent, $0$ can be written uniquely in the form of $0=0+\dots+0$. Thus, in $U+W$ the only way to write $0$ is $0+0$. This implies that $U+W=V$ is a direct sum.
>
>$\blacksquare$


The following statement is crucial for us to define [[Math/Linear Algebra Done Right/Dimension\|dimension]].

>[!info] Basis length does not depend on basis
>Any two bases of a [[Math/Linear Algebra Done Right/Finite-dimensional Vector Space\|finite-dimensional vector space]] have the same length
>
>Proof:
>
>Let $B',B$ be two bases of a finite-dimensional vector space $V$. If the length of $B'$ is smaller than $B$, by the [[Math/Linear Algebra Done Right/Linear Independence\|linear independence lemma]], $B$ cannot be linearly independent. By symmetry the length of $B$ cannot be smaller than $B'$ either. Thus, the two bases must have the same length.
>
>$\blacksquare$

The following statement tells us about the relationship between linearly independent list and basis.

>[!info] Every linearly independent list of the right length is a basis.
>Suppose $V$ is finite-dimensional. Then every linearly independent list in $V$ with the length of $\dim V$ is a basis of $V$.
>
>Proof:
>
>Let $B$ be any linearly independent list with the length of $\dim V$. If $\text{span}(B)$ does not span the whole vector space, then we can find another vector $v\notin \text{span}(B)$ and we add $v$ into $B$ to form $B'$ such that $B'$ is linearly independent. 
>
>But the [[Math/Linear Algebra Done Right/Linear Independence\|linear independence lemma]] tells us that:
> 
>$$\text{the length of linear independent list} \leq \text{length of basis} =\dim V \leq \text{length of spanning list.}$$ 
>
>Thus, the list should $B'$ not linearly independent. There is a contradiction so no such $v$ exists. Thus, any linearly independent list $B$ with the length of $\dim V$ is a basis of $V$
>
>$\blacksquare$


Conversely, every spanning list of the right length is a basis is also true.

>[!info] Spanning list of the right size is a basis
>Suppose $V$ is finite-dimensional, every spanning list with the length of $\dim V$ is a basis.
>
>Proof:
>
>If the spanning list is not linearly independent, then by [[Math/Linear Algebra Done Right/Linear Dependence\|linear dependence lemma]], we could remove one vector and leave the span to be the same. Repeat the process until the list become linearly independent.
>
>Now we have a list that spans the vector space and is linearly independent with a length of something smaller than $\dim V$. However, any basis of the vector space should have the same length. Therefore, there is a contradiction. This implies that no such list exists.
>
>$\blacksquare$
>


