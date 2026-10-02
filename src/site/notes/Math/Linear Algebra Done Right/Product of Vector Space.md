---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/product-of-vector-space/","dg-note-properties":{}}
---

# Product of Vector Space

>[!example] product of [[Math/Linear Algebra Done Right/Vector Space\|vector spaces]]
>Suppose $V_{1},\dots,V_{n}$ are vector space over $\mathbf{F}$. Then,
>The product $V_{1}\times\dots \times V_{n}$ is defined by 
> $$
> V_{1}\times\dots \times V_{n}=\{ (v_{1},\dots,v_{n})\ :\ v_{1}\in V_{1},\dots,v_{n}\in V_{n} \}.
> $$
> Addition on $V_{1}\times\dots \times V_{n}$ is defined by
> $$
> (u_{1},\dots,u_{n})+(v_{1},\dots,v_{n})=(u_{1}+v_{1},\dots,u_{n}+v_{n})
> $$
> Scalar multiplication is defined by
> $$
> \lambda(v_{1},\dots,v_{n})=(\lambda v_{1},\dots,\lambda v_{n})
> $$


By the definition above we can see that:

>[!info] The product of vector space is a vector space
>Suppose $V_{1},\dots,V_{n}$ are vector spaces over $\mathbf{F}$. Then $V_{1}\times\dots \times V_{n}$ is a vector space over $\mathbf{F}$.
>
>Proof:
>
>This is so obvious, a person who knows vector space should be able to prove this.

Now we show the dimension of this new vector space.
>[!info] Dimension of a product is the sum of dimensions.
>Suppose $V_{1},\dots,V_{n}$ are [[Math/Linear Algebra Done Right/Finite-dimensional Vector Space\|finite-dimensional]] vector spaces. Then $V_{1}\times\dots \times V_{n}$ is finite-dimensional and 
> $$
> \dim(V_{1}\times\dots \times V_{n})=\dim V_{1}+\dots+\dim V_{n}
> $$
> Proof:
> 
> For every $v_{k}\in V_{k}$ where $k=1,\dots,n$. There are $\dim V_{k}$ basis vectors. Therefore, by putting the basis vectors in the $k^{th}$ entry and putting 0 in the other entry, we have created a basis vector of $V_{1}\times\dots \times V_{n}$. Thus, the dimension of $V_{1}\times\dots \times V_{n}$ should be $\dim V_{1}+\dots+\dim V_{n}$
> 
> $\blacksquare$







