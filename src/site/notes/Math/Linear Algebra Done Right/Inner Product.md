---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/inner-product/","dg-note-properties":{}}
---

# Inner Product
>[!example] Definition of inner product
>An inner product on [[Math/Linear Algebra Done Right/Vector Space\|$V$]] is a function that takes each ordered pair $(u,v)$ of elements of $V$ to a number $\langle u,v\rangle\in \mathbf{F}$ and has the following properties:
>
>Positivity
>
> $\langle v,v \rangle\geq 0$  for all $v\in V$
> 
> Definiteness
> 
> $\langle v,v \rangle=0$ if and only if $v=0$
> 
> Additivity in first slot
> 
> $\langle u+v,w \rangle=\langle u,w \rangle+\langle v,w \rangle$ for all $u,v,w\in V$
> 
> Homogeneity in first slot
> 
> $\langle \lambda u,v \rangle=\lambda \langle u,v \rangle$ for all $\lambda \in \mathbf{F}$ and all $u,v\in V$
> 
> Conjugate symmetry
> 
> $\langle u,v \rangle=\overline{\langle v,u \rangle}$ for all $v,u\in V$

The defintion of inner product is shown above, but we still don't know the exact function of inner product. Some common definitions are shown below.

(a) The **Euclidean inner product** on [[Math/Linear Algebra Done Right/Dimensional Spaces\|Dimensional Spaces]] is defined by
$$
\langle (w_{1},\dots,w_{n}),(u_{1},\dots u_{n}) \rangle=w_{1}\overline{u_{1}}+\dots+w_{n}\overline{u_{n}}
$$

(b) If $c_{1},\dots c_{n}$ are positive numbers, then an inner product can be defined on $\mathbf{F}^n$ by
$$
\langle (w_{1},\dots w_{n}),(u_{1},\dots ,u_{n}) \rangle=c_{1}w_{1}\overline{u_{1}}+\dots+c_{n}w_{n}\overline{u_{n}}
$$

(c) An inner product can be defined on the vector space of continuous real-valued functions on the interval $[-1,1]$ by
$$
\langle f,g \rangle=\int_{-1}^1f(x)g(x)dx
$$
(d) An inner product can be defined on [[Math/Linear Algebra Done Right/P(F)\|$\mathcal{P}(\mathbf{R})$]] by
$$
\langle p,q \rangle=\int_{0}^{\infty}f(x)g(x)e^{-x}dx
$$


> [!info]  Properties of an inner product
> (a) For each fixed $u\in V$, the function that takes $v$ to $\langle u,v \rangle$ is a linear map from $V$ to $\mathbf{F}$.
> 
> (b) $\langle 0,u \rangle=0$ for every $u\in V$
> 
> (c) $\langle u,0 \rangle=0$ for every $u\in V$
> 
>(d) $\langle u,v+w \rangle=\langle u,v \rangle+\langle u,w \rangle$ for all $u,v,w\in V$
>
>(e) $\langle u,\lambda v \rangle=\overline{\lambda}\langle u,v \rangle$ for every $\lambda \in \mathbf{F}$ and for all $u,v\in V$.
>
>Proof:
>
> (a), (b), (c) should be trival and thus we skip the proof. 
> 
> For (d), 
> $$
> \begin{align} \\
> \langle u,v+w \rangle &= \overline{\langle v+w,u \rangle} \\
> & =\overline{\langle v,u  \rangle}+\overline{\langle w,u \rangle} \\ 
> & =\langle u,v  \rangle+\langle u,w \rangle \\
\end{align}
> $$
> For (e),
> $$
> \begin{align} \\
> \langle u,\lambda v  \rangle & =\overline{\langle \lambda v,u \rangle} \\
> & =\overline{\lambda}\cdot\overline{\langle v,u \rangle} \\
 & =\overline{\lambda}\langle v,u \rangle
\end{align}
> $$
> 
> $\blacksquare$

