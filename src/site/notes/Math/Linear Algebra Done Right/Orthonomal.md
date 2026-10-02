---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/orthonomal/","dg-note-properties":{}}
---

# Orthonomal
> [!example] Definition of orthonomal
> A list of vectors is called orthonormal if each vector in the list has [[Math/Linear Algebra Done Right/Norm\|norm]] 1 and is [[Math/Linear Algebra Done Right/Orthogonal\|orthogonal]] to all the other vectors in the list.
> 
> In other words, a list of vectors $e_{1},\dots,e_{n}$  in [[Math/Linear Algebra Done Right/Vector Space\|$V$]] is orthonomal if and only if
>  $$
> \langle e_j, e_k \rangle = 
\begin{cases} 
1 & \text{if } j = k, \\
0 & \text{if } j \neq k.
\end{cases}
> $$
> $\blacksquare$

> [!info]  The norm of an orthonormal linear combination
> Suppose $e_{1},\dots,e_{n}$ is an orthonomal list of vectors in $V$. Then 
>  $$\lVert a_{1}e_{1}+\dots+a_{n}e_{n} \rVert^2=\lvert a_{1} \rvert^2+\dots+\lvert a_{n} \rvert^2$$
>  For all $a_{1},\dots ,a_{n}\in \mathbf{F}$
>  
>  Proof:
>  
>  The conclusion can be reached by applying [[Math/Linear Algebra Done Right/Orthogonal\|pythagorean theorem]] $n$ times.
>  
>  $\blacksquare$

The result above has the following important corollary.

> [!info]  An orthonormal list is linearly independent
> Every orthonormal list of vectors is [[Math/Linear Algebra Done Right/Linear Independence\|linearly independent]].
> 
> Proof:
> $$
> \begin{align}
a_{1}v_{1}+\dots+a_{n}v_{n}=0 & \iff \lVert a_{1}e_{1}+\dots+a_{n}e_{n} \rVert ^2 =0\\
 & \iff \lvert a_{1} \rvert ^2+\dots+\lvert a_{n} \rvert ^2=0 \\
 & \iff a_{1}=\dots=a_{n}=0
\end{align}
> $$
> $\blacksquare$

Since orthonormal list is linearly independent, we'd like it to be a basis.

> [!example] Definition of orthonormal basis
> An orthonormal basis of $V$ is an orthonormal list of vectors in $V$ that is also a [[Math/Linear Algebra Done Right/Basis\|basis]] of $V$.
>


Easy to see, every orthonormal list with the right length is a basis of a $V$, since every linearly independent list with the right length is a basis.

The good point of using an orthogonal basis is that the coeffiecients can be computed easily.

> [!info]  Writing a vector as linear combination of orthonormal basis
> Suppose $e_{1},\dots,e_{n}$ is an orthogonal basis of $V$ and $v\in V$. Then 
> $$
> v=\langle v,e_{1} \rangle e_{1}+\dots+\langle v,e_{n} \rangle e_{n}
> $$
> and
> $$
> \lVert v \rVert ^2=\lvert \langle v,e_{1} \rangle \rvert ^2+\dots+\lvert \langle v,e_{n} \rangle \rvert ^2.
> $$
> Proof:
> 
> Let $v=a_{1}v_{1}+\dots+a_{n}v_{n}$ and we compute every $\langle v,e_{j} \rangle$. $\langle v,e_{j} \rangle=\langle a_{1}e_{1}+\dots+a_{n}e_{n},e_{j} \rangle=\langle a_{j}e_{j},e_{j} \rangle=a_{j}$.
> 
> Since $e_{1},\dots,e_{n}$ are orthogonal, applying the pythagoream theorem $n$ times and we get the desired.

Now we prove that such basis does exists.

> [!info]  Existence of orthonormal basis
> Every finite-dimensional inner product space has an orthonormal basis.
> 
> Proof:
> 
> Every linearly independent list can be transformed into an orthogonal list by the [[Math/Linear Algebra Done Right/Orthonomal\|gram-schimidt procedure]], including basis.
> 
> $\blacksquare$

In fact, every orthonormal list of vectors can be extended into a basis.

> [!info]  Orthonormal list extends to orthonormal basis
> Suppose $V$ is [[Math/Linear Algebra Done Right/Finite-dimensional Vector Space\|finite-dimensional]]. Then every orthonormal list of vectors in $V$ can be extended to an orthonormal basis of $V$.
> 
> Proof:
> 
> Let the list of orthonormal list be $e_{1},\dots,e_{j}$. Since the list is linearly independent, we can expand it to a basis $e_{1},\dots,e_{j},v_{j+1},\dots,v_{n}$. Now we use the Gram-Schimidt Procedure to transform it into a orhonormal basis.
> 
> $\blacksquare$

Orthonormal basis has even better properties, 

> [!info]  Upper-triangular matrix with respect to orthonormal basis
> Suppose $T\in$[[Math/Linear Algebra Done Right/L(V)\|L(V)]]. If $T$ has an [[Math/Linear Algebra Done Right/Upper-triangular Matrix\|upper-triangular matrix]] with respect to some basis of $V$, then $T$  has an upper-triangular matrix with respect to some orthonormal basis of $V$.
> 
> Proof:
> 
> Suppose the basis $v_{1},\dots,v_{n}$ is the basis respect to the upper=triangular matrix. Then by using the Gram-Schimidt Procedure, we get a new basis $e_{1},\dots,e_{n}$. Since we have $\text{span }(v_{1},\dots,v_{j})=\text{span }(e_{1},\dots,e_{j})$ for every $j=1,\dots,n$, $e_{1},\dots,e_{n}$ is a basis with respect to some upper-triangular of $T$.
> 
> $\blacksquare$

The direct collorary of this is, 

> [!info]  Schur's Theorem
> Suppose $V$ is finite-dimensional complex vector space and $T\in \mathcal{L}(V)$. Then $T$ has an upper triangular matrix with respect to some orthonormal basis of $V$.
> 
> Proof:
> 
> Every operator in a finite-dimensionall complex vector space has an upper-triangular matrix, and thus, has an upper-triangular matrix with respect to some orthonormal basis.
> 
> $\blacksquare$

