---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/adjoint/","dg-note-properties":{}}
---

# Adjoint
> [!example] Definition of adjoint
> Suppose $T\in$[[Math/Linear Algebra Done Right/L(V,W)\|L(V,W)]]. The adjoint of $T$ is the function $T*\ :\ W\to V$ such that 
> $$
> \langle Tv,w \rangle=\langle v,T^*w \rangle
> $$
> for every $v\in$[[Math/Linear Algebra Done Right/Vector Space\|$V$]] and every $w\in W$.

 The fact that adjoint always exists is guarenteed by the [[Math/Linear Algebra Done Right/Riesz Representation Theorem\|riesz representation theorem]]. 

> [!info]  The adjoint is a [[Math/Linear Algebra Done Right/Linear Map\|linear map]]
> If $T\in \mathcal{L}(V,W)$, then $T^*\in \mathcal{L}(W,V)$
> 
> Proof:
> 
> We prove the additive property first
>  $$
> \begin{align}
\langle v,T^*(w_{1}+w_{2}) \rangle & =\langle Tv, w_{1}+w_{2} \rangle\ \\
 & =\langle Tv,w_{1} \rangle+\langle Tv,w_{2} \rangle \\
 & =\langle v,T^*w_{1} \rangle+\langle v,T^*w_{2} \rangle \\
 & =\langle v,T^*w_{1}+T^*w_{2} \rangle
\end{align}
> $$
> Now we prove the homogeneous property 
> $$
> \begin{align}
\langle v,T^*\lambda w \rangle  & =\langle Tv,\lambda w \rangle\ \\
 &= \overline{\lambda}\langle Tv,w \rangle \\
 & =\overline{\lambda}\langle v,T^*w \rangle \\
 & =\langle v,\lambda T^*w \rangle
\end{align}
> $$
> $\blacksquare$

Despite of the basic properties of linear map, adjoint map has some other properties.

> [!info]  Properties of the adjoint
> (a) $(S+T)^*=S^*+T^*$ for all $S,T\in \mathcal{L}(V,W)$;
> 
> (b) $(\lambda T)^*=\overline{\lambda}T^*$ for all $\lambda \in \mathbf{F}$ and $T\in \mathcal{L}(V,W)$;
> 
> (c) $(T^*)^*=T$ for all $T\in \mathcal{L}(V,W)$;
> 
> (d) $I^*=I$, where $I$ is the identity operator on $V$;
> 
> (e) $(ST)^*=T^*S^*$ for all $T\in \mathcal{L}(V,W)$ and $S\in \mathcal{L}(W,U)$ (here $U$ is an [[Math/Linear Algebra Done Right/Inner Product Space\|inner product space]] over $\mathbf{F}$)
> 
> Proof:
> 
> (a)
> $$
> \begin{align}
\langle v,(S+T)^*w \rangle & =\langle (S+T)v,w \rangle \\
 & =\langle Sv,w \rangle+\langle Tv,w \rangle \\
 & =\langle v,S^*w \rangle+\langle v,T^*w \rangle \\
 & =\langle v,S^*w+T^*w \rangle
\end{align}
> $$
> (b)
> $$
> \begin{align}
 \langle v,(\lambda T)^*w \rangle & =\langle \lambda Tv,w \rangle \\
 & =\lambda \langle Tv,w \rangle \\
 & =\langle v,\overline{\lambda}T^*w \rangle
\end{align}
> $$
> (c)
> $$
> \langle v,(T^*)^*w \rangle=\langle T^*v,w \rangle=\overline{\langle w,T^*v \rangle}=\overline{\langle Tw,v \rangle}=\langle v,Tw \rangle
> $$
> (d)
> This should be trival
> 
> (e)
> $$
> \begin{align}
\langle v,(ST)^*w \rangle & =\langle STv,w \rangle \\
 & =\langle Tv,S^*w \rangle \\
 & =\langle v,T^*S^*w \rangle
\end{align}
> $$
> $\blacksquare$

> [!info]  [[Math/Linear Algebra Done Right/Null Spaces\|Nulll space]] and [[Math/Linear Algebra Done Right/Ranges\|range]] of $T^*$
> Suppose $T\in \mathcal{L}(V,W)$. Then
> (a) $\text{null }T^*=(\text{range }T)^\perp$
> 
> (b) $\text{range }T^*=(\text{null }T)^\perp$
> 
> (c) $\text{null }T=(\text{range }T^*)^\perp$
> 
> (d) $\text{range }T=(\text{null }T^*)^\perp$
> 
> Proof:
> 
> We start by proving (a) 
> $$
> \begin{align}
w\in \text{null }T^* & \iff T^*w=0 \\
 & \iff \langle v,T^*w  \rangle =0 \text{ for all }v\in V \\
 & \iff \langle Tv,w  \rangle=0 \\
 & \iff w \in(\text{range }T)^\perp
\end{align}
> $$
> Taking the [[Math/Linear Algebra Done Right/Orthogonal Complement\|orthogonal complement]] on both sides gives us (c) and replace $T$ with $T^*$ gives us (d). Finally, take the complement again gives us (b)
> 
> $\blacksquare$

Notice how adjoint is extremely similalr to [[Math/Linear Algebra Done Right/Dual Map\|dual map]].