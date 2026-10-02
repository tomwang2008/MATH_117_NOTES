---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/fundamental-theorem-of-linear-maps/","dg-note-properties":{}}
---

# Fundamental Theorem of Linear Maps

The theorem is also known as the Rank-nullity Theorem.

>[!info] Fundamental Theorem of [[Math/Linear Algebra Done Right/Linear Map\|Linear Maps]] 
>Suppose [[Math/Linear Algebra Done Right/Vector Space\|$V$]] is [[Math/Linear Algebra Done Right/Finite-dimensional Vector Space\|finite-dimensional]] and [[Math/Linear Algebra Done Right/Linear Map\|$T$]] $\in$ [[Math/Linear Algebra Done Right/L(V,W)\|L(V,W)]], then we have 
>$$\text{dim }V=\text{dim range }T+\text{dim null }T$$
>
>Proof:
>
>For any $T\in\mathcal{L}(V,W)$, let $v_1,\dots,v_n$ be a basis of $V$ and let $Tv_1,\dots,Tv_n=w_1,\dots,w_n$.
>
>Now If $w_1,\dots,w_n$ is linearly independent, then $\dim \text{range}\ T =n$ and $\dim\text{null}\ T=0$ since the only way that $Tv=0$ is $v=0$ therefore we have $$\dim V=\dim\text{range}\ T+\dim\text{null} T$$
>
>If $w_1,\dots,w_n$ is linearly dependent, we could pick out some vectors in $w_1,\dots,w_n$ and remain the span of the origin list. Let $w_1,\dots,w_r$ be the vectors we picked out and $w_{r+1},\dots,w_n$ be the remaining vectors. The remaining vectors are linearly independent, so $\dim\text{range}\ T=n-r$ 
>
>For $w_1,\dots,w_r$, since $Tv_j=w_j$ where $j=1,\dots,r$ every linear combination of $v_1,\dots,v_r$ corresponds to a situation when the linear combination of $w_1,\dots,w_n$ equals 0. Also for every $a_1w_1+\dots+a_nw_n=0$ we could always rewrite it into $a_1w_1+\dots+a_jw_j=-(a_{j+1}w_{j+1}+\dots+a_nw_n)$. Thus, for every situation when the linear combination of $w_1,\dots,w_n$ equals 0, it corresponds to a linear combination of $v_1,\dots,v_r$. Thus, the dimension of $\text{null} \ T$ equals $r$. 
 Therefore, 
 $$\dim V=\dim\text{range}\ T+\dim\text{null} T$$
 $\blacksquare$
 
 
 
 
 



