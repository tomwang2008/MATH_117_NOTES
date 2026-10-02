---
{"dg-publish":true,"permalink":"/math/principles-of-mathematical-analysis/function/","dg-note-properties":{}}
---

# Function
> [!example] Definition of function
> Consider two [[Math/Principles of Mathematical Analysis/Set\|sets]] $A$ and $B$, whose elements may be any objects whatsoever, and suppose that with each element $x$ of $A$ there is associated, in some manner, and element of $B$, which we dentoe by $f(x)$. Then $f$ is said to be a function from $A$ to $B$ (or a mapping of $A$ into $b$). The set $A$ is called the domain of $f$ (we also say $f$ is defined on $A$), and the elements $f(x)$ are called the values of $f$. The set of all values of $f$ is called the range of $f$.
> 

> [!example] Definition of image
> Let $A$ and $B$ be two sets and let $f$ be a mapping of $A$ into $B$. If $E\subset A$, $f(E)$ is defined to be the set of all elements $f(x)$, for $x \in E$. We call $f(E)$ the image of $E$ under $f$. In this notation, $f(A)$ is the range of $f$. It is clear that $f(A)\subset B$, we say that $f$ maps $A$ onto $B$.  If $f(A)=B$, we say that $f$ maps $A$ onto $B$.
> 
> If $E\subset B$, $f^{-1}(E)$ denotes the set of all $x \in A$  such that $f(x)\in E$. We call $f^{-1}(E)$ the inverse image of $E$ under $f$. If $y\in B$, $f^{-1}(y)$ is the set of all $x \in A$ such that $f(x)=y$. If, for each $y\in B$, $f^{-1}(y)$ consists of at most one element of $A$, then $f$ is said to be a one-toone mapping of $A$ into $B$. This may also be expressed as follows: $f$ is a 1-1 mapping of $A$ into $B$ provided that $f(x_{1})\neq f(x_{2})$ whenever $x_{1}\neq x_{2}$, $x_{1}\in A,x_{2}\in A$.

Notice the similarities between 1-1 mapping and [[Math/Linear Algebra Done Right/Injectivity\|injectivity]].

