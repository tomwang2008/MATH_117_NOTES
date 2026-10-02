---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/subspace/","dg-note-properties":{}}
---

# Subspace

> [!example] Definition of a supspace
> A subset U of V is called a supspace if U is a [[Math/Linear Algebra Done Right/Vector Space\|Vector Space]]

However, we don't need to check if all the properties of vector space hold in U, the only three things we need to check is:
- Additive Identity
  $0\in U$
- Closed under addition
  $u,v\in U, u+v\in U$
- Closed under scalar multiplication
  $\lambda \in F, u\in U$ then $\lambda u\in U$

>[!info] Proof:
>Since $U$ is a subset of $V$, many good properties are inherited from V such as commutativity and associativity, the only two properties we need to prove is additive identity and additive inverse.
>
>$0\in U$ so the additive identity holds.
>
>Since addition makes sense in $U$ and $U$ is closed under scalar multiplication, there exists $(-1)v$ in $U$ where $v+(-1)v=0$ for $v\in U$.
>
>$\blacksquare$

Now we prove an intuitive property of subspace
>[!info] Every subspace of a [[Math/Linear Algebra Done Right/Finite-dimensional Vector Space\|finite-dimensional vector space]] is finite-dimensional.
>Proof:
>We start from $\set{0}$, if the subspace $U\not = \set{0}$, then we add a vector $v_1\in U$. If $U\not = \text{span}(v_1)$, we add a vector $v_2\in U$ where $v_2\notin \text{span}(v_1)$. We continue to repeat this process: 
>
>For the $j^{\text{th}}$ turn, if we still didn't have the spanning list of $U$, we add a vector $v_j\in U$ where $v_j\notin \text{span}(v_1,\dots,v_{j-1})$. 
>
>This process will eventually terminate because the list we construct is [[Math/Linear Algebra Done Right/Linear Independence\|linearly independent]] and the length of the list cannot be larger than the spanning list of the vector space.
>
>$\blacksquare$
>


Next: [[Math/Linear Algebra Done Right/Sum of Subspace\|Sum of Subspace]]

