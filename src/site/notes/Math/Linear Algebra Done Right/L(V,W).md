---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/l-v-w/","dg-note-properties":{"mathLink":"$\\mathcal{L}(V,W)$"}}
---

# $\mathcal L (V,W)$ 



>[!example] $\mathcal L (V,W)$
>The set of all [[Math/Linear Algebra Done Right/Linear Map\|linear map]] is denoted $\mathcal L (V,W)$

Now we define the operations on $\mathcal{L}(V,W)$.

>[!example] Addition and scalar multiplication on $\mathcal{L}(V,W)$
>Suppose $T,S\in\mathcal{L}(V,W)$ and $\lambda \in\mathbf F$. The sum and product $\lambda T$ are linear maps from $V$ to $W$ defined by
>$$(S+T)(v)=Sv+Tv \ \ \  \text{and}\ \ \ (\lambda T)(v)=\lambda(Tv)$$
>for all $v\in V$
>

With the operation defined above, we can conclude that:
>[!info] $\mathcal{L}(V,W)$ is a [[Math/Linear Algebra Done Right/Vector Space\|vector space]] 
>With the operations of addition and scalar multiplication as defined above, $\mathcal{L}(V,W)$ is a vector space
>
>Proof:
>
>Commutativity
>$$Tv+Sv=Sv+Tv$$
>This property is true because $Tv,Sv$ is a vector in vector space $W$
>
>Associativity
>$$
>(T+(S+R))(v)=Tv+(S+R)(v)=(T+S)(v)+Rv=((T+S)+R)(v)$$
>
>$$a(bT)v=a[(bT)(v)]=a[b(Tv)]=ab(Tv)=(abT)v$$
>
>Additive Identity
>See examples in [[Math/Linear Algebra Done Right/Linear Map\|linear map]], there we define the additive identity
>
>Additive Inverse
>For every $T\in\mathcal{L}(V,W)$ let $(-T)$ be the additive inverse of $T$.
>$$Tv+(-T)v=Tv+(-1)Tv=0$$
>Thus, $(-T)$ is the additive inverse of $T$.
>
>Multiplicative Identity
>$$(1T)v=1(Tv)=Tv$$
>
>Distributive Properties
>$$((a+b)T)v=(a+b)(Tv)=aTv+bTv=a(Tv)+b(Tv)$$
>
>$$a(T+S)v=a[(T+S)v]=a[Tv+Sv]=aTv+aSv$$
>
>$\blacksquare$

Since $\mathcal{L}(V,W)$ is a vector space, then we should also know the dimension of this vector space.

>[!info] $\dim\mathcal{L}(V,W)=(\dim V)(\dim W)$
>Suppose $V$ and $W$ are finite-dimensional, then 
> $$
> \dim\mathcal{L}(V,W)=(\dim V)(\dim W)
> $$
> 
> Proof:
> 
> This result can be directly inferred by the [[Math/Linear Algebra Done Right/Matrix Representation\|matrix representation]].
> 
> $\blacksquare$
