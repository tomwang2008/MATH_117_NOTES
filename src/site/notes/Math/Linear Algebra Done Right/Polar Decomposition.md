---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/polar-decomposition/","dg-note-properties":{}}
---

# Polar Decomposition
> [!info]  Polar decomposition
> Suppose $T\in$[[Math/Linear Algebra Done Right/L(V)\|L(V)]]. Then there exists an [[Math/Linear Algebra Done Right/Isometry\|isometry]] $S\in \mathcal{L}(V)$ such that 
> $$
> T=S\sqrt{ T^*T }
> $$ 
> Proof:
> 
> If $v\in$[[Math/Linear Algebra Done Right/Vector Space\|$V$]], then
> $$
> \begin{align}
\lVert Tv \rVert ^2 & =\langle Tv,Tv \rangle \\
 & =\langle T^*Tv,v \rangle \\
 & =\langle (\sqrt{ T^*T })^2v,v \rangle \\
 & =\langle \sqrt{ T^ *T}v,\sqrt{ T^*T }v \rangle \\
 & =\lVert \sqrt{ T^*T }v \rVert^2 
\end{align}
> $$
> Thus we have $\lVert Tv \rVert=\lVert \sqrt{ T^*T }v \rVert$, we now can define a [[Math/Linear Algebra Done Right/Linear Map\|linear map]] $S_{1}\ :\ \text{range }\sqrt{ T^*T }\to \text{range }T$ such that $S_{1}(\sqrt{ T^*T }v)=Tv$. However $\sqrt{ T^*T }$ might not be [[Math/Linear Algebra Done Right/Injectivity\|injective]], thus, we need to check if $S_{1}$ is well-defined. Suppose we have $\sqrt{ T^*T }v_{1}=\sqrt{ T^*T }v_{2}$, we want $Tv_{1}=Tv_{2}$. 
> $$
> \begin{align}
\lVert Tv_{1}-Tv_{2} \rVert  & =\lVert T(v_{1}-v_{2}) \rVert  \\
 & = \lVert \sqrt{ T^*T }(v_{1}-v_{2}) \rVert  \\
 & = 0
\end{align} 
> $$
> Therefore, $S_{1}$ is indeed well-defined and also easy to see, $S_{1}$ is an isometry.
> 
> However, $S_{1}$ is not defined on $\mathcal{L}(V)$, therefore we need to expand it into an operator on $\mathcal{L}(V)$. Therefore, we have $S_{2}$.
> 
> From the [[Math/Linear Algebra Done Right/Fundamental Theorem of Linear Maps\|Fundamental Theorem of Linear Maps]], we have 
> $$
>  \text{dim range }(\sqrt{ T^*T })=\text{dim range }T
> $$
> Therefore, we have 
> $$
> \text{dim range }(\sqrt{ T^*T })^\perp=\text{dim range }T^\perp
> $$
> Because the two [[Math/Linear Algebra Done Right/Orthogonal Complement\|orthogonal comploeements]] have the same length, we could write out two [[Math/Linear Algebra Done Right/Orthonomal\|orthonormal]] basis $e_{1},\dots,e_{m}$ and $f_{1},\dots,f_{m}$ for $\text{range }(\sqrt{ T^*T })^\perp$ and $\text{range }T^\perp$. We define $S_{2}\ :\ \text{range }(\sqrt{ T^*T })^\perp\to \text{range }T^\perp$. Where $S_{2}(a_{1}e_{1}+\dots+a_{n}e_{n})=a_{1}f_{1}+\dots+a_{n}f_{n}$. Therefore, we have $\lVert S_{2}u \rVert=\lVert u \rVert$.
> 
> We now define $S$ on $\mathcal{L}(V)$ as $Sv=S_{1}u+S_{2}w$, where $v=u+w$ and $u\in \text{range }(\sqrt{ T^*T })$, $w\in \text{range }(\sqrt{ T^*T })^\perp$. $S$ is an isometry because
> $$
> \begin{align}
\lVert Sv \rVert ^2 & =\lVert S_{1}u+S_{2}v \rVert ^2 \\
 & =\lVert S_{1}u \rVert ^2+\lVert S_{2}w \rVert ^2 \\
 & =\lVert u \rVert ^2+\lVert w \rVert ^2 \\
 & =\lVert v \rVert
{ #2}

\end{align}
> $$
> Also for every $v\in V$, we have $Tv=S\sqrt{ T^*T }v=S_{1}(\sqrt{ T^*T })v$
> 
> $\blacksquare$

<span style="color:rgb(188, 145, 16)">Notice</span><span style="color:rgb(188, 145, 16)">:</span> The two orthonormal basises are not necessarily the same, so we may require two different bases on the same vector space

<span style="color:rgb(192, 0, 0)">Important:</span> Always pay attention that $S$ could be different, because $S_{2}$ can change when $S_{2}\neq 0$.


> [!info]  Uniqueness and invertibility
> Suppose $T\in \mathcal{L}(V)$, Then $T$ is [[Math/Linear Algebra Done Right/Invertible\|inveretible]] if and only if there exitsts a unique isometry $S\in \mathcal{L}(V)$ such that $T=S\sqrt{ T^*T }$.
> 
> Proof:
> 
>Suppose $S$ is unique, if $T$ is not invertible, we have $\sqrt{ T^*T }$ is not invertible, therefore, $\text{range }\sqrt{ T^*T }\neq V$. Thus, change the $S_{2}$ above, we get different $S$. This contradicts our assumption so $T$ is invertible.
>
>If $T$ is invertible, then $\sqrt{ T^*T }$ is invertible and all the [[Math/Linear Algebra Done Right/Singular Value\|singular values]] of $T$ is non-zero. If $S$ is not unique. Suppose $S_{1}$ and $S_{2}$ are two different isometries that satisfy the decompostition. For all $v\in V$, we have $Tv-Tv=S_{1}(\sqrt{ T^*T }v)-S_{2}(\sqrt{ T^*T }v)$. Which is $S_{1}(\sqrt{ T^*T }v)=S_{2}(\sqrt{ T^*T }v)$. Since $\sqrt{ T^*T }$ is invertible, it's also surjective. Therefore, we have $S_{1}u=S_{2}u$ for all $u\in V$. Contradiction occurs, so $S$ is unique.
>
>$\blacksquare$

