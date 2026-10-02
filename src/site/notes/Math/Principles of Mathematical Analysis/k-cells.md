---
{"dg-publish":true,"permalink":"/math/principles-of-mathematical-analysis/k-cells/","dg-note-properties":{}}
---

# k-cells
> [!example] Definition of k-cell
> If $a_{i}<b_{i}$ for $i=1,\dots,k$ the set of all points $\mathbf{x}=(x_{1},\dots,x_{k})$ in [[Math/Principles of Mathematical Analysis/Euclidean Space\|$\mathbb{R}^k$]] whose coordinates satisfy the inequalities $a_{i}<x_{I}<b_{i}$ is called a k-cell. Thus a 1-cell is an interval, a 2-cell is called a rectangle.

We usually write $[a,b]$ to indicate the interval wherer $a\leq x\leq b$ and $(a,b)$ to indicate the interval where $a<x<b$. 

Occasionally we shall also encounter "half-open intervals" $[a,b)$ and $(a,b]$: the first consists of all $x$ such that $a\leq x<b$, the second of all $x$ such that $a<x\leq b$.

If $\mathbf{x}\in \mathbb{R}^k$ and $r>0$, the open (or closed) ball $B$ with center at $\mathbf{x}$ and radius $r$ is defined to be the set of all $\mathbf{y}\in \mathbb{R}^k$ such that $\lvert \mathbf{y}-\mathbf{x} \rvert<r$ (or $\lvert \mathbf{y}-\mathbf{x} \rvert\leq r$).

> [!info]  Nonemptiness of infinite series of intervals
> 
> If $\{ I_{n} \}$ is a sequence of intervals in $\mathbb{R}^1$ such that $I_{n}\supset I_{n+1}$, then $\bigcap_{1}^{\infty} I_{n}$ is not empty.
> 
> Proof:
> 
> We denote that $I_{j}$ to be $[b_{j},a_{j}]$, by the conditions, we have $b_{j}<b_{j+1}$ and $a_{j}>a_{j+1}$.Trivially, $I_{n}$ has a upper bound for any finite number of $n$. 
> 
> Since every $I_{n}$ is closed, $\bigcap_{1}^\infty I_{n}$ is closed, and by the least upper bound property, $\bigcap_{1}^\infty I_{n}$ has a supremum. If a set is closed and have a supremum, it contains the supremum in the set. Therefore, $\bigcap_{1}^\infty I_{n}$ is not empty. 
> 
> $\blacksquare$

We could also expand this theorem to any k-cell where $k$ is any positive integer. Notice that we also have the theorem which claims that every $\bigcap_{1}^\infty K_{n}$ is non-empty, where $K_{n}$ is a compact subset and $K_{n}\subset K_{n+1}$. Which drives people to the idea that if every k-cell is compact?

> [!info]  Compactness of k-cells
> Every k-cell is compact.
> 
> Proof:
> 
> By the way of induction, we start at the case of $k=1$. We now prove that any closed interval is compact.

 