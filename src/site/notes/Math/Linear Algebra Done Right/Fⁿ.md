---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/f/","dg-note-properties":{"mathLink":"$\\mathbf{F^n}$"}}
---


# $F^n$


>[!example] Definition for $F^{n}$
>$F^n$ is the set of all lists of length n of elements of $F$
>$$F^n = \set{(x_1, . . . , x_n) : x_j \in F\ \text{for}\  j = 1, . . . , n}$$
>For $(x_1, ... ,x_n)\in F^n$ and $j = 1,...n$ we say that $x_j$ is the $j^{th}$ **coordinate** of $(x_1, ... ,x_n)$


### **Definitions of Operations on $F^n$
#### 1.Addition
$$(x_1,...,x_n)+(y_1,...,y_n)=(x_1+y_1,...,x_n+y_n)$$

#### 2.Scalar Multiplication 
$$ \forall \lambda \in F\ ,\  \lambda (x_1,...,x_n) = (\lambda x_1,...,\lambda x_n)$$
#### 3. 0 
Let 0 denote the list of length n whose coordinates are all 0
$$ 0 = (0,...,0)
$$
### Properties of $F^n$
#### 1. Commutativity of Addition**
For $\forall x,y \in F^n$ 
$$ x+y= y+x$$

#### 2. Additive Identity
 $\exists \mathbf{0} \in F^n$ such that for  $\forall x \in F^n$:
$$x + \mathbf{0} = x$$

#### 3. Additive inverse
For $\forall x\in F^n$ 
$$x+(-x)=0$$
> [!info] Every $\boldsymbol{x}$ has a Additive Inverse
> For every vector $\boldsymbol{x} \in F^n$, there exists a vector $\boldsymbol{y} \in F^n$ such that $\boldsymbol{x} + \boldsymbol{y} = \boldsymbol{0}$.
>
> **Proof:**
> Let $\boldsymbol{x} = (x_1, \dots, x_n) \in F^n$.
> Consider the vector $\boldsymbol{y} = (-x_1, \dots, -x_n)$.
> By the definition of vector addition in $F^n$:
> $$
> \begin{aligned}
> \boldsymbol{x} + \boldsymbol{y} &= (x_1, \dots, x_n) + (-x_1, \dots, -x_n) \\
> &= (x_1 + (-x_1), \dots, x_n + (-x_n)) \\
> &= (0, \dots, 0) \\
> &= \boldsymbol{0}
> \end{aligned}
> $$
> Since $x_i + (-x_i) = 0$ holds in the field $F$, the result is the zero vector in $F^n$.
> Thus, $\boldsymbol{y}$ is the additive inverse of $\boldsymbol{x}$.
> 
> $\blacksquare$

#### 4. Associativity of Addition
For $\forall x,y,z \in F^n$

$$(x+y)+z = x+(y+z)$$

For $\forall a,b \in F$
$$(ab)x = a(bx)$$

#### 5. Multiplicative Identity
For $\forall x \in F^n$

$$1x = x$$

#### 6. Distributivity (Vector Addition)
For $\forall \lambda \in F$ and $\forall x, y\in F^n$ 
$$\lambda(x+y) = \lambda x + \lambda y$$

For $\forall a,b\in F$ and $\forall x\in F^n$ 
$$(a+b)x = ax + bx$$

Thus, the set $F^n$ together with the defined operations of addition and scalar multiplication forms a **Vector Space**.


