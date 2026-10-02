---
{"dg-publish":true,"permalink":"/math/principles-of-mathematical-analysis/closed-set/","dg-note-properties":{}}
---

# Closed Set
> [!example] Definition of closed set
> A [[Math/Principles of Mathematical Analysis/Set\|set]] is called closed if every [[Math/Principles of Mathematical Analysis/Limit Point\|limit point]] of $E$ is a point of $E$.


 > [!info]  Union (or intersection) of closed sets is a closed set
 > - (a) For any collection $\{ F_{\alpha} \}$ of closed sets, $\bigcap_{\alpha}F_{\alpha}$ is closed.
 > - (b) For any finite collection $F_{1},\dots,F_{n}$ of closed sets, $\bigcup_{i=1}^nF_{i}$ is closed.
 >   
 >   Proof:
 >   
 >   Suppose there is a point $x$ that is a limit point of $\bigcap_{\alpha}F_{\alpha}$ but is not in the set. By definition, we have $N_{r}(p)$ intersects with $\bigcap_{\alpha}F_{\alpha}$ for any $r>0$, which indicates $N_{r}(p)$ intersects with $F_{\alpha}$ for any $\alpha$ and $r>0$. Since $F_{\alpha}$ is closed, we have $p \in F_{\alpha}$. Therefore, $p \in \bigcap_{\alpha}F_{\alpha}$. Contradiction occurs, thus every limit point of $\bigcap_{\alpha}F_{\alpha}$ is included inside.
 >   
 >   Take the complement of $\bigcup_{i=1}^nF_{i}$, we need to prove $\bigcap_{i=1}^nF_{i}^c$ is open, which we've already proved in note [[Math/Principles of Mathematical Analysis/Open Set\|open set]]
 > 
 > $\blacksquare$
 > 

> [!info]  Relation between closed and [[compac\|compact]]
> Closed subsets of compact sets are compact.
> 
> Proof:
> 
> Let $K$ be a closed subset of a compact set $F$ and let ${G_{\alpha}}$ be a [[Math/Principles of Mathematical Analysis/Open Cover\|open cover]] that covers $K$. Consider the [[Math/Principles of Mathematical Analysis/Complement\|complement]] of $K$, as verified, $K^c \cup \{ G_{\alpha} \}$ is a open cover of $F$. Since $F$ is compact, $K^c\cup K_{\alpha_{1}}\cup\dots \cup K_{\alpha_{n}}$ covers $F$ with finitely many choices of $\alpha_{1},\dots,\alpha_{n}$. Therefore, $K\subset K^c\cup G_{\alpha_{1}}\cup\dots\cup G_{\alpha_{n}}$ and since $K\cap K^c=\emptyset$, we have $K\subset G_{\alpha_{1}}\cup\dots\cup G_{\alpha_{n}}$. 
> 
> $\blacksquare$

<span style="color:rgb(0, 176, 80)">Collary</span>: If $F$ is closed and $K$ is compact, then $F\cap K$ is compact.