---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/injectivity/","dg-note-properties":{}}
---

# Injectivity

>[!example] Definition of Injective
>A function $T\ :\ V\to W$ is called injective if $Tu=Tv$ implies $u=v$.

Here is an easy way to check if a linear map is injective.

>[!info] Injectivity is equivalent to null space equal 0
>Let $T\in$ [[Math/Linear Algebra Done Right/L(V,W)\|L(V,W)]]. Then $T$ is injective if and only if $\text{null}\ T=\set{0}$. 
>
>Proof:
>Suppose $T$ is injective, then $Tv=Tu$ implies $u=v$. Therefore, $Ta=0=T0$ implies $a=0$.
>
>Suppose $\text{null}\ T=\set{0}$, if $Tu=Tv$ does not imply $u=v$, we have $Tu=Tv$ where $u\not =v$. This indicates that $T(u-v)=0$, thus, $\text{null}\ T\not=\set{0}$. Therefore, $T$ is injective.
>
>$\blacksquare$

Now we show that no linear map that maps the vector space to a smaller vector space can be injective.

>[!info] A map to a smaller dimensional vector space cannot be injective.
>
>Suppose [[Math/Linear Algebra Done Right/Vector Space\|$V$]] and $W$ are [[Math/Linear Algebra Done Right/Finite-dimensional Vector Space\|finite-dimensional vector space]] such that $\text{dim }V>\text{dim }W$. Then no linear map from $V$ to $W$ is injective.
>
>Proof:
>
>$$
>\begin{align}
>\text{dim null }T&=\text{dim }V-\text{dim range }T\\
>&\ge\text{dim }V-\text{dim }W\\
>&>0\\
>\end{align}
>$$
>From the statement above, $T$ cannot be injective.
>
>$\blacksquare$





