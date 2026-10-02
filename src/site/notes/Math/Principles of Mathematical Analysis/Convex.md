---
{"dg-publish":true,"permalink":"/math/principles-of-mathematical-analysis/convex/","dg-note-properties":{}}
---

# Convex
> [!example] Definition of convex
> We call a [[Math/Principles of Mathematical Analysis/Set\|set]] $E\subset \mathbb{R}^k$ convec if 
> $$
> \lambda \mathbf{x}+(1-\lambda)\mathbf{y}\in E
> $$
> Whenever $\mathbf{x}\in E$, $\mathbf{y}\in E$, and $0<\lambda<1$.


 > [!info]  [[Math/Principles of Mathematical Analysis/k-cells\|balls]] are convex.
 > If $\lvert \mathbf{y}-\mathbf{x} \rvert<r$, $\lvert \mathbf{z}-\mathbf{x} \rvert<0$, and $0<\lambda<1$, we have $\lvert \lambda \mathbf{y}+(1-\lambda)\mathbf{z}-\mathbf{x} \rvert<r$. For $\mathbf{x}\in \mathbb{R}^k$ and $r>0$
 > 
 > Proof:
 > 
 > $$
> \begin{align}
\lvert \lambda \mathbf{y}+(1-\lambda)\mathbf{z}-\mathbf{x} \rvert & =\lvert \lambda(\mathbf{y}-\mathbf{x})+(1-\lambda)(\mathbf{z}-\mathbf{x}) \rvert \\
 & \leq \lambda \lvert \mathbf{y}-\mathbf{x} \rvert +(1-\lambda)\lvert \mathbf{z}-\mathbf{x} \rvert <\lambda r+(1-\lambda)r \\
 & =r  
\end{align}
> $$
> $\blacksquare$

