---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/polynomials-applied-on-operators/","dg-note-properties":{}}
---

# Polynomials applies on operators

>[!example] Definition of $T^m$
>Suppose [[Math/Linear Algebra Done Right/Operator\|$T$]]$\in$[[Math/Linear Algebra Done Right/L(V)\|L(V)]], and $m$ is a positive integer.
>$T^m$ is defined by 
> $$
> T^m= \underbrace{T\cdot \cdot \cdot T}_{\text{m times}}
> $$

For special cases:
$T^0$ is defined to be the identity map $I$ on $V$.
If $T$ is [[Math/Linear Algebra Done Right/Invertible\|invertible]], then $T^{-m}$ is defined by $(T^{-1})^m$.

>[!example] Definition of $\mathcal{P}(T)$
>Suppose $T\in \mathcal{L}(V)$ and $p \in$[[Math/Linear Algebra Done Right/P(F)\|P(F)]] is a polynomial given by 
> $$
> p(z)=a_{0}+a_{1}z+a_{2}z^2+\dots+a_{m}z^m
> $$
> Then the definition of $\mathcal{P}(T)$ is given by 
> $$
> p(T)=a_{0}I+a_{1}T+a_{2}T^2+\dots+a_{m}T^m
> $$

>[!info] Multiplicative Properties
>Suppose $p,q\in \mathcal{P}(\mathbf{F})$ and $T\in \mathcal{L}(V)$.
>Then
>
>(a) $(pq)(T)=p(T)q(T)$
>
>(b) $p(T)q(T)=q(T)p(T)$

The conclusion above requires a proof, I'm too lazy to write it out.


>[!info] Polynomial applied on any operator cannot span the whole vector space
>Suppose $V$ is [[Math/Linear Algebra Done Right/Finite-dimensional Vector Space\|finite-dimensional]] with $\text{dim }V>1$ and $T\in \mathcal{L}(V)$. Prove that 
> $$
> \{ p(T) \:\ p \in \mathcal{P}(\mathbf{F})\} \neq \mathcal{L}(V)
> $$
> Proof:
> 
> For any $q,p \in \{ p(T) \:\ p \in \mathcal{P}(\mathbf{F})\}$, they hold the property that $q(T)p(T)=(qp)(T)=(pq)(T)=p(T)q(T)$. This indicates that every linear map in $\mathcal{L}(V)$, they satisfy that $TS=ST$, which is impossible.
> 
> $\blacksquare$

