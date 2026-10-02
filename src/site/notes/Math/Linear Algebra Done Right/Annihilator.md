---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/annihilator/","dg-note-properties":{}}
---

# Annihilator

>[!example] Definition $U^0$
>For $U \subset \text{ }$[[Math/Linear Algebra Done Right/Vector Space\|$V$]], we define $U^0$ as the annihilator of $U$:
> $$
> U^0=\{ \varphi \in V': \varphi (u)=0, u\in U \}
> $$ 

As we desired, $U^0$ is a [[Math/Linear Algebra Done Right/Subspace\|subspace]] of [[Math/Linear Algebra Done Right/Dual Space\|$V'$]].

>[!info] The annihilator is a subspace
>Suppose $U \subset V$, then $U^0$ is a subspace of $V'$.
>
>Proof:
>
>Let's verify if the three conditions of becoming a subspace is true or not in $U^0$.
>
>1.$0\in U^0$: For $0\in V'$, $0(u)=0,u\in U$. Thus, $0\in U^0$.
>
>2.$\varphi+\phi \in U^0$: For $\varphi,\phi \in U^0$, $\varphi(u)+\phi(u)=(\varphi+\phi)(u)=0$. Thus, $\varphi+\phi \in U^0$
>
>3.$\lambda \varphi \in U^0$: For $\varphi \in U^0$, $\lambda \varphi(u)=\varphi(\lambda u)=0$
>
>$\blacksquare$

>[!info] The [[Math/Linear Algebra Done Right/Dimension\|dimension]] of annihilator
>Suppose $U\subset V$ then,
> $$
> \text{dim }U+\text{dim }U^0=\text{dim }V
> $$
> Proof:
> 
> Let $I:U\to V$ be a [[Math/Linear Algebra Done Right/Linear Map\|linear map]] such that $I(u)=u$. We consider the [[Math/Linear Algebra Done Right/Dual Map\|dual map]] of $I$, $I'$. Then we have
>  $$
> \text{dim null }I'+\text{dim range }I'=\text{dim }V'
> $$
> Notice that $\text{null }I'$ is exactly $U^0$, because for every $\varphi \in \text{null }I'$, $\varphi \in V'$ and $\varphi(u)=0$. So $\text{null }I'\subseteq U^0$. Also, for every $\varphi \in U^0$ and $u\in U$, $I'(\varphi)(u)=\varphi \circ I(u)=\varphi(u)=0$. Thus, $\varphi \in \text{null }I'$, therefore, $U^0\subseteq \text{null }I'$. Now we get:
> $$
> \text{dim }U^0+\text{dim range }I'=\text{dim }V'
> $$
> For every $\varphi \in V'$, $\varphi \circ I\in U'$. Also for every $\phi \in U'$, we have $\varphi \circ I=\phi,\text{ }\varphi \in V'$. This can be proved by basis extension. So we now have
> $$
> \text{dim }U^0 +\text{dim }U'=\text{dim }V'
> $$
> Substitute $\text{dim }U'$ to $\text{dim }U$ and $\text{dim V'}$ to $\text{dim }V$. We get
> $$
> \text{dim }U^0 + \text{dim }U=\text{dim }V
> $$
> 
> $\blacksquare$

>[!info] Characterization of a Subspace via Annihilator
>Suppose $V$ is [[Math/Linear Algebra Done Right/Finite-dimensional Vector Space\|finite-dimensional]] and $U$ is a subspace of $V$. Show that 
> $$
>  U=\{ v\in V\ :\ \varphi(v)=0\ \text{for every}\ \varphi \in U^0 \}
> $$
> Proof:
> 
> Let $S$ be the vector space on the right, it's easy to see that $U\subseteq S$, we now want to prove $S\subseteq U$.
> 
> Suppose $v\in S$ where $v \not\in U$. We can find a vector space $W$ such that $U\oplus W=V$. Then vector $v$ can be rewritten as $v=v_{1}+v_{2}$. Where $v_{1}\in U$ and $v_{2}\in W$.
> 
> For every $\psi \in W^0$, we have $\psi(v_{2})=0$, however, since $v\in S$, we have $\varphi(v)=\varphi(v_{1})+\varphi(v_{2})=\varphi(v_{2})=0$, for every $\varphi \in U^0$. Therefore, we have $\psi(v_{2})=0$ and $\varphi(v_{2})=0$, for every $\psi \in W^0$ and $\varphi \in U^0$. We can conclude that $v_{2}=0$. Thus, $v=v_{1}$ so $v\in U$ which contradicts our assumption. 
> 
> $\blacksquare$

>[!info] Characterization of an annihilator via subspace
>Suppose $V$ is finite-dimensional and $\Gamma$ is a subspace of $V'$. Show that 
> $$
> \Gamma=\{ v\in V\:\ \varphi(v)=0\ \text{for every}\ \varphi \in \Gamma \}^0
> $$
> Proof:
> 
> Let $\{ v\in V\:\ \varphi(v)=0\ \text{for every}\ \varphi \in \Gamma \}$ be $U$. From the conclusion above we have the desired.
> 
> $\blacksquare$




