---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/orthogonal-projection/","dg-note-properties":{}}
---

# Orthogonal Projection
> [!example] Definition of orthogonal projection
> Suppose $U$ is a [[Math/Linear Algebra Done Right/Finite-dimensional Vector Space\|finite-diemsnioanl]] [[Math/Linear Algebra Done Right/Subspace\|subspace]] of $V$. The [[Math/Linear Algebra Done Right/Orthogonal\|orthogonal]] projection of [[Math/Linear Algebra Done Right/Vector Space\|$V$]]onto $U$ is the [[Math/Linear Algebra Done Right/Operator\|operator]] $P_{U}\in$[[Math/Linear Algebra Done Right/L(V)\|L(V)]] defined as follows: For $v\in V$, write $v=u+w$, where $u\in U$ and $w\in U^\perp$. Then $P_{U}v=u$.

 Orthogonal has many basic properties

(a) $P_{U}\in \mathcal{L}(V)$;

(b) $P_{U}u=u$ for every $u\in U$;

(c) $P_{U}w=0$ for every $w\in U^\perp$;

(d) $\text{range }P_{U}=U$;

(e) $\text{null }P_{U}=U^\perp$;

(f) $v-P_{U}v\in U^\perp$;

(g) $P_{U}^2=P_{U}$;

(h) $\lVert P_{Uv} \rVert\leq \lVert v \rVert$;

(i) for every [[Math/Linear Algebra Done Right/Orthonomal\|orthonormal]] basis $e_{1},\dots,e_{m}$ of $U$,
$$
P_{U}v=\langle v,e_{1} \rangle e_{1}+\dots+\langle v,e_{n} \rangle e_{n}.
$$

This should be trival as readers can verify.

> [!info]  Minimizing the distance to a subspace
> Suppose $U$ is a finite-dimensional subspace of $V$, $v\in V$, and $u\in U$. Then 
> $$
> \lVert v-P_{U}v \rVert \leq \lVert v-u \rVert 
> $$
> Futhermore, the inequality above is an equality if and only if $u=P_{U}v$.
> 
> Proof:
> 
> We have
> $$
> \begin{align}
\lVert v-u \rVert ^2&=\langle v-u.v-u \rangle \\
 & =\lVert v \rVert ^2-\langle v,u \rangle-\langle u,v \rangle+\lVert u \rVert ^2 \\
 & =\lVert v \rVert ^2-\langle v,P_{U}v+u_{1} \rangle-\langle P_{U}v+u_{1},v \rangle+\lVert P_{U}v+u_{1} \rVert  \\
 & =\lVert v \rVert ^2-\langle v,P_{U} \rangle-\langle P_{U}v,v \rangle-\langle v,u_{1} \rangle-\langle u_{1},v \rangle+\lVert P_{U}v+u_{1} \rVert \\
 & =\lVert v \rVert^2-\langle v,P_{U} \rangle-\langle P_{U}v,v \rangle-\langle u_{1},P_{U}v \rangle-\langle P_{U}v,u_{1} \rangle +\lVert P_{U}v+u_{1} \rVert \\
 & =\lVert v \rVert^2- \langle v,P_{U} \rangle-\langle P_{U}v,v \rangle+\lVert P_{U}v \rVert^2+\lVert u_{1} \rVert^2 \\
 & \geq \lVert v-P_{U}v \rVert^2 
\end{align}
> $$
> $\blacksquare$




 
 

 
 

