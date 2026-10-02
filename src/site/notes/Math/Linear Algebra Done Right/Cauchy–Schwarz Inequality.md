---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/cauchy-schwarz-inequality/","dg-note-properties":{}}
---

# Cauchy–Schwarz Inequality
> [!info] Cauchy–Schwarz Inequality
> Suppose $u,v\in$[[Math/Linear Algebra Done Right/Vector Space\|$V$]]. Then 
> $$
> \lvert \langle u,v \rangle \rvert \leq \lVert u \rVert \cdot \lVert  v \rVert 
> $$
> This inequality is an equality if and only if one of $u,v$ is a scalar multiple of the other.
> 
> Proof:
> 
> Consider the [[Math/Linear Algebra Done Right/Orthogonal\|orthogonal]] decomposition of $u,v$. We get
> $$
> 
u  =\frac{\langle u,v \rangle}{\lVert v \rVert ^2}v+w
> $$
> Since $v,w$ are orthogonal, by applying the [[Math/Linear Algebra Done Right/Orthogonal\|pythagorean theorem]], we get
> $$
>\begin{align}
 \lVert u \rVert ^2 & =\left\lVert  \frac{\langle u,v \rangle}{\lVert v \rVert ^2}  \right\rVert ^2+\lVert w \rVert ^2  \\
 & =\frac{\lvert \langle u,v \rangle \rvert ^2}{\lVert v \rVert ^2}+\lVert w \rVert ^2 \\
 & \geq \left\lVert  \frac{\langle u,v \rangle}{\lVert v \rVert }  \right\rVert
{ #2}

\end{align}
> $$
> Take the square root on both sides and we get the desired result
> 
> $\blacksquare$



