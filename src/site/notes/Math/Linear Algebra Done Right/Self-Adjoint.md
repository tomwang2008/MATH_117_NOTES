---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/self-adjoint/","dg-note-properties":{}}
---

# Self-Adjoint

> [!example] Definition of self-adjoint
> An [[Math/Linear Algebra Done Right/Operator\|operator]] $T\in$[[Math/Linear Algebra Done Right/L(V)\|L(V)]] is called self-adjoint if $T=T^*$. In other words, $T\in \mathcal{L}(V)$ is self-adjoint if and only if 
> $$
> \langle Tv,w \rangle=\langle v,Tw \rangle
> $$
> for all $v,w\in V$.

> [!info]  [[Math/Linear Algebra Done Right/Eigenvalue\|Eigenvalue]] of self-adjoint operators are real
> Every eigenvalues of a self-adjoint operator is real.
> 
> Proof:
> 
>  Suppose $v\in$ [[Math/Linear Algebra Done Right/Vector Space\|$V$]] and $v$ is an eigenvalue of $T$ such that $Tv=\lambda v$ where $\lambda \in \mathbf{F}$.
>  $$
> \lambda \lVert v \rVert =\langle Tv,v \rangle=\langle v,Tv \rangle=\langle v,\lambda v \rangle=\overline{\lambda}\langle v,v \rangle=\overline{\lambda}\lVert v \rVert 
> $$
> $\blacksquare$

> [!info]  Over $\mathbb{C}$, $Tv$ is [[Math/Linear Algebra Done Right/Orthogonal\|orthogonal]] to $v$ for all $v$ only for the $0$ operator.
> Suppose $V$ is a complex [[Math/Linear Algebra Done Right/Inner Product\|inner product]] space and $T\in \mathcal{L}(V)$. Suppose 
> $$
> \langle Tv,v \rangle=0
> $$
> for all $v\in V$. Then $T=0$
> 
> Proof:
> 
> Since $T$ is on a complex vector spaec, let $e_{1},\dots,e_{n}$ be the [[Math/Linear Algebra Done Right/Orthonomal\|orthonormal]] basis with respect to the [[Math/Linear Algebra Done Right/Upper-triangular Matrix\|upper-triangular matrix]] of $T$. Then we have 
> $$
> \langle Te_{j},e_{j} \rangle=0
> $$
> We want to prove that $\langle Te_{j},e_{i} \rangle=0$ for all $j,i=1,\dots,n$ 
>
> Before we start, it should be obivous that $\langle Te_{i},e_{j}=0 \rangle$ for every $j>i$. Thus, we only need to prove that $\langle Te_{i},e_{j} \rangle=0$ for all $i>j$. and we prove this by induction.
> 
> $i=1$ is trival, thus, we start at $i=2$. $\langle Te_{2},e_{1} \rangle=A_{2,1}$. From the problem, we get 
> $$
> \begin{align}
\langle T(e_{1}+e_{2}),e_{1}+e_{2} \rangle & =0 \\
 & =\langle Te_{2},e_{1} \rangle+\langle Te_{2},e_{2} \rangle+\langle Te_{1},e_{1}+e_{2} \rangle \\
 &= A_{2,1}
\end{align}
> $$
> Thus we have $A_{2,1}=0$.
> 
> Suppose $\langle Te_{k},e_{j} \rangle=0$ for all $k=1,\dots,m$, we prove that $\langle Te_{k},e_{j} \rangle=0$ for all $k=1,\dots,m+1$. 
> $$
> \begin{align}
\langle T(e_{k}+e_{j}),e_{k}+e_{j} \rangle & =\langle Te_{k},e_{k} \rangle+\langle Te_{k},e_{j} \rangle+\langle Te_{j},(e_{k}+e_{j}) \rangle \\
 & =0+\langle Te_{k},e_{j} \rangle+0 \\
 & =\langle Te_{k},e_{j} \rangle
\end{align}
> $$
> The second equation comes from our assumption. Thus, we've proved that $\langle Te_{j},e_{i} \rangle=0$ for all $j,i=1,\dots,n$. Therefore, for every $u,w\in V$, we have $\langle Tu,w \rangle=0\implies T=0$.
> 
> $\blacksquare$

<span style="color:rgb(188, 145, 16)">Notice</span><span style="color:rgb(188, 145, 16)">:</span> The proof above only works when $V$ is a [[Math/Linear Algebra Done Right/Finite-dimensional Vector Space\|finite-dimensional]] vector space. For [[Math/Linear Algebra Done Right/Infinite-dimensional Vector Space\|infinite-dimensional vector spaces]], we use the Polarization Identity

$$
\begin{align}
\langle Tu,w \rangle= & \frac{\langle T(u+w),u+w \rangle-\langle T(u-w),u-w \rangle}{4} \\
 & +\frac{\langle T(u+iw),u+iw \rangle-\langle T(u-iw),u-iw \rangle}{4}i
\end{align}
$$
Now we have $\langle Tu,w \rangle=0$ for all $u,w\in V$, and thus, $T=0$

> [!info]  Over $\mathbb{C}$, $\langle Tv,v \rangle$ is real for all $v$ only for self-adjoint operators.
> Suppose $V$ is a complex inner product space and $T\in \mathcal{L}(V)$. Then $T$ is self-adjoint if and only if 
> $$
> \langle Tv,v \rangle\in \mathbb{R}
> $$
> for every $v\in V$.
> 
> Proof:
> $$
> \langle Tv,v \rangle-\overline{\langle Tv,v \rangle}=\langle Tv,v \rangle=\langle T^*v,v \rangle=\langle (T-T^*)v,v \rangle=0
> $$
> From the conclusion above, we have $T-T^*=0$, which is $T=T^*$. 
> 
> The forward side should be trival, $\langle Tv,v \rangle=\langle v,Tv \rangle=\overline{\langle Tv,v \rangle}$ and we get the desired.
> 
> $\blacksquare$


> [!info]  If $T=$[[Math/Linear Algebra Done Right/Adjoint\|$T^*$]] and $\langle Tv,v \rangle=0$ for all $v$, then $T=0$
> Suppose $T$ is self-adjoint operator on $V$ such that 
> $$
> \langle Tv,v \rangle=0
> $$
> for all $v\in V$. Then $T=0$
> 
> Proof:
> 
> We use the polarization identity just like how we proved it before.
> 
> $\blacksquare$

