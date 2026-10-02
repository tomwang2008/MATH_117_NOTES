---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/characteristic-polynomial/","dg-note-properties":{}}
---

# Charateristic Polynomial
> [!example] Definition of charateristic polynomial
> Suppose $V$ is a complex [[Math/Linear Algebra Done Right/Vector Space\|vector space]] and $T\in$[[Math/Linear Algebra Done Right/L(V)\|L(V)]]. Let $\lambda_{1},\dots,\lambda_{m}$ denote the distinct [[Math/Linear Algebra Done Right/Eigenvalue\|eigenvalues]] of $T$, with [[Math/Linear Algebra Done Right/Multiplicity\|multiplicities]] $d_{1},\dots,d_{m}$. Then [[Math/Linear Algebra Done Right/Polynomial\|polynomial]] 
> $$
> (z-\lambda_{1})^{d_{1}}\dots(z-\lambda_{m})^{d_{m}}
> $$
> is called the characteristic polynomial of $T$

> [!example] Definition of characterisitic polynomial on a real vector space
> Suppose $V$ is a real vector space and $T\in \mathcal{L}(V)$. Then the characterisitic polynomial of $T$ is defined to be the characterisitic polynomial of $T_{\mathbb{C}}$.


> [!info]  Degree and zeros of characteristic polynomial
> Suppose $V$ is a complex vector space and $T\in \mathcal{L}(V)$. Then
> 
> (a) the characteristic polynomial of $T$ has degree [[Math/Linear Algebra Done Right/Dimension\|$\text{dim V}$]];
> 
> (b) the zeros of the characteristic polynomial of $T$ are the eigenvalues of $T$.
> 
> Proof:
> 
> The two results directly follows the definition of characterisitic polynomial.
> 
> $\blacksquare$

> [!info]  Characteristic polynomial of [[Math/Linear Algebra Done Right/Complexification\|$T_{\mathbb{C}}$]]
> Suppose $V$ is a real vectors space and $T\in \mathcal{L}(V)$. Then the coeffiecients of the charecteristic polynomial of $T_{\mathbb{C}}$ are all real.
> 
> Proof:
> 
> Becauase every eigenvalue $\lambda$ of $T_{\mathbb{C}}$ come in pairs. Therefore the characteristic polynomial of $T_{\mathbb{C}}$ inclues the factor $(z-\lambda)^m$ and $(z-\overline{\lambda})^m$. Putting them toghether, we get $(z^2-\mathrm{Re}(\lambda)z+|\lambda|^2)^m$. 
> 
> Therefore,  in the characteristic polynomial of $T_{\mathbb{C}}$, every non-real eigenvalue combines with its conjugate, giving us a real coefficient polynomial. So there are no complex coeifficient in the polynomial
> 
> $\blacksquare$

> [!info]  Degree and zeros of characterisitc polynomial
> Suppose $V$ is real vector space and $T\in \mathcal{L}(V)$. Then
> 
> (a) the coeifficients of the characterisitc polynomial of $T$ are all real
> 
> (b) the characteristic polynomial of $T$ has degree of $\text{dim }V$
> 
> (c) the [[Math/Linear Algebra Done Right/Eigenvalue\|eigenvalue]] of $T$ are precisely the real zeros of the characterisitc polynomial of $T$.
> 
> Proof:
> 
> (a) and (b) should be trivial.
> 
> (c) Since the characteristic polynomial of $T$ is defined by the characteristic polynomial of $T_{\mathbb{C}}$, all the zeros of the characteristic polynomial of $T$ is a eigenvalue of $T_{\mathbb{C}}$, and $\lambda$ is an eigenvalue of $T_{\mathbb{C}}$ if and only if $\lambda$ is an eigenvalue of $T$. Therefore all the zeros of the charachterisitic polynomial of $T$ are the eigenvalues of $T$ . Vice versa.
> 
> $\blacksquare$

