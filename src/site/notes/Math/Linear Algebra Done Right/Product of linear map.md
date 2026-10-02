---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/product-of-linear-map/","dg-note-properties":{}}
---

# Product of linear map

Usually products of two elements in a vector space don't make sense, however, for some pairs of linear map a useful product exists.

>[!example] Product of Linear Map
>If $T\in\mathcal{L}(U,V)$ and $S\in\mathcal{L}(V,W)$, then the product $ST\in\mathcal{L}(U,W)$ is defined by
>$$(ST)u=S(Tu)$$
>for every $u\in U$

Note that $ST$ is only defined when $T$ is mapped into the domain of $S$.

Now we introduce some algebraic properties of products of linear map

>[!info] Algebraic Properties of Products of Linear Map 
> 1.
>$$(T_1T_2)T_3=T_1(T_2T_3)$$
> 2.
>$$TI=IT=T$$
> 3.
>$$(S_1+S_2)T=S_1T+S_2T$$
>and
>$$S(T_1+T_2)=ST_1+ST_2$$
>
>
> Proof:
> The proof below is based on the truth that [[Math/Linear Algebra Done Right/L(V,W)\|L(V,W)]] and [[Math/Linear Algebra Done Right/L(V,W)\|$\mathcal{L}(U,V)$]] is a vector space
> For the first one,
>$$(T_1T_2)T_3v=(T_1T_2)(T_3v)=T_1(T_2(T_3v))=T_1((T_2T_3)v)=T_1(T_2T_3)v$$
> For the second one,
> $$TI(v)=Tv=I(Tv)=ITv$$
> For the third one,
> $$(S_1+S_2)Tv=(S_1+S_2)(Tv)=S_1(Tv)+S_2(Tv)=S_1Tv+S_2Tv$$
> and
> $$S(T_1+T_2)v=S(T_1v+T_2v)=S(T_1v)+S(T_2v)=ST_1v+ST_2v$$
> 
> $\blacksquare$






