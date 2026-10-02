---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/norm/","dg-note-properties":{}}
---

# Norm
> [!example] Definition of norm
> For $v\in$[[Math/Linear Algebra Done Right/Vector Space\|$V$]], the norm of $v$, denoted $\lVert v \rVert$, is defined by
>  $$
> \lVert v \rVert  =\sqrt{ \langle v,v \rangle }
> $$
> Where $\langle v,v \rangle$ denotes the [[Math/Linear Algebra Done Right/Inner Product\|inner product]] of $v$.



> [!info]  Basic properties of the norm
> Suppose $v\in$[[Math/Linear Algebra Done Right/Vector Space\|$V$]] 
> 
> (a) $\lVert v \rVert=0$ if and only if $v=0$.
> 
> (b) $\lVert \lambda v \rVert=\lvert \lambda \rvert \lVert v \rVert$ for all $\lambda \in \mathbf{F}$.
> 
> Proof:
> 
> For (a), since $\langle v,v \rangle=0$ if and only if $v=0$, the desired result holds.
> 
> For (b), 
> $$
> \begin{align}
>\lVert \lambda v \rVert  & =\sqrt{ \langle \lambda v,\lambda v \rangle } \\
 & =\sqrt{ \lambda \langle v,\lambda v \rangle } \\
 & =\sqrt{ \lambda^2\langle  v,v \rangle } \\
 & =\lambda \sqrt{ \langle v,v \rangle } \\
 & =\lvert \lambda \rvert \lVert v \rVert 
\end{align}
> $$
> $\blacksquare$

> [!info]  Triangle Inequality 
> Suppose $u, v \in V$. Then 
> $$\|u + v\| \le \|u\| + \|v\|.$$
 > This inequality is an equality if and only if one of $u, v$ is a nonnegative multiple of the other.
 > 
 > Proof:
 > $$ \begin{aligned} \|u + v\|^2 &= \langle u + v, u + v \rangle \\ &= \langle u, u \rangle + \langle v, v \rangle + \langle u, v \rangle + \langle v, u \rangle \\ &= \langle u, u \rangle + \langle v, v \rangle + \langle u, v \rangle + \overline{\langle u, v \rangle} \\ &= \|u\|^2 + \|v\|^2 + 2\mathrm{Re}\langle u, v \rangle \\ &\le \|u\|^2 + \|v\|^2 + 2|\langle u, v \rangle| \quad \quad \\ &\le \|u\|^2 + \|v\|^2 + 2\|u\|\|v\| \quad \quad  \\ &= (\|u\| + \|v\|)^2, \end{aligned} $$
 > $\blacksquare$
 
 > [!info]  Parallelogram Equality 
> Suppose $u, v \in V$. Then 
> $$\|u + v\|^2 + \|u - v\|^2 = 2(\|u\|^2 + \|v\|^2).$$
> Proof:
> 
> We have $$ \begin{aligned} \|u + v\|^2 + \|u - v\|^2 &= \langle u + v, u + v \rangle + \langle u - v, u - v \rangle \\ &= \|u\|^2 + \|v\|^2 + \langle u, v \rangle + \langle v, u \rangle \\ &\quad + \|u\|^2 + \|v\|^2 - \langle u, v \rangle - \langle v, u \rangle \\ &= 2(\|u\|^2 + \|v\|^2), \end{aligned} $$
>  as desired. 
>  
>  $\blacksquare$


