---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/direct-sum/","dg-note-properties":{}}
---

# Direct Sum

See [[Math/Linear Algebra Done Right/Sum of Subspace\|Sum of Subspace]] to understand how to find the sum of subspaces.

Direct sum is a special case of sum of subspaces

>[!example] Definition of Direct Sum
>The sum of $U_1\dots U_n$ is called a direct sum if and only if all the elements in $U_1+\dots +U_n$ can be uniquely written in a sum $u_1+\dots +u_n$ where $u_j\in U_j\ ,\ j=1,\dots ,n$
>
>We denote $U_1 \bigoplus\dots \bigoplus U_n$ if $U_1+\dots+U_n$ is a direct sum


Direct sum has many good properties since there is no redundancy in the subspace. Here we introduce one way to identify a direct sum

> [!info] The sum $U_1+\dots+U_n$ is a direct sum if and only if 0 can be uniquely expressed as $0+\dots+0$.
> Proof:
> 
> If $U_1+\dots+U_n$ is a direct sum, then by definition, the only way to express 0 is $0+\dots+0$.
> 
> If the only way to express 0 in $U_1+\dots+U_n$ is $0+\dots+0$, then we can infer that $u_1+\dots+u_n\not = 0$ when $\exists u_j \not = 0$. This means that there are no situations when $u_1+\dots+u_n = v_1+\dots+v_n$ where $\exists u_j\not = v_j$. Thus $U_1+\dots+U_n$ is a direct sum
> 
> $\blacksquare$


From the statement above we could infer that:

> [!info] $U+V$ is a direct sum if and only if $U\cap V=\set{0}$
> 
> Proof:
> 
> If $U+V$ is a direct sum then $U \cap V=\set{0}$. If not, let $U\cap V= S$ where $S\not = \set{0}$. We pick $u, -u\in S$ where $\ u,\ -u\not =0$, $u+(-1)u=0$. This counters the statement above  
> 
> If $U\cap V=\set{0}$. If there exists $u\in U, v\in V$ where $u,v\not =0$, such that $u+v=0$, then $v=-u$. Since every element in the subspace has a additive inverse, this will cause that $v\in U$. However, $v\in U$ will lead to $U\cap V\not = \set{0}$. Thus $U+V$ is a direct sum
> 
> $\blacksquare$

Now here is another way:

>[!info] Suppose $U_{1},\dots,U_{n}$ are subspaces from $V$. Then $U_{1}+\dots+U_{n}$ is a direct sum if and only if
> $$
> \text{dim }(U_{1}+\dots+U_{n})=\text{dim }U_{1}+\dots+\text{dim }U_{n}
> $$
> 
> Proof:
> 
> If the sum is direct, then from [[Math/Linear Algebra Done Right/Γ\|note $\Gamma$]] we know that the linear map $\Gamma$ is injective, easy to verify that $\Gamma$ is [[Math/Linear Algebra Done Right/Surjectivity\|surjective]], thus, $\Gamma$ is invertible. So $U_{1}+\dots+U_{n}$ is [[Math/Linear Algebra Done Right/Isomorphism\|isomorphic]] to [[Math/Linear Algebra Done Right/Product of Vector Space\|$U_1 \times \dots \times U_n$]]. Therefore, 
>  $$
> \text{dim }(U_{1}+\dots+U_{n})=\text{dim }(U_{1}\times\dots \times U_{n})=\text{dim }U_{1}+\dots+\text{dim }U_{n}
> $$
> If $U_{1}+\dots+U_{n}$ has the same dimension of $U_{1}\times\dots \times U_{n}$. Then by the [[Math/Linear Algebra Done Right/Fundamental Theorem of Linear Maps\|Fundamental Theorem of Linear Maps]], 
>$$
>\begin{align}
>& \text{dim }(U_{1}\times\dots \times U_{n})=\text{dim null }\Gamma+\text{dim Range }\Gamma\\
>\iff &\text{dim }(U_{1}\times\dots \times U_{n})=\text{dim null }\Gamma+\text{dim }(U_{1}+\dots+U_{n})\\
>\iff &0=\text{dim null }\Gamma
>\end{align}
> $$
> Thus, the linear map $\Gamma$ is injective, therefore, invertible. $U_{1}+\dots+U_{n}$ is direct.(see the note [[Math/Linear Algebra Done Right/Γ\|Γ]]) 
> 
> $\blacksquare$


