---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/span/","dg-note-properties":{}}
---

# Span

> [!example] Definition of Span
> A span is the set of all [[Math/Linear Algebra Done Right/Linear Combination\|Linear Combination]] of a list of vectors $v_1,\dots,v_n$ denoted span$(v_1,\dots,v_n)$.
> $$\text{span}(v_1,\dots,v_n)=\set{a_1v_1+\dots+a_nv_n\ :\ a_1,\dots,a_n \in F}$$

The following statement reveals the relationship between span and [[Math/Linear Algebra Done Right/Subspace\|Subspace]] and [[Math/Linear Algebra Done Right/Vector Space\|Vector Space]].

>[!info] The span of a list of vectors in $V$ is the smallest subspace containing all the vectors in the list
>Proof:
>Let span$(v_1,\dots,v_n)=S$. The set $S$ is closed under addition and scalar multiplication because $a_1,\dots,a_n$ is in the field $F$. Also, obviously $0\in S$ so $S$ is a subspace of $V$.
>
>Let $W$ be any subspace of $V$ that contains the list of vectors $v_1,\dots,v_n$, Since $W$ is a subspace, it's closed under addition and scalar multiplication. Therefore any linear combination of $v_1,\dots,v_n$ should be in the set $W$. Thus $W\supseteq S$.
>
>$\blacksquare$

Easy for notation, we give the definition below

>[!example] Spans
>If the span of a list of vectors $(v_1,\dots,v_n)$ in $V$ equals $V$, then we say $(v_1,\dots,v_n)$ spans $V$.





