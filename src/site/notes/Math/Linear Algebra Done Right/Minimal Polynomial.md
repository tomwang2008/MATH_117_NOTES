---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/minimal-polynomial/","dg-note-properties":{}}
---

# Minimal Polynomial


> [!info]  Minimal polynomial
> Suppose $T\in$[[Math/Linear Algebra Done Right/L(V)\|L(V)]]. Then there is a unique monic polynomial $p$ of smallest degree such that $p(T)=0$. 
> 
> Proof:
> 
> The [[Math/Linear Algebra Done Right/Characteristic Polynomial\|characteristic polynomial]] of $T$ guarenteed that $T$ has at least one polynomial that satisfy $p(T)=0$. Therefore, we only need to prove that the monic polynomial of smallest degree is unique.
> 
> Suppose it is not unique, we have $p,q\in \mathcal{P}(\mathbf{F})$ such that both polynomials that is monic and has the smallest degree such that $p(T)=q(T)=0$. Then, $(p-q)(T)=0$. Since both of them are monic, we have $\text{deg}(p-q)=\text{deg }(p)-1$. Therefore, $p$ and $q$ are not the polynomials that have the smallest degree, which contradicts our assumption.
> 
> $\blacksquare$


> [!example] Definition of minimal polynomial
> Suppose $T\in \mathcal{L}(V)$. Then the minimal polynomial of $T$ is the unique monic polynomial $p$ of smallest degree such that $p(T)=0$.


> [!info]  Minimal polynomial is the smallest polynomial such that $q(T)=0$
> Suppose $T\in \mathcal{L}(V)$ and $q\in \mathcal{P}(\mathbf{F})$. Then $q(T)=0$ if and only if $q$ is a polynomial multiple of the minimal polynomial of $T$.
> 
> Proof:
> 
> The backward side should be trivial, if $q$ is a polynomial multiple of the minimal polynomial, then $q(T)=0$. 
> 
> Now we prove the forward side, suppose it's not true. Let the minimal polynomial be $p$ and we have 
> $$
> q=np+r
> $$
> where $\text{deg }r<\text{deg }p$ and $r\neq0$.  
> 
> Since $q(T)=0$, we have $0=np(T)+r(T)$, which is $r(T)=0$. Because we assume $r\neq 0$, we have a new polynomial such that $r(T)=0$ and has a smaller degree. This contradicts the definition of minimal polynomial. Therefore, the forward side is true.
> 
> $\blacksquare$

> [!info]  [[Math/Linear Algebra Done Right/Eigenvalue\|Eigenvalues]] are the zeros of the minimal polynomial
> Let $T\in$[[Math/Linear Algebra Done Right/L(V)\|L(V)]]. Then the zeros of the minimal polynomial of $T$ are precisely the eigenvalues of $T$.
> 
> Proof:
> 
> From the last result, we know that the characteristic polynomial is a polynomial multiple of the minimal polynomial, therefore, all the zeros of the minimal polynomial should also be the zero of the characteristic polynomial. 
> 
> Now we prove the eigenvalues of $T$ appears in the zeros of the minimal polynomial at least once. Suppose $v_{1},\dots,v_{m}$ are distinct [[Math/Linear Algebra Done Right/Eigenvector\|eigenvectors]] corresponding to distinct eigenvalues $\lambda_{1},\dots,\lambda_{m}$. Let the minimal polynomial be $p$. We have
> $$
> p(T)v_{j}=0
> $$
> which is 
> $$
> p(\lambda_{j})v_{j}=0
> $$
> Since $v_{j}\neq 0$, we have $p(\lambda_{j})=0$. This leads to $\lambda_{j}$ is a zero of $p$ for every $j=1,\dots,m$.
> 
> $\blacksquare$

> [!info]  Minimal polynomial of [[Math/Linear Algebra Done Right/Complexification\|$T_{\mathbb{C}}$]] equals minimal polynomial of [[Math/Linear Algebra Done Right/Operator\|$T$]]
> Suppose [[Math/Linear Algebra Done Right/Vector Space\|$V$]] is a real vector space and $T\in \mathcal{L}(V)$. Then the minimal polynomial of $T_{\mathbb{C}}$ equals the minimal polynomial of $T$.
> 
> Proof:
> 
> Suppose $p$ is the minimal polynomial of $T$ and $q$ is the minimal polynomial of $T_{\mathbb{C}}$. First, we have 
> $$
> p(T_{\mathbb{C}})(u+iv)=p(T)u+ip(T)v=0
> $$
> Therefore, $p$ is a polynomial multiple of $q$.
> 
> We also have
> $$
> q(T_{\mathbb{C}})(u+iv)=0=q(T)u+iq(T)v
> $$
> Thereofore, $q$ is a polynomial multiple of $p$
> 
> Since two polynomials are a multiple of each other, they must be the same.
> 
> $\blacksquare$

