---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/equivalence-of-injectivity-and-surjectivity/","dg-note-properties":{}}
---

# Equivalence of Injectivity and Surjectivity

The result in this note is remarkable — it states that for operators on a finite-dimensional vector space, either injectivity or surjectivity alone implies the other condition.

>[!info] Injectivity is equivalent to surjectivity in finite dimensions
>Suppose $V$ is finite-dimensional and $T\in$[[Math/Linear Algebra Done Right/L(V)\|L(V)]]. Then the following are equivalent:
>(a) $T$ is [[Math/Linear Algebra Done Right/Invertible\|invertible]]  
>(b) $T$ is [[Math/Linear Algebra Done Right/Injectivity\|injective]]
>(c) $T$ is [[Math/Linear Algebra Done Right/Surjectivity\|surjective]] 
>
>Proof:
>
>Easy to notice we only need to prove that injective and surjective are equivalent.
>
>Suppose $T$ is injective. By the [[Math/Linear Algebra Done Right/Fundamental Theorem of Linear Maps\|Fundamental Theorem of Linear Maps]],
> $$
> \text{dim rangeT}=\text{dim V}-\text{dim nullT}=\text{dim V}
> $$
> Thus, $T$ is surjective.
> 
> Suppose $T$ is surjective. By the [[Math/Linear Algebra Done Right/Fundamental Theorem of Linear Maps\|Fundamental Theorem of Linear Maps]], 
>  $$
> \text{dim nullT}=\text{dim V}-\text{dim rangeT}=0
> $$
> Thus, $T$ is injective.
> 
> $\blacksquare$



