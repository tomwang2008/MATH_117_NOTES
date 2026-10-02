---
{"dg-publish":true,"permalink":"/math/principles-of-mathematical-analysis/complex-field/","dg-note-properties":{}}
---

# Complex Field
> [!example] Definition of complex number and its operations
> A complex number is an ordered pair $(a,b)$ of real numbers. 
> 
> Let $x=(a,b),y=(c,d)$ be two complex numbers. We write $x-y$ if and only if  $a=c$ and $b-d$. We define 
> $$
>\begin{align}
> x+y & =(a+c,b+d) \\
> xy & =(ax-bd,ad+bc)
\end{align}
> $$

> [!info]  Complex numbers form a field
> The definition of addition and multiplication turn the set of all complex numbers into a field, with $(0,0)$ and $(1,0)$ in the role of $1$ and $0$.
> 
> Proof:
> 
> As you should verify, it indeed is a field
> 

> [!example] Definition of imaginary unit
> We define the imaginary unit $i=(0,1)$.

As you should verify, $i^2=(-1,0)$.

A more familiar way to write complex numbers is to write $(a,b)$ ad $a+bi$. As you should verify, these two are equivalent.


> [!example] Definition of conjugate and the two parts of a complex number
> If $a,b$ are real and $z=a+bi$, then the complex number $\overline{z}=a-bi$ is called the conjugate of $z$. The numbers $a$ and $b$ are the real part and the imaginary part of $z$, respectively.
> 
> We shall occsionally write
> $$
> a=\mathrm{Re}(z)\ \ \ \  b=\mathrm{Im}(z)
> $$

 Here are some properties

- $\overline{z+w}=\overline{z}+\overline{w}$
- $\overline{zw}=\overline{z}\cdot \overline{w}$
- $z+\overline{z}=2\mathrm{Re}(z)$ and $z-\overline{z}=2i\mathrm{Im}(z)$
- If $z\neq 0$, $z\overline{z}$ is real and positive 

> [!example] Definition of absolute value (or [[Math/Linear Algebra Done Right/Norm\|norm]])
> If $z$ is a complex number, its absolute value (or norm) $\lvert z \rvert$ is the nonnegative square root of $z\overline{z}$; that is $\lvert z \rvert=(z\overline{z})^{\frac{1}{2}}$.


 > [!info]  Properties of absolute value
 > (a) $\lvert z \rvert>0$ unless $z=0$
 > (b) $\lvert \overline{z} \rvert=\lvert z \rvert$
 > (c) $\lvert zw \rvert=\lvert z \rvert\lvert w \rvert$
 > (d) $\lvert \mathrm{Re}(z) \rvert\leq \lvert z \rvert$
 > (e) $\lvert z+w \rvert\leq \lvert z \rvert+\lvert w \rvert$
 > 
 > Proof:
 > 
 > We only prove (e).
 > $$
> \begin{align}
\lvert z+w  \rvert^2 & =(z+w)(\overline{z}+\overline{w}) \\
 & =\lvert z \rvert ^2+2\mathrm{Re}(z\overline{w})+\lvert w \rvert ^2 \\
 & \leq \lvert z \rvert ^2+2\lvert z\overline{q} \rvert +\lvert w \rvert ^2 \\
 & =\lvert z \rvert ^2+2\lvert z \rvert \lvert w \rvert  +\lvert w \rvert ^2 \\
 & =(\lvert z \rvert +\lvert w \rvert )^2
\end{align}
> $$
> $\blacksquare$

