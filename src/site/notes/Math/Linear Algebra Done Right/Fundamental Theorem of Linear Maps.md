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
>Now If $w_1,\dots,w_n$ is linearly independent, then $\dim \text{range}\ T =n$ since the the list $(w_{1},\dots,w_{n})$ is linearly independent, we have $\text{dim null }T=0$
>$$\dim V=\dim\text{range}\ T+\dim\text{null } T$$
>
>If $w_1,\dots,w_n$ is linearly dependent, we could pick out some vectors in $w_1,\dots,w_n$ and remain the span of the original space. Let $w_1,\dots,w_r$ be the vectors we picked and $w_{r+1},\dots,w_n$ be the remaining vectors. The vectors we picked are linearly independent, so $\dim\text{range}\ T=r$ 
>
>Remark that $T(v_{i})=a_{i,1}w_{1}+\dots+a_{i,r}w_{r}$,where $i=1+r,\dots,n$. We have $v_{i}-\sum a_{i,j}v_{j}$ is a vector in the null space of $T$. Now we prove that the list $\left( v_{r+1}-\sum a_{r+1,j}v_{j},\dots,v_{n}-\sum a_{n,j}v_{j} \right)$ is linearly independent. This should be trivial since the the linear comnbination is formed by linearly independent vectors. Therefore,
>
 $$\dim V=\dim\text{range}\ T+\dim\text{null } T$$
 $\blacksquare$
 
 
 

 



