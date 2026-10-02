---
{"dg-publish":true,"permalink":"/math/principles-of-mathematical-analysis/complement/","dg-note-properties":{}}
---

# Complement
> [!example] Definition of complement
> The complement of $E$ (denoted by $E^c$) is the [[Math/Principles of Mathematical Analysis/Set\|set]] of all points $p \in X$ such that $p \not\in E$.


> [!info]  Generalized De Morgan's Laws
> Let $\{ E_{\alpha} \}$ be a {finite or infinite} collection of sets $E_{\alpha}$. Then
> $$
> \left( \bigcup_{\alpha}E_{\alpha} \right)^c=\bigcap_{\alpha}E_{\alpha}^c
> $$
> 
> Proof:
> 
> Let the LHS be $S$ and the RHS be $S_{1}$. We want to prove that $S=S_{1}$. For $x \in S$, we have 
> $$
> x\not\in \bigcup_{\alpha}E_{\alpha}
> $$
> Therefore, we have $x \in E_{\alpha}^c$ for every $\alpha$, which $x \in \bigcap_{\alpha}E_{\alpha}^c$.
> 
> For $x \in S_{1}$, we have 
> $$
> x \in E_{\alpha}^c
> $$
> For every $\alpha$. Therefore, $x \not\in \bigcup_{\alpha}E_{\alpha}$, which $x \in\left( \bigcup_{\alpha}E_{\alpha} \right)^c$.
> 
>By proving $S_{1}\subset S$ and $S\subset S_{1}$, we have proved $S_{1}=S$.
>
>$\blacksquare$
>
