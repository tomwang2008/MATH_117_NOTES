---
{"dg-publish":true,"permalink":"/math/principles-of-mathematical-analysis/open-set/","dg-note-properties":{}}
---

# Open Set
> [!example] Definition of open set
> A [[Math/Principles of Mathematical Analysis/Set\|set]] $E$ is called open if every point of $E$ is an [[Math/Principles of Mathematical Analysis/Interior Point\|interior point]] of $E$.


> [!info]  Duality of Open and Closed Sets
> A set $E$ is open if and only if its [[Math/Principles of Mathematical Analysis/Complement\|complement]] is [[Math/Principles of Mathematical Analysis/Closed Set\|closed]]
> 
> Proof:
> 
> Let $E$ be a open set, if $E^c$ is not closed, there exists a limit point $x$ of $E^c$ where $x \not\in E^c$. Which indicates $x \in E$. Since $x$ is a limit point of $E^c$, every neighborhood of $x$ intersects with $E^c$. This indicates that $x$ is not a [[Math/Principles of Mathematical Analysis/Interior Point\|interior point]] of $E$. This contradicts our condition, so $E^c$ is closed
> 
> Without loss of generality, suppose $E$ is closed.  For every $x \not\in E$, there exists a $r>0$, such that $N_{r}(x)$ does not intersect with $E$, if not, $x$ is a limit point of $E$, which is impossible because $x \not\in E$. Therefore, $E^c$ is open.
> 
>$\blacksquare$
>

 > [!info]  Union (or intersection) of open sets is open
 > -(a) For any collection $\{ G_{\alpha} \}$ of open sets, $\bigcup_{\alpha}G_{\alpha}$ is open
 > -(b) For any finite collection $G_{1},\dots,G_{n}$ of open sets, $\bigcap_{i=1}^nG_{i}$ is open
 > 
 > Proof:
 > 
 > For (a), any $x \in G_{\alpha}$ is a interior point of $G_{\alpha}$, thus, there exists $r>0$, such that $N_{r}(x)\subset G_{\alpha}$. Therefore, $N_{r}(x)\subset \bigcup_{\alpha}G_{\alpha}$. By definition, $\bigcup_{\alpha}G_{\alpha}$ is open
 > 
 > For (b), any $x \in \bigcap_{i=1}^nG_{i}$, $x \in G_{i}$ where $i=1,\dots,n$, thus there exists $r_{i}>0$ such that $N_{r_{i}}(x)\subset G_{i}$. Let $r=\min(r_{1},\dots,r_{n})$. We have $N_{r}(x)\subset \bigcap_{i=1}^cG_{i}$. The existence of $r$ is guarenteed by the finite collection of $G$. 
 > 
 > $\blacksquare$
 
> [!info]  Characterization of Relative Openness
> Suppose $Y \subset X$. A subset $E$ of $Y$ is open relative to $Y$ if and only if $E = Y \cap G$ for some open subset $G$ of $X$.
>
Proof:
>
Suppose $E$ is open relative to $Y$. To each $p \in E$ there is a positive number $r_p$ such that the conditions $d(p, q) < r_p, q \in Y$ imply that $q \in E$. Let $V_p$ be the set of all $q \in X$ such that $d(p, q) < r_p$, and define
>
$$G = \bigcup_{p \in E} V_p.$$
>
Then $G$ is an open subset of $X$
>
Since $p \in V_p$ for all $p \in E$, it is clear that $E \subset G \cap Y$.
>
By our choice of $V_p$, we have $V_p \cap Y \subset E$ for every $p \in E$, so that $G \cap Y \subset E$. Thus $E = G \cap Y$, and one half of the theorem is proved.
>
Conversely, if $G$ is open in $X$ and $E = G \cap Y$, every $p \in E$ has a neighborhood $V_p \subset G$. Then $V_p \cap Y \subset E$, so that $E$ is open relative to $Y$.
>
>$\blacksquare$

 
 
