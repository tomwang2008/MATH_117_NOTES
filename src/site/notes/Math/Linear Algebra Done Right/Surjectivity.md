---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/surjectivity/","dg-note-properties":{}}
---

# Surjectivity

>[!example] Definition of Surjectivity
>A function $T\ :\ V\to W$ is called surjective if its [[Math/Linear Algebra Done Right/Ranges\|range]] equals [[Math/Linear Algebra Done Right/Vector Space\|$W$]].
>

Now, we show that no [[Math/Linear Algebra Done Right/Linear Map\|linear map]] from a [[Math/Linear Algebra Done Right/Finite-dimensional Vector Space\|finite-dimensional vector space]] to a bigger vector space can be surjective.

>[!info] A map to a larger dimensional vector space is not surjective
>
>Suppose $V$ and $W$ are finite-dimensional vector spaces such that $\text{dim }V<\text{dim }W$. Then no linear map from $V$ to $W$ is surjective.
>
>Proof:
>
>$$
>\begin{align}
>\text{dim range }T&=\text{dim }V-\text{dim null }T\\
>&\leq \text{dim }V\\
>&<\text{dim }W\\
>\end{align}
>$$
>From the definition above, $T$ is not surjective.
>
>$\blacksquare$


>


