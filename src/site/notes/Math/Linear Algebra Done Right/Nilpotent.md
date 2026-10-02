---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/nilpotent/","dg-note-properties":{}}
---

# Nilpotent
> [!example] Definition of nilpotent
> An [[Math/Linear Algebra Done Right/Operator\|operator]] is called nilpotent if some power of it equals $0$

> [!info]  Nilpotent operator rasied to [[Math/Linear Algebra Done Right/Dimension\|dimension]] of domain is $0$
> Suppose $N\in$[[Math/Linear Algebra Done Right/L(V)\|L(V)]] is nilpotent. Then $N^{\text{dim }V}=0$
> 
> Proof:
> 
> Beacause $N$ is nilpotent, we have $N^j=0$ for some positive integer $j$. Therefore we have $\text{null }(N-0\cdot I)^j=V$ which is $G(0,N)=V$. Therefore, we have $N^{\text{dim  }V}$.
> 
> $\blacksquare$

One thing good for nilpotent operators is that, they always have a [[Math/Linear Algebra Done Right/Upper-triangular Matrix\|upper-triangular matrix]].

> [!info]  [[Math/Linear Algebra Done Right/Matrices\|matrix]] of nilpotent operator
> Suppose $N$ is a nilpotent operator on [[Math/Linear Algebra Done Right/Vector Space\|$V$]]. Then there is a basis of $V$ with respect to which the matrix of $N$ has the form 
> $$
> \begin{pmatrix}
0 &  & * \\
 & \ddots &  \\
0 &  & 0
\end{pmatrix}
> $$
> Proof:
> 
> Suppose $\text{null }N=k$, we pick a [[Math/Linear Algebra Done Right/Basis\|basis]] of $\text{null }N$ and let it be the first $k$ columns of the matrix. Because it's a basis of $\text{null }N$, the first $k$ columns should be all $0$. 
> 
> Then we the basis to a basis of $\text{null }N^2$.  Let the extra part of the new basis be the following columns of the matrix. Apply $N$ to the new vectors of the basis, we get a vector in $\text{null }N$, which means it can be written in a [[Math/Linear Algebra Done Right/Linear Combination\|linear combination]] of the previous basis vectors in $\text{null }N$. 
> 
> Continue in this fashion to complete the matrix, once we reach to $\text{null }N^{\text{dim }V}$, we are able to fill out all the entries in the matrix. Easy to see, the matrix should be in the form as we ex.
> 
> $\blacksquare$


> [!info]  Basis corresponding to a nilpotent operator
> Suppose $N\in \mathcal{L}(V)$ is nilpotent. Then there exist vectors $v_{1},\dots,v_{n}\in V$ and nonnegative integers $m_{1},\dots,m_{n}$ such that
> 
> (a) $N^{m_{1}}v_{1},\dots,Nv_{1},v_{1},\dots,N^{m_{n}}v_{n},\dots,Nv_{n},v_{n}$ is a basis of $V$
> 
> (b) $N^{m_{1}+1}v_{1}=\dots=N^{m_{n}+1}v_{n}=0$
> 
> Proof:
> 
> Suppose $p$ is the index of nilpotency, so $n^p = 0$. We pick a basis for the quotient space $\text{null } N^p / \text{null } N^{p-1}$. Let these be our first leader vectors.
>
Then we apply $N$ to these vectors, dropping them into $\text{null } n^{p-1}$. We extend this dropped set to a basis of the next quotient space $\text{null } n^{p-1} / \text{null } n^{p-2}$. Let the extra part of the new basis be the new leader vectors for this level.
>
Continue in this fashion to complete the quotient space bases down to $\text{null } n / \{0\}$. Once we reach the bottom, we are able to collect all leader vectors $v_1, \dots, v_k$.
>
Apply $N$ repeatedly to each leader vector $v_j$ picked at level $m_j + 1$ to get a sequence. because its local minimal polynomial has degree $m_j + 1$, the vectors in its own sequence cannot form a linear combination to $0$.
>
Because we picked the extra parts as independent representatives in the quotient spaces, linear combinations from different sequences will not cancel each other out.
>
Easy to see, the total count of vectors in all sequences equals the dimension of $v$, so they form a basis of $v$.
>
>$\blacksquare$



