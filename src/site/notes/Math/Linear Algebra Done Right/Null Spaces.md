---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/null-spaces/","dg-note-properties":{}}
---

 
$\def\null{\text{null}\ }$

# Null Spaces

>[!example] Null Space or $\text{null}\ T$
>For $T\in\mathcal{L}(V,W)$, the null space of $T$, denoted null $T$, is the subset of $V$ containing of those vectors that $T$ maps to $0$. Mathematically, null space is expressed as:
>$$\text{null}\ T=\set{v\in V\ :\ Tv=0}$$
>

Now, the following shows that null space is a subspace of the vector space.

>[!info] The null space is a [[Math/Linear Algebra Done Right/Subspace\|subspace]] of [[Math/Linear Algebra Done Right/Vector Space\|$V$]].
>
>Proof:
>
>To verify $\null T$ is a subspace, we need to check if $\null T$ is closed under addition and scalar multiplication.
>
>Addition:
>For $u,v\in \null T$, $Tu+Tv=T(u+v)=0+0=0$. Thus, $u+v$ is also in $\null T$.
>
>Scalar multiplication:
>For $v\in \null$, $\lambda Tv=T(\lambda v)=0$. Thus, $\lambda v$ is also in $\null T$.
>
>$\blacksquare$


> [!info]  Sequence of increasing null spaces
> Suppose $T\in$[[Math/Linear Algebra Done Right/L(V)\|L(V)]]. Then
> $$
> \{ 0 \}=\text{null }T^0\subset \text{null }T^1\subset\dots \subset \text{null }T^k\subset \text{null }T^{k+1}\subset\dots
> $$
> Proof:
> 
> Suppose $v\in \text{null }T^k$, Then $T^k=0$. Hence $T^{k+1}v=T(T^kv)=T(0)=0$. Therefore, $v \in \text{null }T^{k+1}$. 
> 
> $\blacksquare$


> [!info]  Equality in the sequence of null space
> Suppose $T\in \mathcal{L}(V)$. Suppose $m$ is a nonnegative integer such that $\text{null }T^m=\text{null }T^{m+1}$. Then
> $$
> \text{null }T^m=\text{null }T^{m+1}=\text{null }T^{m+2}=\dots
> $$
> Proof:
> 
> It suffices to prove that $\text{null } T^{m+2} \subseteq \text{null } T^{m+1}$, as the reverse inclusion holds trivially for any linear operator, and the general result then follows by induction.
>
First, let us examine the intersection of $\text{range } T^m$ and $\text{null } T$. Suppose $u \in \text{range } T^m \cap \text{null } T$. Because $u \in \text{range } T^m$, there exists a vector $v \in V$ such that $u = T^m v$. Furthermore, since $u \in \text{null } T$, we have $Tu = 0$. Substituting the expression for $u$ yields $T(T^m v) = 0$, which implies $T^{m+1} v = 0$. Thus, $v \in \text{null } T^{m+1}$. By our initial hypothesis that $\text{null } T^{m+1} = \text{null } T^m$, it follows that $v$ must also be in $\text{null } T^m$. This implies $T^m v = 0$, and consequently, $u = 0$. Therefore, $\text{range } T^m \cap \text{null } T = \{0\}$.
>
Notice that the range of a linear operator shrinks or remains constant with successive applications, meaning $\text{range } T^{m+1} \subseteq \text{range } T^m$. Since the larger space $\text{range } T^m$ has a trivial intersection with $\text{null } T$, its subspace must as well. Hence, we can immediately deduce that $\text{range } T^{m+1} \cap \text{null } T = \{0\}$.
>
Now, suppose $x \in \text{null } T^{m+2}$. By definition, $T^{m+2} x = 0$, which can be naturally rewritten as $T(T^{m+1} x) = 0$. Let $y = T^{m+1} x$. Clearly, $y \in \text{range } T^{m+1}$, and the equation $T(y) = 0$ shows that $y \in \text{null } T$. Therefore, $y \in \text{range } T^{m+1} \cap \text{null } T$. Based on our previous deduction, this intersection contains only the zero vector, forcing $y = 0$. Thus, $T^{m+1} x = 0$, which means $x \in \text{null } T^{m+1}$.
>
We have shown that any vector in $\text{null } T^{m+2}$ is also in $\text{null } T^{m+1}$, establishing $\text{null } T^{m+2} = \text{null } T^{m+1}$. By induction, the sequence of null spaces remains constant for all subsequent powers.
>
>$\blacksquare$

> [!info]  Null space stop growing
> Suppose $T\in \mathcal{L}(V)$. Let $n=\text{dim }V$. Then
> $$
> \text{null }T^n=\text{null }T^{n+1}=\text{null }T^{n+2}
> $$
> Proof:
> 
> We only need to prove the first equation holds true. Now, suppose it doesn't hold true, which is $\text{null }T^n\neq \text{null }T^{n+1}$. By the two conclusion above, we get
> $$
> \text{null }T  \subsetneq \text{null }T^2 \subsetneq\dots \subsetneq \text{null }T^n
> $$
> Therefore, for every null spaec, the dimension increases at least by one. As we reaches $\text{null }T^n$, the dimension is greater than $\text{dim }V$. Which is impossible. Therefore, contradiction occurs as desired.
> 
> $\blacksquare$


> [!info]  $V$ is the direct sum of $\text{null }T^{\text{dim }V}$ and $\text{range }T^{\text{dim }V}$
> Suppose $T\in \mathcal{L}(V)$. Let $n=\text{dim }V$. Then
> $$
> V=\text{null }T^\text{dim }n \oplus \text{range }T^\text{dim n}
> $$
> Proof:
> 
> We first prove that $\text{null }T^n \cap \text{range }T^n=\{ 0 \}$. We prove by contradiction. Suppose it doesn't hold, then there exists $v\in V$ such that $T^nv=u$ and $T^n u=0$. Therefore, we have $T^{2n}v=T^n(T^nv)=0$, which leads to $v\in \text{null }T^{2n}$ and $v \not\in \text{null }T^n$. This contradicts the conclusion above. 
> 
> The sum of dimension equals the whole vector space can be deduced directly by the [[Math/Linear Algebra Done Right/Fundamental Theorem of Linear Maps\|Fundamental Theorem of Linear Maps]]. 
> 
> $\blacksquare$



