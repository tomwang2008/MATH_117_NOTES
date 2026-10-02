---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/f/","dg-note-properties":{"mathLink":"$\\mathbf{F^S}$"}}
---


# $F^S$

The notion $F^S$ denotes the set of functions from S to F. The addition and scalar multiplication is defined as followed.

> [!example] Definition of addition and scalar multiplication for $F^S$
> - **Addition**
>   $\forall f,g \in F^S$ the sum $f+g$ is defined by
>   $$(f+g)(x)=f(x)+g(x)$$
>   for all $x\in S$
> - Scalar multiplication 
>   $\forall f\in  F^S$ and $\forall \lambda \in F$, the product $\lambda f$ is defined by
>   $$(\lambda f)(x)=\lambda f(x)$$
>   for all $x\in S$

## $F^S$ is a vector space

The 0 identity is defined by
$$0(x)=0$$
The additive inverse of $f$ is defined by
$$(-f)(x)=-f(x)$$
> [!abstract] Notice
> The existence of the additive inverse function $-f$ relies entirely on the additive inverse in the field $F$. We constitute the function $-f$ point-by-point:
> $$
> \underbrace{(-f)}_{\text{New Function}} (x) = \underbrace{-}_{\text{Scalar Inverse}} \underbrace{(f(x))}_{\text{Scalar Value}}
> $$



The properties of a vector space hold in $F^S$ and it's easy to verify.