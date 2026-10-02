---
{"dg-publish":true,"permalink":"/math/principles-of-mathematical-analysis/upper-bound/","dg-note-properties":{}}
---

# Upper Bound
> [!example] Definition of upper bound
> Suppose $S$ is an ordered set, and $E\subset S$. If there exists a $\beta \in S$ such that $x\leq \beta$ for every $x \in E$, we say that $E$ is bounded above, and call $\beta$ an upper bound of $E$.
> 

 By the same way, we can also define lower bound.

> [!example] Definition of least upper bound
> Suppose $S$ is an ordered set, $E\subset S$, and $E$ is bounded above. Suppose there exists an $\alpha \in S$ with the following properties:
> 
> (i) $\alpha$ is an upper bound of $E$
> (ii) If $\gamma<\alpha$ then $\gamma$ is not an upper bound of $E$.
> 
> Then $\alpha$ is called the least upper bound of $E$ or the supremum of $E$, and we write
> $$
> \alpha = \text{sup }E
> $$

By the same way we define the greatest lower bound of the infimum as $\text{inf }E$

> [!example] Definition of least-upper-bound property
> An [[Math/Principles of Mathematical Analysis/Set\|ordered set]] $S$ is said to have the least-upper-bound property if the following is true:
> If $E\subset S$, $E$ is not empty, and $E$ is bounded above, then $\text{sup }E$ exists in $S$.

 
> [!info]  The greatest lower bound of one set is the lowest upper bound of another set
> Suppose $S$ is an ordered set with the least-upper-bound property, $B\subset S$, $B$ is not empty, and $B$ is bounded below. Let $L$ be the set of all lower bounds of $B$. Then
> $$
> \alpha = \text{sup }L
> $$
> exists in $S$, and $\alpha=\text{inf } B$.
> 
> Proof:
>  Obviously $\alpha$ is a lower bound of $B$, we now prove that $\alpha$ is the greatest lower bound. Suppose we have a lower bound of $B$, let it be $\beta$ and $\beta>\alpha$. Because $\beta$ is a lower bound of $B$, we have $\beta \in L$, this indicates that $\beta\leq \alpha$, which contradicts our assuption. Thus, $\alpha=\text{inf }B$.
>
>$\blacksquare$

> [!info]  Supremum and Closure
> Let $E$ be a nonempty set of real numbers which is bounded above. Let $y=\text{sup } E$. Then [[Math/Principles of Mathematical Analysis/Closure\|$y \in \overline{E}$]], hence $y \in E$ if $E$ is [[Math/Principles of Mathematical Analysis/Closed Set\|closed]].
> 
>Proof:
>
>If $y$ is not a limit point of $E$, There exists $r$ such that $N_{r}(y)$ does not intersects with $E$. However, by definition, we have $p \in E$ if $p<y$. Let $p   \in N_{r}(p)$ such that $p<y$, we get $p \not\in E$. Thus, $y$ is not a supremum of $E$. There is a contradiction therefore, $y$ is a limit point of $E$.
>
>$\blacksquare$

