---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/determinant/","dg-note-properties":{}}
---

# Determinant
> [!example] Definition of determinant of an operator
> Suppose $T\in$[[Math/Linear Algebra Done Right/L(V)\|L(V)]].
> - If $\mathbf{F}=\mathbb{C}$, then the determinant of $T$ is the product of the eigenvalues of $T$, with each [[Math/Linear Algebra Done Right/Eigenvalue\|eigenvalue]] repeated according to its [[Math/Linear Algebra Done Right/Multiplicity\|multiplicity]].
>   
> - If $\mathbf{F}=\mathbb{R}$, then the determinant of $T$ is the product of the eigenvalues of $T_{\mathbb{C}}$, with each eigenvalue repeated according to its multiplicity.
> 
> The determinant of $T$ is denoted by $\det T$.

> [!info]  Determinant and charateristic polynomial
> Suppose $T\in \mathcal{L}(V)$. Let $n=\text{dim }V$. Then $\det T$ eqauls $(-1)^n$ times the constant term of the [[Math/Linear Algebra Done Right/Characteristic Polynomial\|characteristic polynomial]] of $T$.
> 
> Proof:
> 
> Shouldn't this be trivial?
> 

> [!info]  Characteristic polynomial, [[Math/Linear Algebra Done Right/Trace\|trace]], and determinant
> Suppose $T\in \mathcal{L}(V)$. Then the characteristic polynomial of $T$ can be written as
> $$
> z^n-\text{trace }Tz^{n-1}+\dots+(-1)^n(\det T)
> $$


> [!info]  Invertible is equivalent to nonzero determinant
> An operator on $V$ is [[Math/Linear Algebra Done Right/Invertible\|invertible]] if and only if its determinant is nonzero.
> 
> Proof:
> 
> If an operator $T$ is invertible, then $0$ is not an eigenvalue of $T$, therefore $\det T$ is nonzero and vice versa.
> 
> $\blacksquare$

> [!info]  Characteristic polynomial of $T$ equals $\det(zI-T)$
> Suppose $T\in \mathcal{L}(V)$. Then the characteristic polynomial of $T$ equals $\det(zI-T)$.
> 
> Proof:
> 
> Suppose $\lambda$ is an eigenvalue of $T$, then $z-\lambda$ is an eigenvalue of $zI-T$. Therefore, $\det (zI-T)=(z-\lambda_{1})\cdot\dots \cdot(z-\lambda_{n})$, which is exactly the characteristic polynomial of $T$.
> 
> $\blacksquare$


> [!example] Definition of determinant of a [[Math/Linear Algebra Done Right/Matrices\|matrix]] 
> Suppose $A$ is an n-by-n matrix. The determinant of $A$, denoted $\det A$, is defined by 
> $$
> \det A=\sum_{(m_{1},\dots,m_{n})\in \text{perm }n}(\text{sign }(m_{1},\dots,m_{n}))A_{m_{1},1}\cdot \cdot \cdot A_{m_{n},n}
> $$
> 

> [!info]  Interchanging two columns in a matrix 
> Suppose $A$ is a square matrix and $B$ is the matrix obtain from $A$ by interchanging two columns. Then
> $$
> \det A=-\det B
> $$
> Proof:
> 
> This shares the proof where we proved changing two entires of a permutation multiplies the [[Math/Linear Algebra Done Right/Sign\|sign]] by $-1$.
> 
> $\blacksquare$

> [!info]  Matrices with two equal columns
> If $A$ is a square matrix that has two equal columns, then $\det A=0$.
>
>Proof:
>
>Interchange the two equal columns, we get $\det A=-\det A$. Which leads to $\det A=0$.
>
>$\blacksquare$

> [!info]  Determinant is a linear function of each column
> Suppose $k,n$ are positive integers with $1\leq k\leq n$. Fix n-by-1 matrices $A_{.,1},\dots,A_{.,n}$ except $A_{.,k}$. Then the fucntion that takes an n-by-1 column vector $A_{.,k}$ to 
> $$
> \det (A_{.,1}\dots A_{.,k}\dots A_{.,n})
> $$
> is a linear map from the vector space of n-by-1 matrices with entries in $\mathbf{F}$ to $\mathbf{F}$.
> 

The following result is considerably important, it reveals some good properties of determinants.

> [!info]  Determinant is multiplicative
> Suppose $A$ and $B$ are square matrices of the same size. Then
> $$
> \det(AB)=\det(BA)=(\det A)(\det B)
> $$
> 
> Proof:
> 
> 
>
Let $A$ and $B$ be $n \times n$ matrices. We can write them as block matrices of their columns:
>
$A = (A_{.,1} \dots A_{.,n})$ and $B = (B_{.,1} \dots B_{.,n})$.
>
Let $e_k$ denote the $k$-th standard basis vector. It is clear that $Ae_k = A_{.,k}$. The $k$-th column of $B$ can be expressed as a linear combination of these basis vectors:
>
$$B_{.,k} = \sum_{m=1}^n B_{m,k}e_m$$
>
By the definition of matrix multiplication, the $k$-th column of $AB$ is simply the matrix $A$ multiplied by the $k$-th column of $B$. Therefore:
>
$$AB = (AB_{.,1} \dots AB_{.,n}) = \left( A\left(\sum_{m_1=1}^n B_{m_1,1}e_{m_1}\right) \dots A\left(\sum_{m_n=1}^n B_{m_n,n}e_{m_n}\right) \right)$$
>
Because the determinant function is linear with respect to each individual column, we can factor out the summations and the scalar multiples $B_{m,k}$ step by step:
>
$$\det(AB) = \sum_{m_1=1}^n \dots \sum_{m_n=1}^n B_{m_1,1} \dots B_{m_n,n} \det(Ae_{m_1} \dots Ae_{m_n})$$
>
At this stage, we are looking at a massive sum consisting of $n^n$ individual terms.
>
Let's examine the core matrix inside the determinant: $(Ae_{m_1} \dots Ae_{m_n})$. The columns of this matrix are drawn from the set of columns of $A$.
>
By the alternating property of the determinant, if a matrix has any two identical columns, its determinant is exactly $0$.
>
This means that in our massive sum, if any two indices in the sequence $(m_1, \dots, m_n)$ are the same, that entire term vanishes.
>
Consequently, the only terms that survive (i.e., evaluate to a non-zero number) are those where $m_1, \dots, m_n$ are all distinct. In other words, the sequence of indices must form a permutation of the integers $1$ through $n$.
>
Let $S_n$ denote the symmetric group (the set of all permutations of $n$ elements), and let $\pi \in S_n$. The sum collapses beautifully into:
>
$$\det(AB) = \sum_{\pi \in S_n} B_{\pi(1),1} \dots B_{\pi(n),n} \det(Ae_{\pi(1)} \dots Ae_{\pi(n)})$$
>
The matrix $(Ae_{\pi(1)} \dots Ae_{\pi(n)})$ is simply the original matrix $A$, but with its columns scrambled according to the permutation $\pi$.
>
By the alternating property, swapping any two columns multiplies the determinant by $-1$. Therefore, rearranging the scrambled columns back into their natural standard order $(Ae_1 \dots Ae_n)$ requires multiplying the determinant by the sign (or signature) of the permutation, denoted as $\text{sgn}(\pi)$ (which is $1$ for even permutations and $-1$ for odd permutations):
>
$$\det(Ae_{\pi(1)} \dots Ae_{\pi(n)}) = \text{sgn}(\pi) \det(Ae_1 \dots Ae_n) = \text{sgn}(\pi) \det(A)$$
>
Substituting this back into our summation gives:
>
$$\det(AB) = \sum_{\pi \in S_n} B_{\pi(1),1} \dots B_{\pi(n),n} \text{sgn}(\pi) \det(A)$$
>
Notice that $\det(A)$ is now a common constant factor across all terms in the sum. We can factor it completely outside the summation:
>
$$\det(AB) = \det(A) \left( \sum_{\pi \in S_n} \text{sgn}(\pi) B_{\pi(1),1} \dots B_{\pi(n),n} \right)$$
>
Look closely at the expression isolated inside the parentheses. This is exactly the foundational Leibniz formula for the determinant of matrix $B$! Thus, the entire summation perfectly evaluates to $\det(B)$:
>
$$\det(AB) = (\det A)(\det B)$$
>
$\blacksquare$

