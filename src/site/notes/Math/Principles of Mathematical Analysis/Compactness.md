---
{"dg-publish":true,"permalink":"/math/principles-of-mathematical-analysis/compactness/","dg-note-properties":{}}
---

# Compectness
> [!example] Definition of  compact
> A subset $K$ of a [[Math/Principles of Mathematical Analysis/Metric Space\|metric space]] $X$ is said to be compact if every open cover of $K$ contains a finite subcover
> 
> More explicitly. the requirement is that if $\{ G_{\alpha} \}$ is an open cover of $K$, then there are finitely many indices $\alpha_{1},\dots,\alpha_{n}$ such that 
>  $$
> K\subset G_{\alpha_{1}}\cup \dots \cup G_{\alpha_{n}}
> $$



> [!info]  Compatness is relative to the sets
> Suppose $K\subset Y\subset X$. Then $K$ is compact relative to $X$ if and only if $K$ is compact relative to $Y$.
> 
> Proof:
> 
> Suppose $K$ is compact to $X$, let $\{ V_{\alpha} \}$ be a collection of open sets relative to $Y$, such that $K \subset \bigcup_{\alpha}V_{\alpha}$. By the properties of [[Math/Principles of Mathematical Analysis/Open Set\|open set]], there is a collection of open set relative to $X$ such that $G_{\alpha}\cap Y=V_{\alpha}$. Since $K$ is compact relative to $X$, we have 
> $$
> K\subset G_{\alpha_{1}}\cup \dots G_{\alpha_{n}}
> $$
> for finitely many $n$. Since $K\subset Y$, we have 
> $$
> K\subset V_{\alpha_{1}}\cup\dots\cup V_{\alpha_{n}}
> $$
> 
> Now supoose $K$ is compact to $Y$. We define $\{ V_{\alpha} \}$ and $\{ G_{\alpha} \}$ the same. Since we have 
> $$
> K \subset V_{\alpha_{1}}\cup\dots\cup V_{\alpha_{n}}
> $$
> for finitely many $\alpha_{1},\dots,\alpha_{n}$. We get 
> $$
> K \subset (G_{\alpha_{1}}\cap Y)\cup \dots\cup (G_{\alpha_{n}}\cap Y)=(G_{\alpha_{1}}\cup\dots\cup G_{\alpha_{n}})\cap Y
> $$
> Which indicates that 
> $$
> K\subset G_{\alpha_{1}}\cup\dots\cup G_{\alpha_{n}}
> $$
> $\blacksquare$

> [!info]  Properties of compactness
> Compact subsets of [[Math/Principles of Mathematical Analysis/Metric Space\|metric spaces]] are [[Math/Principles of Mathematical Analysis/Closed Set\|closed]].
> 
> Proof:
> 
> Let $K$ be a subset of a metric space $X$. We prove that the [[Math/Principles of Mathematical Analysis/Complement\|complement]] of $K$ is open (or by contradiction, which is left to the readers).
> 
> Suppose $p \in X$ which $p \not\in K$. Let $d(p,q)$ be the distance between $p$ and any point $q \in K$. Let $r$ be a number which is smaller than $\frac{1}{2}d(p,q)$. Consider the [[Math/Principles of Mathematical Analysis/Neighborhood\|neighborhood]] $N_{r}(q)$, trivially, all the neighborhoods cover the set $K$. Since $K$ is open, there are finitely many neighborhoods such that 
> $$
> K \subset N_{r_{1}}(q_{1})\cup \dots\cup N_{r_{n}}(q_{n})
> $$
> Therefore, $N_{r}(p)$, the neighborhood of $p$, where $r=\frac{1}{2}\min_{1\leq i\leq n}(d(q_{i},p))$. The minimum exists because there are only finitely many $q$ and as verified $N_{r}(p)$ does not intersect with $N_{r_{1}}(q_{1})\cup \dots\cup N_{r_{n}}(q_{n})$ therefore $p$ is an [[Math/Principles of Mathematical Analysis/Interior Point\|interior]] point of $K^c$.
> 
> $\blacksquare$

> [!info]  Compactness indicates nonemptyness
> If $\{ K_{\alpha} \}$ is a collection of compact subsets of a metric space $X$ such that the intersection of every finite subcollection of $\{ K_{\alpha} \}$ is nonempty, then $\bigcap K_{\alpha}$ is nonempty.
> 
> Proof:
> 
> We prove by contradiction, suppose $\bigcap K_{\alpha}$ is empty, then for every $K_{\alpha}$ and every element $q$ in $K_{\alpha}$, there exists at least one $K_{\beta}$ such that $p \in K^c_{\beta}$. Therefore, we have $K_{\alpha}\subset \{ K_{\beta}^c \}$. Since $K_{\alpha}$ is compact and $K^c_{\beta}$ is open, we have $K_{\alpha}\subset K^c_{\beta_{1}}\cup\dots\cup K^c_{\beta_{n}}$. For finitely many choices of $K_{\beta_{1}}^\mathbf{c},\dots,K^c_{\beta_{n}}$. So we have $K_{\alpha}\cap K_{\beta_{1}}\cap\dots\cap K_{\beta_{n}}=\emptyset$. Contradiction occurs therefore $\bigcap K_{\alpha}$ is nonempty.
> 
> $\blacksquare$

> [!info]  Compactness ensures a [[Math/Principles of Mathematical Analysis/Limit Point\|limit point]] of subset
> If $E$ is an infinite subset of a compact set $K$, then $E$ has a limit point in $K$.
> 
> Proof:
> 
> Suppose $E$ does not have any limit point in $K$, consider $E'$, we have $E' \cap K=\emptyset$ . Therefore, we have $\overline{E}\cap K=E\neq \emptyset$, since intersection of a closed set and a compact set is compact, $E$ is compact. Therefore, $E$ is closed, which indicates all the limit points of $E$ are included in $E$. We get $E'=\emptyset$, which indicates that $E$ is finite. Contradiction occurs.
> 
>$\blacksquare$



