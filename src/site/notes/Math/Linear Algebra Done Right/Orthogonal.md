---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/orthogonal/","dg-note-properties":{}}
---

# Orthogonal
> [!example] Definition of orthogonal
> Two vectors $u,v\in$[[Math/Linear Algebra Done Right/Vector Space\|$V$]] are called orthogonal if and only if [[Math/Linear Algebra Done Right/Inner Product\|$\langle u,v \rangle$]] $=0$
>

Orthogonal is somehow important in the study of linear algebra, think of it as a ultra-plus version of [[Math/Linear Algebra Done Right/Linear Independence\|linearly independnet]].

> [!info]  Orthogonality and $0$
> (a) $0$ is orthogonal to every vector in $V$.
> 
> (b) $0$ is the only vector that is orthogonal to itself.
> 
> Proof:
> 
> For (a), since $\langle 0,u \rangle=\langle u,0 \rangle=0$, we get the desired.
> 
> For (b), since $\langle v,v \rangle=0$ if and only if $v=0$, we get the desired.
> 
> $\blacksquare$

> [!info] Pythagorean Theorem
> Suppose $u,v\in V$ are orthogonal. Then
> $$
> \lVert u+v \rVert ^2=\lVert u \rVert ^2+\lVert v \rVert
{ #2}

> $$
> Proof:
> $$
> \begin{align}
\lVert u+v \rVert ^2 & =\langle u+v,u+v \rangle \\
 & =\langle u,u \rangle+\langle v,v \rangle+\langle u,v \rangle+\langle v,u \rangle \\
 & =\lVert u,u \rVert ^2+\lVert v,v \rVert ^2 \\
\end{align}
> $$
> $\blacksquare$

Why orthogonal is important is beacuase that every pair of vector $(u,v)$ where $u,v\in V$ can be rewrite into a pair of orthogonal vector 

Suppose $u,v\in V$ with $v\neq0$. Set $c=\frac{\langle u,v \rangle}{\lVert v \rVert^2}$ and $w=u-\frac{\langle u,v \rangle}{\lVert v \rVert^2}v$. Then 

$$
\langle w,v \rangle=0\text{ and }u=cv+w
$$

Even better, we can rewrite every [[Math/Linear Algebra Done Right/Linear Independence\|linearly independnet]] list into an orthogonal list.

> [!info]  Gram-Schimidt Procedure
> Suppose $v_{1},\dots ,v_{m}$ is a linearly independent list of vectors in $V$. Let $e_{1}=v_{1}/\lVert v_{1} \rVert$. For $j=2,\dots,m$ define $e_{j}$ inductively by 
>  $$
> e_{j}=\frac{v_{j}-\langle v_{j},e_{1} \rangle e_{1}-\dots-\langle v_{j-1},e_{j-1} \rangle e_{j-1}}{\lVert v_{j}-\langle v_{j},e_{1} \rangle e_{1}-\dots-\langle v_{j-1},e_{j-1} \rangle e_{j-1} \rVert }
> $$
> Then $e_{1},\dots,e_{m}$ is an [[Math/Linear Algebra Done Right/Orthonomal\|orthonoamal]] list of vectors in $V$ such that 
> $$
> \text{span }(v_{1},\dots,v_{j})=\text{span }(e_{1},\dots,e_{j})
> $$
> for $j=1,\dots,m$.
> 
> Proof:
> 
> We verify that $e_{j}$ are orthogonal first. For every $e_{i},e_{j}$ where $j>i$. 
> $$\begin{align}
\langle e_{j},e_{i} \rangle & =\left\langle  \frac{v_{j}-\langle v_{j},e_{1} \rangle e_{1}-\dots-\langle v_{j-1},e_{j-1} \rangle e_{j-1}}{\lVert v_{j}-\langle v_{j},e_{1} \rangle e_{1}-\dots-\langle v_{j-1},e_{j-1} \rangle e_{j-1} \rVert },e_{i}  \right\rangle \\
 & =\frac{\langle v_{j},e_{j} \rangle -\langle  v_{j},e_{j}\rangle}{\lVert v_{j}-\langle v_{j},e_{1} \rangle e_{1}-\dots-\langle v_{j-1},e_{j-1} \rangle e_{j-1} \rVert }=0
\end{align}$$
>Therefore, the list $e_{1},\dots,e_{n}$ is orthogonal.
>
>From the definition above, $v_{i}\in \text{span }(e_{1},\dots,e_{j})$ where $i=1,\dots,j$ and both $v_{1},\dots,v_{j}$ and $e_{1},\dots,e_{j}$ are linearly independent, since $\text{span }(v_{1},\dots,v_{j})\subset \text{span }(e_{1},\dots,e_{j})$ and they have the same [[Math/Linear Algebra Done Right/Dimension\|dimension]]. So we get the desired.
>
>$\blacksquare$


