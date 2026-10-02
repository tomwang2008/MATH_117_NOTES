---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/matrices/","dg-note-properties":{}}
---

# Matrix

>[!example] Definition of Matrix
>Let $m$ and $n$ denote positive integers. An $m-\text{by}-n$ matrix $A$ is a rectangular array of elements of $\mathbf F$ with $m$ rows and $n$ columns:
>$$
>A = \begin{pmatrix}
>A_{1,1} & \dots & A_{1,n} \\
>\vdots & & \vdots \\
>A_{m,1} & \dots & A_{m,n}
>\end{pmatrix}
>$$
>The notation $A_{j,k}$ denotes the entry in row $j$, column $k$ of $A$.


Matrices have many good properties. The most important thing is that: it's closed under addition and scalar multiplication.

>[!example] Definition of matrix addition
>The sum of two matrices of the **same size** is defined:
> $$
> \begin{pmatrix}
 A_{1,1}&\dots&A_{1,n}\\
>\vdots&&\vdots \\
>A_{m,1}&\dots&A_{m,n} \\
>\end{pmatrix}
>+
>\begin{pmatrix}
>C_{1,1} & \dots & C_{1,n}\\ 
>\vdots &  & \vdots \\
>C_{m,1} & \dots & C_{m,n}
>\end{pmatrix}
> = 
> \begin{pmatrix}
> A_{1,1}+C_{1,1} & \dots & A_{1,m}+C_{1,m} \\
>\vdots &  & \vdots \\
> A_{n,1}+C_{n,1} & \dots & A_{n,m}+C_{n,m} \\
>\end{pmatrix}
> $$ 
>

>[!example] Definition of matrix scalar multiplication
>The product of a scalar and a matrix is defined by:
>  $$
>\lambda
>\begin{pmatrix}
>A_{1,1} & \dots & A_{1,n} \\
>\vdots &  & \vdots \\
>A_{m,1} & \dots & A_{m,n}
>\end{pmatrix}
> =
> \begin{pmatrix}
>\lambda A_{1,1} & \dots & \lambda A_{1,n} \\
>\vdots &  & \vdots \\
>\lambda A_{m,1} &  \dots & \lambda A_{m,n} 
>\end{pmatrix}
> $$



Since matrices have such good properties, we naturally want to introduce a [[Math/Linear Algebra Done Right/Vector Space\|vector space]] for matrices. That is [[Math/Linear Algebra Done Right/The matrix representation of L, 𝗙ᵐ,ⁿ\|The matrix representation of L, 𝗙ᵐ,ⁿ]]. See the definition of this vector space in another note.

Matrices has another good property, that is: it has a product.

>[!example] Product of Matrices
>Suppose $A$ is an $m-\text{by}-n$ matrix and $C$ is an $n-\text{by}-p$ matrix. Then the product of $A$ and $C$ is an $m-\text{by}-p$ matrix whose entry in row $j$ column $k$ is given by the following equation.
> $$
> (AC)_{j,k}=\sum_{r=1}^{n}A_{j,r}C_{r,k}
> $$


We have multiple ways to understand the product of matrices.


## 1. Column of matrix product equals matrix times column

Suppose $A$ is an $m-\text{by}-n$ matrix and $C$ is an $n-\text{by}-p$ matrix. Then,
$$
(AC)_{.,k}=AC_{.,k}
$$
for $1\leq k\leq p$.

## 2. Linear combination of columns

Suppose $A$ is an $m-\text{by}-n$ matrix and $c=\begin{pmatrix}c_{1}\\\vdots\\c_{n} \end{pmatrix}$. Then, 
$$
Ac=c_{1}A_{.,1}+\dots+c_{n}A_{.,n}
$$
In other words, $Ac$ is the [[Math/Linear Algebra Done Right/Linear Combination\|linear combination]] of the columns of $A$, with the scalars that multiply the columns coming from $c$.

> [!example] Definition of identity matrix, $I$
> Suppose $n$ is a positive integer. The n - by - n [[Math/Linear Algebra Done Right/Diagonal Matrix\|diagonal matrix]] 
> $$
> \begin{pmatrix}
1 &  & 0 \\
 & \ddots &  \\
0 &  & 1
\end{pmatrix}
> $$
> is called the identity matrix and is denoted $I$.
> 
