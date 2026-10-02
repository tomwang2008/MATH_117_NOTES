---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/linear-map/","dg-note-properties":{}}
---

# Linear Map

Now we introduce one of the key definitions in linear algebra

>[!example] Linear Map
>A linear map from [[Math/Linear Algebra Done Right/Vector Space\|$V$]] to [[Math/Linear Algebra Done Right/Vector Space\|$W$]] is a function $T: V\to W$ with the following properties:
>additivity
>$$T(u+v)=Tu+Tv$$for all $u,v\in V$
>homogeneity
>$$T(\lambda v)=\lambda Tv$$for all $\lambda \in \mathbf F$ and $v\in V$


Our next result shows us that a linear map is completely determined by its values on a basis.

>[!info] Linear maps and basis of domain
>Suppose $v_1,\dots,v_n$ is a basis of $V$ and $w_1,\dots,w_n\in W$. Then there exists a unique linear map $T:V\to W$ such that
>$$Tv_j=w_j$$
>for every $j=1,\dots,n$
>
>Proof:
>We define $T(a_1v_1+\dots+a_nv_n)=a_1w_1+\dots+a_nw_n$ now we prove that this is the only linear map that satisfy the problem.
>The function $T$ is a linear map because $$\begin{align*} T(u + v) &= T( (a_1 + c_1)v_1 + \dots + (a_n + c_n)v_n ) \\ &= (a_1 + c_1)w_1 + \dots + (a_n + c_n)w_n \\ &= (a_1w_1 + \dots + a_nw_n) + (c_1w_1 + \dots + c_nw_n) \\ &= Tu + Tv. \end{align*}$$
>and also 
>$$\begin{align*}
>T(\lambda a_1v_1+\dots+\lambda a_nv_n)&=\lambda a_1w_1+\dots+\lambda a_nw_n\\
>&=\lambda(a_1w_1+\dots+a_nw_n)\\
>&=\lambda T(v)
>\end{align*}$$
>Thus, $T$ is a linear map.
>
>For every $v\in V$, $v$ could be uniquely written in the form of $a_1v_1+\dots+a_nv_n$. Thus, by the definition of linear map $Tv=a_1Tv_1+\dots+a_nTv_n$. Since $Tv_j=w_j$, every $T(v)$ is uniquely determined. Thus, once the basis is determined, the linear map will be fixed.
>
>$\blacksquare$

>[!info] Linear maps take 0 to 0
>Suppose $T$ is a linear map from $V$ to $W$. Then $T(0)=0$ 
>Proof:
>$$T(0)=T(0+0)=T(0)+T(0)$$
>Thus,
>$$T(0)=0$$



## Examples of linear map

Zero
$0\in \mathcal {L}(V,W)$ is defined by
$$0v=0$$
The 0 on the left side is a function from $V$ to $W$ whereas the 0 on the left side is the additive identity in $W$.

Identity
The identity map, denoted $I$, is a function on some vector space that takes each element to itself. To be specific, $I\in\mathcal{L}(V,V)$ is defined by
$$Iv=v$$

Differentiation
Define $D\in\mathcal{L}(\mathcal{P}(R),\mathcal{P}(R))$ by
$$Dp=p'$$
Easy to verify that $D$ is a linear map by the properties of differentiation.

Integration
Define $T\in\mathcal{L}(\mathcal{P}(R),R)$ by
$$Tp = \int_{0}^{1} p(x) \ dx$$
Easy to verify that $T$ is a linear map by the properties of integration.


