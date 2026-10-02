---
{"dg-publish":true,"permalink":"/homework-adv-linear-algebra/homework-1-oct-1/","dg-note-properties":{}}
---

1. Proof that if $a \in \mathbf{F}$, $v \in V$, $av=0$, then $a=0$, or $v=\mathbf{0}$.

Proof:

Since $av=0$, by definition, we have $av=av+av$. If $a\neq0$, we can multiply $\frac{1}{a}$ on both sides and get the equation $v=v+v$. Since $\mathbf{0}$ vector is unique, we get $v=\mathbf{0}$. If $a=0$, we get the desired.

$\blacksquare$

2. For each of the following subsets of $\mathbf{F^3}$, determine whether it is a subspace of $\mathbf{F^3}$.
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

3. Prove or give the counterexample: If $U_{1},U_{2},W$ are subspaces of $V$ such that 
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

4. Prove or give the counterexample: If $U_{1},U_{2},W$ are subspaces of $V$ such that 
$$
U_{1}\oplus W=U_{2}\oplus W
$$
then $U_{1}=U_{2}$.

Proof:

