---
{"dg-publish":true,"permalink":"/math/principles-of-mathematical-analysis/closure/","dg-note-properties":{}}
---

# Closure
> [!example] Definition of closure
> If $X$ is a [[Math/Principles of Mathematical Analysis/Metric Space\|metric space]], if $E\subset X$, and if $E'$ denotes the set of all [[Math/Principles of Mathematical Analysis/Limit Point\|limit points]] of $E$ in $X$, then the closure of $E$ is the set $\overline{E}=E\cup E'$.

> [!info]  Properties of closure
> - (a) $\overline{E}$ is [[Math/Principles of Mathematical Analysis/Closed Set\|closed]]
> - (b) $E=\overline{E}$ if and only if $E$ is closed
> - (c) $\overline{E}\subset F$ for every closed set $F\subset X$ such that $E\subset F$.
>   
>   Proof:
>   
>   For (a), if $p \not\in \overline{E}$, we have $p$ is not a limit point of $E$, now we prove that $p$ is not a limit point of $\overline{E}$. Suppose $p$ is a limit point of $\overline{E}$, we have $N_{r}(p)$ intersects with only $E'$ for some $r>0$. Let $x$ be a point such that $x \in N_{r}(p)\cap E'$ and $0<r_{1}<r-d(x,p)$. Therefore, we have $N_{r_{1}}(x)\subset N_{r}(p)$, and $N_{r_{1}}(x)\cap E\neq \emptyset$. Thus $N_{r}(p)\cap E\neq \emptyset$. There is a contradiction, therefore, $p$ is not a limit point of $\overline{E}$.
>   
>   For (b), if $E$ is closed, by definition, we have $E=\overline{E}$. If $E=\overline{E}$, since $\overline{E}$, is closed, then $E$ is closed
>   
>   For (c), we first prove that if $E\subset F$, we have $E'\subset F'$. For every $p \in E'$, every [[Math/Principles of Mathematical Analysis/Neighborhood\|neighborhood]] intersects with $E$ also intersects with $F$. Therefore, $E' \subset F$. Since $F$ is closed, we have $F\supset F'$. Hence, $F\supset \overline{E}$.
>   
>   $\blacksquare$



