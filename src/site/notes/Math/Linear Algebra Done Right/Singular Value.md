---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/singular-value/","dg-note-properties":{}}
---

# Singular Value
> [!example] Definition of singular values
> Suppose $T\in$[[Math/Linear Algebra Done Right/L(V)\|L(V)]]. The singular values of $T$ are the [[Math/Linear Algebra Done Right/Eigenvalue\|eigenvalues]] of $\sqrt{ T^*T }$, with each eigenvalue $\lambda$ repeated $\text{dim }E(\lambda,\sqrt{ T^*T })$ times.

 See [[Math/Linear Algebra Done Right/Square Root\|the note sqaure root]] and [[Math/Linear Algebra Done Right/Eigenspace\|eigenspace]] if you forgot what they are.
 
 Notice that the singular values of [[Math/Linear Algebra Done Right/Operator\|$T$]] are all nonnegative, because they are the eigencalues of the [[Math/Linear Algebra Done Right/Positive\|positive]] operator $\sqrt{ T^*T }$.

> [!info]  Singular Value Decomposition
> Suppose $T\in \mathcal{L}(V)$ has singular values $s_{1},\dots,s_{n}$. Then there exist orthonormal bases $e_{1},\dots,e_{n}$ and $f_{1},\dots,f_{n}$ such that 
> $$
> Tv=s_{1}\langle v,e_{1} \rangle f_{1}+\dots+s_{n}\langle v,e_{n} \rangle f_{n}
> $$
> for every $v\in$[[Math/Linear Algebra Done Right/Vector Space\|$V$]].
> 
> Proof:
> 
> Let $e_{1},\dots,e_{n}$ be the [[Math/Linear Algebra Done Right/Orthonomal\|orthonormal basis]] guarenteed by the [[Math/Linear Algebra Done Right/Spectral Theorem\|spectral theorem]], and $v=\langle v,e_{1} \rangle e_{1}+\dots+\langle v,e_{n} \rangle e_{n}$. Therefore, we have $\sqrt{ T^*T }v=s_{1}\langle v,e_{1} \rangle e_{1}+\dots+s_{n}\langle v,e_{n} \rangle e_{n}$. By the [[Math/Linear Algebra Done Right/Polar Decomposition\|polar decomposition]], we know that $T=S\sqrt{ T^*T }$. By the charateristicis of isometries, we know $Se_{1},\dots,Se_{n}$ is also orthonormal, therefore, let $f_{j}=Se_{j}$ and we get the desired.
> 
> $\blacksquare$

> [!info]  Singular values without taking square root of an operator
> Suppose $T\in \mathcal{L}(V)$. Then the singular values of $T$ are the nonnegative square roots of the eigenvalues of $T^*T$, with each eigenvalue $\lambda$ repeated $\text{dim }E(\lambda,T^*T)$ times.
> 
> Proof:
> 
> Not really hard to see that for every $\lambda_{j}$ that is an eigenvalue of $T^*T$, we have $\sqrt{ T^*T }e_{j}=\sqrt{ \lambda_{j} }e_{j}$.
> 
> $\blacksquare$

