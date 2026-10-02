---
{"dg-publish":true,"permalink":"/math/principles-of-mathematical-analysis/fields/","dg-note-properties":{}}
---

# Fields
> [!example] Definition of fields
> A field is a [[Math/Principles of Mathematical Analysis/Set\|set]] $\mathbf{F}$ with two operations, called addition and multiplication, which satisfy the following so=called "field axioms"
> (A) Axioms for addition
> &emsp;&emsp; A1 If $x \in \mathbf{F}$ and $y \in \mathbf{F}$, then their sum $x+y$ is in $\mathbf{F}$.
> &emsp;&emsp;A2 Addition is commutative: $x+y=y+x$ for all $x,y\in \mathbf{F}$.
> &emsp;&emsp;A3 Addition is asociative: $(x+y)+z=z+(y+z)$ for all $x,y,z\in \mathbf{F}$.
> &emsp;&emsp;A4 $\mathbf{F}$ contains an element $0$ such that $0+x=x$ for every $x \in \mathbf{F}$.
> &emsp;&emsp;A5 To every $x \in \mathbf{F}$ corresponds an element $-x \in \mathbf{F}$ such that 
> $$
> x+(-x)=0
> $$
> (M) Axioms for multiplication
> &emsp;&emsp; M1 If $x \in \mathbf{F}$ and $y \in \mathbf{F}$, then their product $xy$ is in $\mathbf{F}$.
> &emsp;&emsp; M2 Multiplication is commutative: $xy=yx$ for all $x,y\in \mathbf{F}$.
> &emsp;&emsp; M3 Multiplication is asociative: $x(yz)=(xy)z$ for all $x,y,z\in \mathbf{F}$.
> &emsp;&emsp; M4 $\mathbf{F}$ contains an element $1\neq0$ such that $1x=x$ for every $x \in \mathbf{F}$.
> &emsp;&emsp; M5 If $x \in \mathbf{F}$ and $x\neq 0$ then there exists an element $1/x \in \mathbf{F}$ such that
> $$
> x\cdot(1/x)=1
> $$
> (D) The distributive law
> $$
> x(y+z)=xy+xz
> $$
> holds for all $x,y,z \in \mathbf{F}$.

> [!info]  Proposition of the axioms for addition
> (a) If $x+y=x+z$ then $y=z$.
> (b) If $x+y=x$ then $y=0$.
> (c) If $x+y=0$ then $y=-x$.
> (d)  $-(-x)=x$.
> 
> Proof:
> 
> For (a), $(-x)+x+y=(-x)+x+z$ leads to $y=z$.
> For (b), use conclusion (a) and subsitute $z=0$, we get $y=0$.
> For (c), add $(-x)$ on both sides and we get the desired
> For(d), Since we have $(-x)+(-(-x))=0$, add $x$ on both sides, we have $-(-x)=x$,
> 
> $\blacksquare$

> [!info]  Proposition of the axioms for multiplication
> (a) If $x\neq 0$ and $xy=xz$ then $y=z$.
> (b) If $x\neq0$ and $xy=x$ then $y=1$.
> (c) If $x\neq 0$ and $xy=1$ then $y=1/x$.
> (d) If $x\neq 0$ then $1/(1/x)=x$.
> 
> Proof:
> 
> The prove is so similar to addition, we omit it.


 > [!info]  Proposition of field axioms
 > (a) $0x = 0$.
 > (b) If $x\neq 0$ and $y\neq 0$ then $xy\neq 0$.
 > (c) $(-x)y=-(xy)=x(-y)$.
 > (d) $(-x)(-y)=xy$.
 > 
 > Proof:
 > 
 > For (a), $(0+0)x=0x$, therefore, by our proposition of axoms for addition (b), $0x=0$.
 > 
 > For (b), if $xy=0$, we have $xy=0=0y$, by the conclusion above, we have $y=0$, this contradicts the assumption that $x,y\neq 0$.
 > 
 > For (c), we only need to prove that $(-x)y=-(xy)$. $xy+(-x)y=(x+(-x))y=0=xy+(-xy)$, therefore, by the proposition of the addition axiom (a), we have $(-x)y=-xy$.
 > 
 > For(d), $(-x)(-y)+(-x)y=(-x)(-y+y)=0$, by the proposision above, we have $(-x)(-y)=-(-xy)=xy$.
 > 
 > $\blacksquare$
 
 
> [!example] Definition of [[Math/Principles of Mathematical Analysis/Order\|ordered]] field
> An ordered field is a field $\mathbf{F}$ which is alos an ordered [[Math/Principles of Mathematical Analysis/Set\|set]], such that 
> &emsp;&emsp; (i) $x+y<x+z$ if $x,y,z \in \mathbf{F}$ and $y<z$
> &emsp;&emsp; (ii) $xy>0$ if $x \in \mathbf{F}$, $y\in \mathbf{F}$, $x>0$, and $y>0$.

If $x>0$, we call $x$ positive; if $x<0$, $x$ is negative.

> [!info]  Proposition of ordered field
> 
> &emsp; (a) If $x>0$ then $-x<0$, and vice versa
> &emsp;&emsp; (b) If $x>0$ and $y<x$ then $xy<xz$
> &emsp;&emsp; (c) If $x<0$ and $y<z$ then $xy>xz$
> &emsp;&emsp; (d) If $x\neq 0$ then $x^2>0$. In particular, $1>0$
> &emsp;&emsp; (e) If $0<x<y$ then $0<1/y<1/x$.
> 
> Proof:
> 
> For (a), if $x>0$, then $x>x+(-x)$, by definition, $0>-x$.
> 
> For (b), we have $y<z$, which is $y+(-y)<z+(-y)$, therefore, $0<z-y$. By definition, we have $x(z-y)>0$, which by distributive law, is $xy-xz>0$. Thus, we get the desireed.
> 
> For (c), do the same process above, but subsitute $x$ with $-x$.
> 
> For (d), if $x>0$, then trivially $x^2>0$. If $x<0$, we have $(-x)(-x)=x^2$, since $-x>0$, we have $(-x)(-x)=x^2>0$.
> 
> For (e), we first prove if $x>0$, then $1/x>0$. Suppose $1/x<0$, we still have $x\cdot 1/x=1>0$. Because $1/x<0$, we have $-1/x>0$, therefore, both $x\cdot 1/x$ and $x \cdot(-1/x)$ are postitive, which contradicts our first proposision. Thus, if $x>0$, we have $1/x>0$. If $0<x<y$, we have $x\cdot1/x<y\cdot 1/x$, which is $1=y\cdot 1/y<y\cdot 1/x$. By our proposition, we have $0<1/y<1/x$.
> 
> $\blacksquare$


> [!info]  The real field has the [[Math/Principles of Mathematical Analysis/Upper Bound\|least-upper-bound property]]
> There exists an ordered field $\mathbb{R}$ which has the least-upper-bound property. Moreover, $\mathbb{R}$ contains $\mathbb{Q}$ as a subfield.
> 
> Proof:
> 
> Step 1: Construction of $\mathbb{R}$ (Dedekind Cuts) Let a cut be defined as a subset $\alpha \subset \mathbb{Q}$ that satisfies the following three properties:$\alpha$ is not empty, and $\alpha \neq \mathbb{Q}$.If $p \in \alpha$, $q \in \mathbb{Q}$, and $q < p$, then $q \in \alpha$.If $p \in \alpha$, then $p < r$ for some $r \in \alpha$.Let $\mathbb{R}$ be the set of all such cuts $\alpha$.
> 
> Step 2: Defining the Order For $\alpha, \beta \in \mathbb{R}$, we define $\alpha < \beta$ to mean that $\alpha$ is a proper subset of $\beta$ (that is, $\alpha \subset \beta$ and $\alpha \neq \beta$).It is straightforward to verify that this relation satisfies the law of trichotomy (for any $\alpha, \beta \in \mathbb{R}$, exactly one of $\alpha < \beta$, $\alpha = \beta$, or $\beta < \alpha$ holds) and transitivity. Thus, $\mathbb{R}$ is an ordered set.
> 
> Step 3: Proof of the Least-Upper-Bound Property Suppose $A$ is a nonempty subset of $\mathbb{R}$, and $A$ is bounded above. We must prove that $\sup A$ exists in $\mathbb{R}$.Let $\beta \in \mathbb{R}$ be an upper bound for $A$. Define $\gamma$ to be the union of all $\alpha \in A$:$$\gamma = \bigcup_{\alpha \in A} \alpha$$First, we must prove that $\gamma \in \mathbb{R}$ by verifying the three properties of a cut:Since $A$ is nonempty, there exists some $\alpha_0 \in A$. Since $\alpha_0$ is nonempty, $\gamma$ is not empty. Furthermore, since $\beta$ is an upper bound for $A$, $\alpha \subset \beta$ for all $\alpha \in A$. Therefore, $\gamma \subset \beta$. Since $\beta \neq \mathbb{Q}$, it follows that $\gamma \neq \mathbb{Q}$.Suppose $p \in \gamma$ and $q < p$. Because $p \in \gamma$, there exists some $\alpha \in A$ such that $p \in \alpha$. Since $\alpha$ is a cut, the condition $q < p$ implies $q \in \alpha$. Thus, $q \in \gamma$.Suppose $p \in \gamma$. Again, $p \in \alpha$ for some $\alpha \in A$. Since $\alpha$ is a cut, there exists an $r \in \alpha$ such that $p < r$. Since $r \in \alpha$, we have $r \in \gamma$, satisfying the third property.Therefore, $\gamma$ is a valid cut, meaning $\gamma \in \mathbb{R}$.Next, we prove that $\gamma = \sup A$:By the definition of $\gamma$ as a union, it is evident that $\alpha \subset \gamma$ (i.e., $\alpha \le \gamma$) for every $\alpha \in A$. Thus, $\gamma$ is an upper bound for $A$.To show it is the least upper bound, suppose $\delta < \gamma$. This implies there exists a rational number $p$ such that $p \in \gamma$ but $p \notin \delta$. Since $p \in \gamma$, there must exist some $\alpha \in A$ such that $p \in \alpha$. Because $p \notin \delta$ and cuts are closed downwards, it is impossible for $\alpha$ to be a subset of $\delta$. Therefore, $\alpha \not\le \delta$, which means $\delta$ is not an upper bound for $A$.Since no $\delta < \gamma$ can be an upper bound, $\gamma$ is the least upper bound. Hence, $\gamma = \sup A$.
> 
> Step 4: Field Operations (Outline)We define the zero element as $0^* = \{p \in \mathbb{Q} \mid p < 0\}$.Addition is defined element-wise:$$\alpha + \beta = \{p + q \mid p \in \alpha, q \in \beta\}$$It can be formally verified that $\alpha + \beta$ is a cut, and that addition satisfies commutativity, associativity, and the existence of inverses (where $-\alpha$ requires a careful definition avoiding the boundary element). Multiplication is defined similarly for positive cuts and extended to negative cuts via absolute values. With these operations rigorously verified, $\mathbb{R}$ forms an ordered field.Step 5: Embedding $\mathbb{Q}$ into $\mathbb{R}$For each rational number $x \in \mathbb{Q}$, we associate a cut $x^* \in \mathbb{R}$ defined by:$$x^* = \{p \in \mathbb{Q} \mid p < x\}$$It is straightforward to check that the mapping $x \mapsto x^*$ preserves addition ($x^* + y^* = (x+y)^*$), multiplication ($x^* y^* = (xy)^*$), and order ($x < y \iff x^* < y^*$).Therefore, the ordered field $\mathbb{Q}$ is isomorphic to the subfield of $\mathbb{R}$ consisting of all rational cuts $x^*$. We can identify $x$ with $x^*$, and conclude that $\mathbb{Q}$ is a subfield of $\mathbb{R}$.
> 
> $\blacksquare$


> [!info]  Archimedean property and the density of rational numbers
> (a) If $x \in \mathbb{R}$, $y\in \mathbb{R}$, and $x>0$, then there is a positiive integer $n$ such that 
> $$
> nx>y
> $$
> (b) If $x \in \mathbb{R}$, $y\in \mathbb{R}$, and $x<y$, then there exists a $p \in \mathbb{Q}$ such that $x<p<y$.
> 
> Proof:
> 
> For (a), suppose there does not exists such positive integer $n$, we have $nx\leq y$, for any posiitve integer $n$ and some $x,y\in \mathbf{F}$. Consider the set $S=\{ nx: n\in \mathbb{Z}_{+} \}$. The set has a upper bound by our assumption, therefore, it has a lowest upper bound. Let it be $y_{1}$, we have $nx\leq y_{1}$ for every $n$ and $mx\geq y_{1}-x$ for some positive integer $m$. Therefore, we have $(m+1)x\geq y_{1}$. This contradicts that $y_{1}$ is an upper bound of $S$. Thus, for every $x,y\in \mathbf{F}$, there exists a positive integer $n$, such that $nx>y$.
> 
> For (b), we have $y-x>0$, therefore, by (a), there exists a positive integer $n$, such that $n(y-x)>1$, which leads to $ny>m>nx$. Thus, we have $y>m/n>x$ and $m/n$ is a rational number.
> 
> $\blacksquare$


> [!info]  Existence of roots
> For every real $x>0$ and every integer $n>0$ there is one and only one positive real $y$ such that $y^n=x$.
> 
> This number $y$ is written $\sqrt[n]{x}$ or $x^{1/n}$.
> 
> Proof:
> 
>  That there is at most one such $y$ is clear, since $0<y_1<y_2$ implies $y_1^n<y_2^n$.
>
Let $E$ be the set consisting of all positive real numbers $t$ such that $t^n<x$.
>
If $t=x/(1+x)$ then $0 \le t < 1$. Hence $t^n \le t < x$. Thus $t \in E$, and $E$ is not empty.
>
If $t>1+x$ then $t^n \ge t > x$, so that $t \notin E$. Thus $1+x$ is an upper bound of $E$.
>
Hence Theorem 1.19 implies the existence of
>
$$y=\sup E.$$
>
To prove that $y^n=x$ we will show that each of the inequalities $y^n<x$ and $y^n>x$ leads to a contradiction.
>
The identity $b^n-a^n=(b-a)(b^{n-1}+b^{n-2}a+\dots+a^{n-1})$ yields the inequality
>
$$b^n-a^n<(b-a)nb^{n-1}$$
>
when $0<a<b$.
>
Assume $y^n<x$. Choose $h$ so that $0<h<1$ and
>
$$h<\frac{x-y^n}{n(y+1)^{n-1}}.$$
>
Put $a=y, b=y+h$. Then
>
$$(y+h)^n-y^n<hn(y+h)^{n-1}<hn(y+1)^{n-1}<x-y^n.$$
>
Thus $(y+h)^n<x$, and $y+h \in E$. Since $y+h>y$, this contradicts the fact that $y$ is an upper bound of $E$.
>
Assume $y^n>x$. Put
>
$$k=\frac{y^n-x}{ny^{n-1}}.$$
>
Then $0<k<y$. If $t \ge y-k$, we conclude that
>
$$y^n-t^n \le y^n-(y-k)^n<kny^{n-1}=y^n-x.$$
>
Thus $t^n>x$, and $t \notin E$. It follows that $y-k$ is an upper bound of $E$.
>
But $y-k<y$, which contradicts the fact that $y$ is the _least_ upper bound of $E$.
>
Hence $y^n=x$, and the proof is complete.
>
>$\blacksquare$



