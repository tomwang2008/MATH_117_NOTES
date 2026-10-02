---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/the-relationship-between-map-and-its-dual-map/","dg-note-properties":{}}
---

# The relationship between map and its dual map

>[!info] The [[Math/Linear Algebra Done Right/Null Spaces\|null space]] of [[Math/Linear Algebra Done Right/Dual Map\|$T'$]] 
>Suppose $V$ and $W$ are [[Math/Linear Algebra Done Right/Finite-dimensional Vector Space\|finite-dimensional]], and $T\in$[[Math/Linear Algebra Done Right/L(V,W)\| $\mathcal{L}(V,W)$]]. Then 
>
> (a) $\text{null }T'$=[[Math/Linear Algebra Done Right/Ranges\| $ (\text{range }T)^0$]] (See [[Math/Linear Algebra Done Right/Annihilator\|Annihilator]] if you don't know what it is)
> 
> (b) $\text{dim null }T'=\text{dim null }T+\text{dim }W-\text{dim }V$
> 
> Proof:
> 
> a.
> For every $\varphi \in \text{null }T'$, $T'(\varphi)=\varphi \circ T$. $\forall v\in V$, $\varphi \circ T(v)=\varphi(w)=0$, where $w\in \text{range }T$. Thus, $\varphi \in (\text{range }T)^0\implies \text{null }T'\subset (\text{range }T)^0$
> 
> On the other hand, $\forall \phi \in(\text{range }T)^0$, $\phi(Tv)=(T'\phi)(v)=0$, where $v \in V$. Thus, $\phi \in \text{null }T'\implies(\text{range }T)^0\subset \text{null }T'$. 
> 
> Since $\text{null }T'\subset (\text{range }T)^0$ and $(\text{range }T)^0\subset \text{null }T'$, we conclude 
> $$
> \text{null }T'=(\text{range }T)^0
> $$
> 
> b.
> $$
> \begin{align}
\text{dim null }T'&=\text{dim }(\text{range }T)^0 &&(1)\\
&=\text{dim }W-\text{dim range }T &&(2)\\
&=\text{dim }W-(\text{dim }V-\text{dim null }T)&&(3) \\
&=\text{dim null }T+\text{dim }W-\text{dim }V&&(4)
\end{align}
> $$
>Note: from 1 to 2, we use the conclusion from the note [[Math/Linear Algebra Done Right/Annihilator\|Annihilator]], from 2 to 3, we use the [[Math/Linear Algebra Done Right/Fundamental Theorem of Linear Maps\|Rank-nullity Theorem]].
>
>$\blacksquare$
 

>[!info] [[Math/Linear Algebra Done Right/Surjectivity\|Surjectivity]] of a map results in [[Math/Linear Algebra Done Right/Injectivity\|injectivity]] in its dual map
>Suppose $V$ and $W$ is finite-dimensional, and $T\in \mathcal{L}(V,W)$. Then $T$ is surjective if and only if $T'$ is injective.
>
>Proof:
> $$
> \text{dim null }T'=\text{dim }W-\text{dim range }T
> $$
>From the equation above, we see that if $T$ is surjective, then $T'$ is injective and vice versa.
>
>$\blacksquare$



>[!info] The [[Math/Linear Algebra Done Right/Ranges\|range]] of $T'$
>Suppose $V$ and $W$ are finite-dimensional and $T\in \mathcal{L}(V,W)$. Then
>
>(a) $\text{dim range }T=\text{dim range }T'$
>
>(b) $\text{range }T'=(\text{null }T)^0$
>
>Proof:
>
>a.
> $$
> \begin{align}
\text{dim null }T'&=\text{dim }W-\text{dim range }T \\
\text{dim }W-\text{dim null }T'&=\text{dim range }T \\
\text{dim range }T'&=\text{dim range }T
\end{align}
> $$
> 
> b.
> For every $\phi \in \text{range }T'$, we have $\varphi \circ T=\phi$. $\forall v\in \text{null }T$, $\phi(v)=\varphi \circ T(v)=\varphi(0)=0$. Thus, $\phi \in (\text{null }T)^0\implies \text{range }T'\subset(\text{null }T')^0$.
> 
> On the other hand, 
> $$
> \begin{align}
\text{dim range }T'&=\text{dim range }T \\
&=\text{dim }W-\text{dim }(\text{range }T)^0 \\
&=\text{dim }W-\text{dim null }T' \\
&=\text{dim }(\text{null }T)^0
> 
\end{align}
> $$
> Since the dimension of the two vector spaces are the same and $\text{range }T'\subset(\text{null }T')^0$, we can conclude that $\text{range }T'=(\text{null }T)^0$.
> 
> $\blacksquare$

>[!info] Injectiviity of a map results in surjectivity of its dual map 
>Suppose $V$ and $W$ is finite-dimensional, and $T\in \mathcal{L}(V,W)$. Then $T$ is injective if and only if $T'$ is surjective.
>
>Proof:
>
> $$
> \text{dim range }T'=\text{dim }W-\text{dim null }T
> $$
> shown as above, $T$ is injective implies $T'$ is surjective and vice versa.
> 
> $\blacksquare$



