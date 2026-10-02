---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/vector-space/","dg-note-properties":{}}
---

# Vector Space

Before we dive into the definition of Vector Space, we need to know what is addition and scalar multiplication on a set V.

>[!example] Definition of addition and scalar multiplication
>- **Addition**
> An addition on a set V is a function that assigns an element $w\in V$ where $u+v=w$, $\forall u,v \in V$
>- **Scalar  Multiplication**
> A Scalar Multiplication is a function that assigns an element $v\in V$ where $\lambda u=v$, $\forall \lambda \in F$ and $\forall u \in V$


>[!example] Definition of Vector Space
>We define a set V as a **Vector Space over [[Math/Principles of Mathematical Analysis/Fields\|$F$]]** if the following properties hold
>- **Commutativity**
> 	 $\forall u,v \in V$
> 	 $$u+v=v+u$$
>- **Associativity**
> 	 1. $\forall u,v,w \in V$
> 	 $$u+(v+w)=(u+v)+w$$
> 	 2. $\forall a,b\in F$ and $\forall v \in V$
> 	 $$a(bv)=(ab)v$$
>- **Additive Identity**
> 	 There exist a $0\in V$ such that $0+v=v,\ \forall v \in V$
>- **Additive Inverse**
> 	 $\forall v\in V$, there exist a $w\in V$, such that $v+w=0$
>- **Multiplicative Identity**
> 	 $\forall v\in V$
> 	 $$1v=v$$
>- **Distributive Properties**
> 	 1. $\forall a,b\in F$ and $\forall u\in V$
> 	 $$(a+b)u=au+bu$$
> 	 2. $\forall u,v \in V$ and $\forall a \in F$
> 	 $$a(u+v)=au+av$$

## **Examples for Vector Space**

Sets like [[Math/Linear Algebra Done Right/Fⁿ\|Fⁿ]] and [[Math/Linear Algebra Done Right/Fˢ\|Fˢ]] are all vector space. Now we are introducing properties of vector space.

## Properties of Vector Space

>[!info] A vector space has a unique additive identity.
>
>Proof:
>
>Say we have two additive identities $0'$ and $0$
>$$0'=0+0'=0'+0=0$$
>Thus $0'=0$
>
>$\blacksquare$

> [!info] Every element in the vector space has a unique additive inverse.
> 
> Proof:
> 
> For $x\in V$, let $v$ and $v'$ be the two additive inverses of $x$
> $$x+v+v'=(x+v)+v'=v'=(x+v')+v=v$$
>
> Thus, $v=v'$
> 
> $\blacksquare$

 Since every element in the vector space has a unique inverse, we let $\boldsymbol{-v}$ **denote the *additive inverse***  of $v$.

 Now we are ready to prove the intuitive truth.

> [!info] $-v=(-1)v$ 
> 
> Proof:
> 
> $$0=(1+(-1))v=v+(-1)v=0$$
> Because the additive inverse for every element is unique, thus $-v=(-1)v$
> 
  $\blacksquare$









