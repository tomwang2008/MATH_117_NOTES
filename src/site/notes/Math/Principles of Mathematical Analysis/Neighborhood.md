---
{"dg-publish":true,"permalink":"/math/principles-of-mathematical-analysis/neighborhood/","dg-note-properties":{}}
---

# Neighborhood
> [!example] Definition of neigborhood
> A neighborhood of $p$ is a [[Math/Principles of Mathematical Analysis/Set\|set]] $N_{r}(p)$ consisting of all $q$ such that [[Math/Principles of Mathematical Analysis/Metric Space\|$d(p,q)<r$]], for some $r>0$. The number $r$ is called the radius of $N_{r}(p)$.


 > [!info]  Every neighborhood is an [[Math/Principles of Mathematical Analysis/Open Set\|open set]].
 > For $p \in E$ and $r>0$, then $N_{r}(p)$ is open
 > 
 > Proof:
 > 
 > For every $q\in N_{r}(p)$, there exists a positive number $h$ such that $d(p,q)=r-h$. Consider the neighborhood $N_{h}(q)$, for $s \in N_{h}(q)$, $d(p,s)\leq d(p,q)+d(q,s)<r-h+h=r$. Therefore, $s \in N_{r}(p)$. 
 > 
 > $\blacksquare$
 
 > [!info]  Every neighborhood of a limit point intersect with the original set
 > If $p$ is a limit point of a set $E$, then every neighborhood of $p$ contains infinitely many points of $E$.
 > 
 > Proof:
 > 
 > Suppose there exists a neighborhood of $p$ such that it only contains finitely many points of $E$, let $r_{1}$ be $\text{min}_{1\leq k\leq n}(d(q_{k},p))$, where $q_{k}$ is any points in the intersection of the neighborhood and $E$. 
 > 
 > Consider the neighborhood $N_{r_{1}}(p)$, if it's not empty, then there exits a $q'$ such that $d(q',p)<r_{1}$, however, since $r_{1}$ is the minimal distance between $p$ and any points in the intersection, $q'$ like that cannot exist. Therefore, every neighborhood of $p$ contains infinitely many points of $E$.
 >  
 > $\blacksquare$
 
 
 
 