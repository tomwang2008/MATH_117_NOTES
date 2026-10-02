---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/quotient-space/","dg-note-properties":{}}
---

# Quotient Space

>[!example] Definition of Quotient Space
>Suppose $U$ is a [[Math/Linear Algebra Done Right/Subspace\|subspace]] of [[Math/Linear Algebra Done Right/Vector Space\|$V$]]. Then the quotient space $V/U$ is the set of all [[Math/Linear Algebra Done Right/Affine Subset\|affine subset]] of $V$ that is parallel to $U$. In other words,
> $$
> V/U=\{ v+U\ :\ v\in V \}
> $$

We do hope that the quotient space is a vector space, to prove that, we need to prove the following statement.

> [!info] Two affine subset parallel to $U$ are equal or disjoint
> Suppose $U$ is a subspace of $V$ and $v,w\in V$. Then the followings are equivalent,
> a)  $v-w\in U$
> b)  $v+U=w+U$
> c)  $(v+U)\ \cap\ (w+U)\neq \varnothing$
> 
> Proof:
> 
> If b holds, then a and c are easy to verify.
> 
> If a holds, then for $u\in U$, we have $u+v=(u+(v-w))+w$. Thus, for every element in set $v+U$ we can find one unique element that is equal to it. By similarity, this holds true for $w+U$. Now b is true, easy to verify c is also true.
> 
> If c holds, then there exist $v+u_{1}=w+u_{2}\iff v-w=u_{2}-u_{1}$. Thus, $v-w\in U$. Now a is true, from above, b,c is also true.
> 
> $\blacksquare$

With the statement above, we finally can define addition and scalar multiplication on $V/U$

>[!example] Addition and scalar multiplication on $V/U$
>Suppose $U$ is a subspace of $V$ then the addition and scalar multiplication are defined on $V/U$ by 
> $$
>\begin{align}
>(v+U)+(w+U)&=(v+w)+U\\
> \lambda(v+U)&=\lambda v+U
>\end{align}
> $$
> where $v,w\in V$ and $\lambda \in \mathbf{F}$

The statement above guarantees that the definition above is well-defined. Suppose we have $v+U=\hat{v}+U$ and $w+U=\hat{w}+U$, we need to make sure that $(v+U)+(w+U)=(\hat{v}+U)+(\hat{w}+U)$. Easy to verify, it's guaranteed by the statement above. 

With the definition above, we now can say that: $V/U$ is a vector space.

>[!info] $V/U$ is a vector space
>By the definition of [[Math/Linear Algebra Done Right/Vector Space\|vector space]], it's easy to verify.
>What is needed to point out is that,
>zero vector: $0_{V/U}=U$
>Inverse: $-(v+U)=-v+U$

>[!info] Dimension of a quotient Space
>Suppose $V$ is finite-dimensional and $U$ is a subspace of $V$. Then 
> $$
>  \text{dim }V/U=\text{dim }V-\text{dim }U
> $$
> 
> Proof:
> 
> Let [[Math/Linear Algebra Done Right/π\|π]] be the quotient map from $V$ to $V/U$. Easy to verify, $\text{dim null }\pi=\text{dim }U$. Thus, by the [[Math/Linear Algebra Done Right/Fundamental Theorem of Linear Maps\|Fundamental Theorem of Linear Maps]] we get
>  $$
> \text{dim }V=\text{dim }U+\text{dim }V/U \iff \text{dim }V/U=\text{dim }V-\text{dim }U
> $$
> 
> $\blacksquare$

