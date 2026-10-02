---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/orthogonal-complement/","dg-note-properties":{}}
---

# Orthogonal Complement
> [!example] Definition of orthogonal complement
> If $U$ is a subset of [[Math/Linear Algebra Done Right/Vector Space\|$V$]], then the [[Math/Linear Algebra Done Right/Orthogonal\|orthogonal]] complement of $U$, denoted $U^{\perp}$, is the set of all vectors in $V$ that are orthogonal to every vector in $U$ :
> $$
> U^{\perp}=\{ v\in V\ :\ \langle v,u \rangle=0 \ \text{for every }u\in U \}.
> $$

Here are some basic properties of orthogonal complement

(a) If $U$ is a subset of $V$, then $U^{\perp}$ is a [[Math/Linear Algebra Done Right/Subspace\|subspace]] of $V$.

(b) $\{ 0 \}^{\perp}=V$.

(c) $V^{\perp}=\{ 0 \}^{\perp}$.

(d) If $U$ is a subset of $V$, then $U\cap U^{\perp}\subset \{ 0 \}$.

(e) If $U$ and $W$ are subsets of $V$ and $U\subset W$, then $W^{\perp}\subset U^\perp$.

The properties above should be trival therefore, there is no proof for them.

> [!info]  [[Math/Linear Algebra Done Right/Direct Sum\|Direct sum]] of a subspace and its orthogonal complement
> Suppose $U$ is a [[Math/Linear Algebra Done Right/Finite-dimensional Vector Space\|finite-dimensional]] subspace of $V$. Then
> $$
> V=U\oplus U^\perp
> $$
> Proof:
> 
> We first show that $V=U+U^\perp$.
> 
> By using [[Math/Linear Algebra Done Right/Riesz Representation Theorem\|Riesz Representation Theorem]], we can define a [[Math/Linear Algebra Done Right/Linear Functional\|Linear Functional]] on $V$ such that 
> $$
> \Phi=\langle x,v \rangle
> $$
> where $x\in V$.
> 
> Now we restrict $\Phi$ on $U$ to get $\varphi=\Phi\big|_{U}=\langle x,v\rangle$ where $x\in U$. Since $\varphi$ is a linear functional on $U$, there exist $u\in U$ such that $\varphi=\langle x,u \rangle$. 
> 
> Now we have $\langle x,v \rangle=\langle x,u \rangle$, which is $\langle x,v-u \rangle=0$. This means that $w=v-u$ is orthogonal to $u$. Therefore, $v=u+w$ for every $v\in V$.
> 
> Based on the properties above, easy to see $U+U^\perp$ is a direct sum.
> 
> $\blacksquare$

 From the result above, we can conclude that 

> [!info]  [[Math/Linear Algebra Done Right/Dimension\|Dimension]] of the orthogoanl complement
> Suppose $V$ is finite-dimensional and $U$ is a subspace of $V$. Then
> $$
> \text{dim }U^\perp=\text{dim }V-\text{dim }U
> $$
> Proof:
> 
> The result follow immediately from $\text{dim }(U_{1}+U_{2})=\text{dim }U_{1}+\text{dim }U_{2}$ if and only if $U_{1}+U_{2}$ is a direct sum.
> 
> $\blacksquare$


> [!info]  The orthogonal complement of the orthogonal complement
> Suppose $U$ is a finite-dimensional subspace of $V$. Then
$$U = (U^\perp)^\perp$$
Proof:
>
We first show that $U \subseteq (U^\perp)^\perp$ and $(U^\perp)^\perp \subseteq U$.
>
Let $u \in U$. By definition, for any $v \in U^\perp$, we have $\langle u, v \rangle = 0$. This means $u$ is orthogonal to every vector in $U^\perp$. Therefore, $u \in (U^\perp)^\perp$.
>
Now we show the reverse. Let $u_1 \in (U^\perp)^\perp$. By using the orthogonal decomposition theorem on the finite-dimensional subspace $U$, we can uniquely write
>
$$u_1 = u + v$$
>
where $u \in U$ and $v \in U^\perp$.
>
Since $u_1 \in (U^\perp)^\perp$ and $v \in U^\perp$, they are orthogonal to each other, yielding $\langle u_1, v \rangle = 0$. Now we have $\langle u + v, v \rangle = 0$. By the additivity of the [[Math/Linear Algebra Done Right/Inner Product\|inner product]], this becomes $\langle u, v \rangle + \langle v, v \rangle = 0$.
>
Since $u \in U$ and $v \in U^\perp$, we know $\langle u, v \rangle = 0$. This leaves $\langle v, v \rangle = 0$, which means $v = 0$.Therefore, $u_1 = u + 0 = u$ for every $u_1 \in (U^\perp)^\perp$, meaning $(U^\perp)^\perp \subseteq U$.
>
Based on the mutual inclusion above, easy to see $U = (U^\perp)^\perp$.
>
$\blacksquare$

