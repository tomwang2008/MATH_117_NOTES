---
{"dg-publish":true,"permalink":"/homework-adv-linear-algebra/homework-1-oct-1/","dg-note-properties":{}}
---

1\. Proof that if $a \in \mathbf{F}$, $v \in V$, $av=0$, then $a=0$, or $v=\mathbf{0}$.

Proof:

Since $av=0$, by definition, we have $av=av+av$. If $a\neq0$, we can multiply $\frac{1}{a}$ on both sides and get the equation $v=v+v$. Since $\mathbf{0}$ vector is unique, we get $v=\mathbf{0}$. If $a=0$, we get the desired.

$\blacksquare$

2\. For each of the following subsets of $\mathbf{F^3}$, determine whether it is a subspace of $\mathbf{F^3}$.
   (a) $\{ (x_{1},x_{2},x_{3})\in \mathbf{F}\ |\ x_{1}+2x_{2}+3x_{3} =0\}$
   (b) $\{ (x_{1},x_{2},x_{3})\in \mathbf{F}\ |\ x_{1}+2x_{2}+3x_{3}=4 \}$
   (c) $\{ (x_{1},x_{2},x_{3})\in \mathbf{F}\ |\ x_{1}x_{2}x_{3}=0 \}$
   (d) $\{ (x_{1},x_{2},x_{3})\in \mathbf{F}\ |\ x_{1}=5x_{3} \}$

Proof: 

(a) and (d) are subspaces of $\mathbf{F^3}$ and the rest are not. 

(a): $\mathbf{0}$ is a vector in the subset as verified

Let $(x_{1},x_{2},x_{3})$ and $(y_{1},y_{2},y_{3})$ be two vectors in the subset, the sum of the two vectors $(x_{1}+y_{1},x_{2}+y_{2},x_{3}+y_{3})$ satisfy the condition that
$$
\begin{align}
(x_{1}+y_1)+2(x_{2}+y_{2})+3(x_{3}+y_{3})&=(x_{1}+2x_{2}+3x_{3})+(y_{1}+2y_{2}+3y_{3}) \\
&=0+0 \\
&=0
\end{align}
$$
Therefore, the sum of the two vectors belongs to the subset. 

For $(x_{1},x_{2},x_{3})\in \mathbf{F^3}$, we verify that $a(x_{1},x_{2},x_{3})$ belongs to the subset, where $a \in \mathbf{F}$. Since $a(x_{1},x_{2},x_{3})=(ax_{1},ax_{2},ax_{3})$, we have $ax_{1}+2ax_{2}+3ax_{3}=0$. Thus $(ax_{1},ax_{2},ax_{3})$ is in the set, which indicates $a(x_{1},x_{2},x_{3})$ is in the set. 

In conclusion, subset (a) is a subspace.

(d):  $\mathbf{0}$ is a vector in the subset as verified

Let $(x_{1},x_{2},x_{3})$ and $(y_{1},y_{2},y_{3})$ be two vectors in the subset, the sum of the two vectors $(x_{1}+y_{1},x_{2}+y_{2},x_{3}+y_{3})$ satisfy the condition that
$$
\begin{align}
5(x_{3}+x_{3})-(x_{1}+y_{1})=(5x_{3}-x_{1})+(5y_{3}-y_{1})=0 \iff x_{1}+y_{1}=5(x_{3}+y_{3})
\end{align}
$$
Therefore, the sum of the two vectors belongs to the subset. 

For $(x_{1},x_{2},x_{3})\in \mathbf{F^3}$, we verify that $a(x_{1},x_{2},x_{3})$ belongs to the subset, where $a \in \mathbf{F}$. 
$$
x_{1}=5x_{3}\iff ax_{1}=5ax_{3}
$$
In conclusion, subset (d) is a subspace.

(b): $\mathbf{0}$ is not a vector of the subset, therefore (b) is not a subspace of $\mathbf{F^3}$.

(c): The two vector $(0,1,1)$ and $(1,0,1)$ in the subset does not satisfy the property closed under addition.

$\blacksquare$

3\. Prove or give the counterexample: If $U_{1},U_{2},W$ are subspaces of $V$ such that 
$$
U_{1}+W=U_{2}+W
$$
then $U_{1}=U_{2}$.

Proof:

We give the counterexample of $V=\mathbf{F^3}$ and
$$
\begin{align}
U_{1}&=\{ (x_{1},x_{2},0) \ |\ x_{1},x_{2} \in \mathbf{F}\} \\
U_{2}&=\{ (x_{1},0,0) \ |\ x_{1} \in \mathbf{F}\} \\
W&=\{ (0,x_{2},x_{3}) \ |\ x_{2},x_{3} \in \mathbf{F}\}
\end{align}
$$

$U_{1}+W=U_{2}+W$ as verified, however, $U_{1}\neq U_{2}$.

$\blacksquare$

4\. Prove or give the counterexample: If $U_{1},U_{2},W$ are subspaces of $V$ such that 
$$
U_{1}\oplus W=U_{2}\oplus W
$$
then $U_{1}=U_{2}$.

Proof:

We give the counterexample of $V=\mathbf{F^2}$ that 
$$
\begin{align}
U_{1}&=\{ (0,y)\ |\ y\in \mathbf{F} \} \\
U_{2}&=\{ (x,x)\ |\ x \in \mathbf{F} \} \\
W&=\{ (x,0)\ |\ x \in \mathbf{F} \}
\end{align}
$$
It's easy to verify that both sums are direct sums and add up to be the whole vector space but $U_{1}\neq U_{2}$.

$\blacksquare$

5\. Prove that if $(v_{1},\dots,v_{n})$ spans/is linearly independent, then so does/is the list 
$$
(v_{1}-v_{2},v_{2}-v_{3},\dots,v_{n-1}-v_{n},v_{n})
$$
Proof:

If $(v_{1},\dots,v_{n})$ is linearly independent, we have 
$$
0=a_{1}v_{1}+a_{2}v_{2}+\dots+a_{n}v_{n}\iff0=a_{1}=\dots=a_{n}
$$
We prove that 
$$
0=b_{1}(v_{1}-v_{2})+\dots+b_{n-1}(v_{n-1}-v_{n})+b_{n}v_{n} \iff 0=b_{1}=\dots=b_{n}
$$
Rearranging the equation, we get 
$$
0=b_{1}v_{1}+(b_{2}-b_{1})v_{2}+\dots+(b_{n}-b_{n-1})v_{n}
$$
Since the list $(v_{1},\dots,v_{n})$ is linearly independent, we get 
$$
b_{1}=b_{2}-b_{1}=\dots=b_{n}-b_{n-1}=0
$$
Therefore, $0=b_{1}=b_{2}=\dots=b_{n}$.

If $(v_{1},\dots,v_{n})$ spans the vector space $V$, we have for $v\in V$ and $a_{i}\in \mathbf{F}$ where $i=1,\dots,n$
$$
v=a_{1}v_{1}+\dots+a_{n}v_{n}
$$
For the list $(v_{1}-v_{2},\dots,v_{n})$, and some $b_{i}\in \mathbf{F}$ where $i=1,\dots,n$, we want
$$
v=b_{1}(v_{1}-v_{2})+\dots+b_{n}v_{n}
$$
which could be obtained by letting $b_{1}=a_{1},\ b_{2}=(a_{2}-a_{1}),\dots,b_{n}=a_{n}-a_{n-1}$ and as verified, $(v_{1}-v_{2},\dots,v_{n})$ spans $V$

$\blacksquare$

6\. Prove that $\mathbf{F^\infty}$ is infinite dimensional.

Proof:

By the way of contradiction, assume $\mathbf{F^\infty}$ is finite dimensional. Therefore some list spans the whole vector space, let the list be $(v_{1},\dots,v_{n})$, the span of the list has a dimension of at most $n$. However, the dimension of 
$$
\begin{align}
\text{span}(((a_{1},0,\dots),(0,a_{2},0,\dots),(0,0,a_{3},0,\dots),\dots,(0,\dots,a_{n},0,\dots),(0,\dots,a_{n},a_{n+1},0,\dots))) 
\in \mathbf{F^\infty}
\end{align}
$$
is $n+1$, where $a_1,\dots,a_{n+1}\in \mathbf{F}$. Contradiction occurs, therefore $\mathbf{F^\infty}$ is infinite dimensional.

$\blacksquare$

7\. Suppose that $V$ is finite dimensional and $U$ is a subsapce of $V$ such that $\text{dim }U= \text{dim }V$. Prove that $U=V$.
   
Proof:

By the way of contradiction, assmue $U\neq V$. Let $(u_{1},\dots,u_{m})$ and $(v_{1},\dots,v_{n})$ be bases of $U$ and $V$. Because $\text{dim }U=\text{dim }V$, we have $m=n$. Since $U\neq V$, there exists a $v\in V$ such that $v\not\in \text{span}(u_{1},\dots,u_{n})$. So the list $(u_{1},\dots,u_{m},v)$ is linearly independent, however, by the linear independecne lemma, the length of linearly independent list $\leq$ the length of spanning list. Contradiction occurs because we now have a linearly independent list whose length is longer than a spanning list. Therefore, $U=V$.

$\blacksquare$

8\. Suppose $U$ and $V$ are subspaces of $\mathbb{R}^8$ such that $\text{dim }U=3$, $\text{dim }V=5$, and $U+V=\mathbb{R}^8$. Prove that $U\cap V=\{ 0 \}$.
   
Proof:

We have $\text{dim }(U+V)=\text{dim }U+\text{dim }V-\text{dim }(U\cap V)$, which gives us that $\text{dim }(U\cap V)=0$. Therefore, $U\cap V=\{ 0 \}$.

$\blacksquare$

 9\. Suppose that $U$ and $V$ are both five dimensional subspaces of $\mathbb{R}^9$. Prove that $U\cap V\neq \{ 0 \}$.

Proof:

Use the same formula above to get $\text{dim }(U\cap V)=1$. Therefore, $U\cap V\neq \{ 0 \}$.

$\blacksquare$

10\. Suppose that $T \in \mathcal{L}(V,W)$ is injective and $(v_{1},\dots,v_{n})$ is linearly independent in $V$. Prove that $(Tv_{1},\dots,Tv_{n})$ is linear independent in $W$.

Proof:

For any linear combination such that 
$$
a_{1}Tv_{1}+\dots+a_{n}Tv_{n}=0
$$
We have 
$$
T(a_{1}v_{1}+\dots+a_{n}v_{n})=0
$$
Since $T$ is injective, the only way for it to be zero is that the linear combination of $a_{1}v_{1}+\dots a_{n}v_{n}=0$. Because the list $(v_{1},\dots,v_{n})$ is linearly independent, we get $a_{1}=\dots=a_{n}=0$.

$\blacksquare$

11\. Suppose that $V$ is finite dimensional and that $T\in \mathcal{L}(V,W)$. Prove that there exists a subspace of $U$ of $V$ such that $U\cap \text{null }T=\{ 0 \}$ and $\text{range }T=\{ Tu\ |\ u\in U \}$.

Proof:

Let $(v_{1},\dots,v_{r})$ be a basis of $\text{null }T$ and we extend it into a basis of $V$, $(v_{1},\dots,v_{r},u_{1},\dots,u_{m})$. We prove that $U=\text{span }(u_{1},\dots,u_{m})$. By our definition, we get $U\cap \text{null }(T)=\{ 0 \}$. For any $v\in V$, we have $v=a_{1}v_{1}+\dots+a_{r+m}u_{m}$, therefore, 
$$
\begin{align}
T(v)&=T(a_{1}v_{1}+\dots+a_{r+m}u_{m}) \\
&=T(a_{1}v_{1}+\dots+a_{r}v_{r})+T(a_{1+r}u_{1+r}+\dots+a_{r+m}u_{r+m}) \\
&=T(a_{1+r}u_{1+r}+\dots+a_{r+m}u_{r+m}) \\
&=Tu
\end{align}
$$

Hence $\text{range }T=\{ Tu\ |\ u\in U \}$.

$\blacksquare$

12\. Suppose that $V$ is a finite dimensional and $S,T\in L(V)$. Prove that $ST=I$ if and only if $TS=I$, where $I$ is the identity in $V$.

Proof:

$(\implies)$
Suppose we have a basis of $V$ $(v_{1},\dots,v_{n})$. Since $ST=I$, we have $(Tv_{1},\dots,Tv_{n})$ should also be a basis of $V$, otherwise, the output of $S$ should have a smaller dimension of $V$ but that contradicts that $ST=I$. Therefore, we have $S(Tv_{i})=v_{i}$. 

For every $Tv_{i}$, we have $TS(Tv_{i})=Tv_{i}=I(Tv_{i})$, since $(Tv_{1},\dots,Tv_{n})$ spans $V$, we have $TS=I$. 

$(\impliedby)$
The reverse side can be obtained by interchanging $S$ and $T$.

$\blacksquare$

