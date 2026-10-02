---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/polynomial/","dg-note-properties":{}}
---

# Polynomial

>[!example] Definition of Polynomial
>A funcion $p\ :\ \mathbf F\to \mathbf F$ is called a polynomial with coeiffients in $\mathbf F$ if there exist $a_1,\dots,a_n\in \mathbf F$ such that
>$$p(z)=a_0+a_1z+a_2z^2+\dots+a_nz^n$$
>for all $z\in \mathbf F$
>
 
Now we introduce what is the degree of a polynomial

> [!example] Definition of degree of a polynomial
> A polynomial $p\in$ [[Math/Linear Algebra Done Right/P(F)\|P(F)]] is said to have a degree of n if there exists $a_0, \dots, a_n\in F$ with $a_n \not = 0$ such that
> $$p(z)=a_0+a_1z+a_2z^2+\dots+a_nz^n$$
> for all $z\in \mathbf F$. If $p$ has a degree $n$, we write $\deg p = n$.

Note that the polynomial that is identically to 0 is said to have a degree of $-\infty$

>[!example] Definition product of polynomials
>If $p,q\in\mathcal{P}(\mathbf{F})$, then the polynomial $pq\in\mathcal{P}$ is defined by 
> $$
> (pq)(z)=p(z)q(z)
> $$

