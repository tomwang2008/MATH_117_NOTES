---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/square-root/","dg-note-properties":{}}
---

# Square Root
> [!example] Definition of square root
> An [[Math/Linear Algebra Done Right/Operator\|operator]] $R$ is called a square root of an operator $T$ if and only if $T=R^2$

> [!info]  Each [[Math/Linear Algebra Done Right/Positive\|positive]] operator has one positive square root
> Every positive operator on [[Math/Linear Algebra Done Right/Vector Space\|$V$]] has a unique positive square root.
> 
> Proof:
> 
> We could use the same idea we did in the proof of the [[Math/Linear Algebra Done Right/Positive\|charatieristics of positive operators]].
> 
> $\blacksquare$

> [!example] Notation of square root
> If $T$ is a positive operator, then $\sqrt{ T }$ denotes the unique square root of $T$.

> [!info]  Identity plus nilpotent has a square root
> Suppose $N\in \mathcal{L}(V)$ is [[Math/Linear Algebra Done Right/Nilpotent\|nilpotent]]. Then $I+N$ has a square root.
> 
> Proof:
> 
> Let $N \in \mathcal{L}(V)$ be a nilpotent operator. By the definition of nilpotency, there exists some positive integer $m$ such that $N^m = 0$.
Recall the Taylor series expansion for the square root function $\sqrt{1+x}$ around $0$:
$$(1+x)^{1/2} = 1 + \frac{1}{2}x - \frac{1}{8}x^2 + \frac{1}{16}x^3 - \dots = \sum_{k=0}^{\infty} \binom{1/2}{k} x^k$$
We can formally substitute the operator $N$ for $x$. Because $N^m = 0$, all terms in the infinite series where the power of $N$ is greater than or equal to $m$ will become the zero operator. This means the infinite series naturally truncates into a finite sum.
>
We can define a new operator $R \in \mathcal{L}(V)$ using this finite sequence:
>
$$R = I + \frac{1}{2}N - \frac{1}{8}N^2 + \dots + \binom{1/2}{m-1}N^{m-1}$$
>
Since $R$ is constructed as a finite polynomial of the operator $N$, $R$ is a well-defined linear operator on $V$.
>
To prove that $R$ is the square root of $I + N$, we must show that $R^2 = I + N$.
>
From the algebraic properties of formal power series, we know that squaring the infinite series for $(1+x)^{1/2}$ yields exactly $1 + x$. When we compute $R^2$, we are multiplying polynomials of the operator $N$. Because powers of $N$ commute with each other, the algebraic expansion of $R^2$ matches the expansion of the formal power series, up to the degree $m-1$.
>
Any cross-multiplied terms in $R^2$ that result in a power of $N$ equal to or greater than $m$ will vanish (since $N^m = 0$). Therefore, the algebraic expansion perfectly simplifies, leaving only:
>
$$R^2 = I + N$$
>
Thus, $R$ is a valid square root of $I + N$.
>
$\blacksquare$

> [!info]  Over $\mathbb{C}$, invertible operator have square roots
> Suppose $V$ is a complex [[Math/Linear Algebra Done Right/Vector Space\|vector space]] and $T\in \mathcal{L}(V)$ is [[Math/Linear Algebra Done Right/Invertible\|invertible]]. Then $T$ has a square root.
> 
> Proof:
> 
> Suppose $\lambda_{1},\dots,\lambda_{m}$ are the distinct [[Math/Linear Algebra Done Right/Eigenvalue\|eigenvalues]] of $T$. Consider every $T\big|_{G(\lambda_{j},T)}$, we could rewrite it into the form of $\lambda_{j}I+(T\big|_{{G(\lambda_{j},T)}}-\lambda_{j}I)$. Notice $T\big|_{{G(\lambda_{j},T)}}-\lambda_{j}I$ is nilpotent, we let $T\big|_{{G(\lambda_{j},T)}}-\lambda_{j}I=N$. Therefore, $T\big|_{{G(\lambda_{j},T)}}=\lambda_{j}I+N=\lambda _j\left( I+\frac{N}{\lambda_{j}} \right)$, which has a sqaure root guarenteed by our last result. Let it be $R_{j}$
> 
> Because [[Math/Linear Algebra Done Right/Generalized Eigenspace\|$V=G(\lambda_{1},T)\oplus G(\lambda_{2},T)\oplus\dots \oplus G(\lambda_{m},T)$]], we could rewrite every $v\in V$ into 
> $$
> v=u_{1}+\dots+u_{m}
> $$
> where $u_{j}\in G(\lambda_{j},T)$. Therefore, we define the square root of $T$ as 
> $$
> Rv=\sum_{i=1}^mR_{i}u_{i}
> $$
> $R$ is a square root of $T$, as we desired.
> 
> $\blacksquare$

