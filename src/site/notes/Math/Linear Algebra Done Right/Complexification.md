---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/complexification/","dg-note-properties":{}}
---

# Complexification
> [!example] Definition of complexification of [[Math/Linear Algebra Done Right/Vector Space\|$V$]]
> Suppose $V$ is a real vector space, the complexification of $V$, denoted $V_{\mathbb{C}}$, equals [[Math/Linear Algebra Done Right/Product of Vector Space\|$V\times V$]]. An element of $V_{\mathbb{C}}$ is an ordered pair $(u,v)$, where $u,v\in V$, but we will write this as $u+iv$.
>  
> Addition on $V_{\mathbb{C}}$ is defined by 
> $$
> (u_{1}+iv_{1})+(u_{2}+iv_{2})=(u_{1}+u_{2})+i(v_{1}+v_{2})
> $$
> for $u_{1},v_{1},u_{2},v_{2}\in V$.
> 
> Complex scalar multiplication on $V_{\mathbb{C}}$ is defined by
> $$
> (a+bi)(u+iv)=(au-bv)+i(av+bu)
> $$
> for $a,b\in \mathbb{R}$ and $u,v\in V$.


> [!info]  $V_{\mathbb{C}}$ is a complex vector space
> Suppose $V$ is a real vector space. Then with the definitions of addition and scalar multiplication as above, $V_{\mathbb{C}}$ is a complex vector space.
> 
> Proof:
> 
> This should be trival as $V\times V$ is a vector space.
> 
> $\blacksquare$


> [!info]  Basis of $V$ is basis of $V_{\mathbb{C}}$
> Suppose $V$ is a real vector space.
> 
> (a) If $v_{1},\dots v_{n}$ is a basis of $V$ (as a real vector space), then $v_{1},\dots,v_{n}$ is a basis of $V_{\mathbb{C}}$ (as a complex vector space).
> 
> (b) The dimension of $V_{\mathbb{C}}$ (as a complex vector space) equals the dimension of $V$ (as a real vector space).
> 
> Proof:
> 
> Since $v_{1},\dots,v_{n}$ is a basis of $V$, we have for $u,v\in V$, $u=a_{1}v_{1}+\dots+a_{n}v_{n}$ and $v=b_{1}v_{1}+\dots+b_{n}v_{n}$. Therefore, $u+iv=(a_{1}+ib_{1})v_{1}+\dots+(a_{n}+ib_{n})v_{n}\in \text{span }(v_{1},\dots,v_{n})$. This implies that $v_{1},\dots,v_{n}$ is a basis of $V_{\mathbb{C}}$.
> 
> (b) follows directly from (a)
> 
> $\blacksquare$


> [!example] Definition of complexification of [[Math/Linear Algebra Done Right/Operator\|$T$]]
> Suppose $V$ is a real vector space and $T\in$[[Math/Linear Algebra Done Right/L(V)\|L(V)]]. The complexification of $T$, denoted $T_{\mathbb{C}}$, is the operator $T_{\mathbb{C}}\in \mathcal{L}(V)$ defined by 
> $$
> T_{\mathbb{C}}(u+iv)=Tu+iTv
> $$
> for $u,v\in V$. 

> [!info]  Matrix of $T_{\mathbb{C}}$ equals matrix
> Suppose $V$ is a real vector space with basis $v_1,\dots,v_{n}$ and $T\in \mathcal{L}(V)$. Then $\mathcal{M}(T)=\mathcal{M}(T_{\mathbb{C}})$, where both matrices are with respect to the basis $v_{1},\dots,v_{n}$.
> 
> Proof:
> 
> Suppose the matrix of $T$ is $A$, we have $A(u+iv)=Au+iAv=Tu+iTv=T_{\mathbb{C}}(u+iv)$. Therefore $A$ is a [[Math/Linear Algebra Done Right/Matrix Representation\|matrix representation]] of $T_{\mathbb{C}}$.
> 
> $\blacksquare$



> [!info]  Real eigenvalues of $T_{\mathbb{C}}$
> Suppose $V$ is a real vector sapce, $T\in \mathcal{L}(V)$, and $\lambda \in \mathbb{R}$. Then $\lambda$ is an eigenvalue of $T_{\mathbb{C}}$ if and only if $\lambda$ is an eigenvalue of $T$.
> 
> Proof:
> 
> Because $T$ and $T_{\mathbb{C}}$ have the same [[Math/Linear Algebra Done Right/Minimal Polynomial\|minimal polynomial]], every real eigenvalue of $T$ is an eigenvalue of $T_{\mathbb{C}}$ and vice versa.
> 
> $\blacksquare$

> [!info]  Symmetry $T_{\mathbb{C}}$ between an eigenvalue of $\lambda$ and its complex conjugate $\overline{\lambda}$.
> Suppose $V$ is a real vector space, $T\in \mathcal{L}(V)$, $\lambda \in \mathbb{C}$, $j$ is a nonnegative integer, and $u,v\in V$. Then
> $$
> (T_{\mathbb{C}}-\lambda I)^j(u+iv)=0\text{ if and only if }(T_{\mathbb{C}}-\overline{\lambda}I)^j(u-iv)=0
> $$
> Proof:
> 
>  Proof1: 
>  
>  Suppose $A_{\mathbb{C}}$ is the matrix representation of $T_{\mathbb{C}}$, we have $(A_{\mathbb{C}}-\lambda I)^j(u+iv)=0$. Take the complex conjugate of the equation we have 
>  $$
> \overline{(A_{\mathbb{C}}-\lambda I)^j(u+iv)}=0
> $$
> Which is
> $$
>(A_{\mathbb{C}}-\overline{\lambda}I)^j(u-iv)=0
> $$
>  Threrefore, we get the desired.
>  
>  $\blacksquare$
>  
>  Proof2:
>  
>  We use induction and we induct on $j$. Consider the situation where $j=0$. $u+iv=0\iff u-iv=0$ should be trivial.
>  
>  Assume that by induction the result holds for $j-1$ where $j\geq0$. We want to prove $(T_{\mathbb{C}}-\lambda I)^J(u+iv)=0\iff(T_{\mathbb{C}}-\overline{\lambda}I)^j(u-iv)=0$.  
>  
>  Notice that $(T_{\mathbb{C}}-\lambda I)^j(u+iv)=(T_{\mathbb{C}}-\lambda I)^{j-1}((T-\lambda I)(u+iv))$. Let $\lambda=a+iv$, this can be rewrite as $(T_{\mathbb{C}}-\lambda I)^{j-1}((Tu-au+bv)+i(Tv-av+bu))$. Let $x=Tu-au+bv$ and $y=Tv-av-bu$, this gives us $(T_{\mathbb{C}}-\lambda I)^{j-1}(x+iy)=0\iff(T_{\mathbb{C}}-\overline{\lambda}I)^{j-1}(x-iy)=0$ by our induction hypothesis. Therefore we get the desired result.
>  
>  $\blacksquare$


> [!info]  Nonreal eigenvalue of $T_{\mathbb{C}}$ come in pairs
> Suppose $V$ is a real vector space, $T\in \mathcal{L}(V)$, and $\lambda \in \mathbb{C}$. Then $\lambda$ is an eigenvalue of $T_{\mathbb{C}}$ if and only if $\overline{\lambda}$ is an eigenvalue of $T_{\mathbb{C}}$.
> 
> Proof:
> 
> Take $j=1$ in  the last result, or use the conclution that $T_{\mathbb{C}}$ has the same [[Math/Linear Algebra Done Right/Minimal Polynomial\|minimal polynomial]]. 
> 
> $\blacksquare$


> [!info]  Multiplicity of $\lambda$ equals multiplicity of $\overline{\lambda}$.
> Suppose $V$ is a real vector space, $T\in \mathcal{L}(V)$, and $\lambda \in \mathbb{C}$ is an eigenvalue of $T_{\mathbb{C}}$. Then the multiplicity of $\lambda$ as an [[Math/Linear Algebra Done Right/Eigenvalue\|eigenvalue]] of $T_{\mathbb{C}}$ equals the multiplicity of $\overline{\lambda}$ as an eigenvalue of $T_{\mathbb{C}}$.
> 
> Proof:
> 
> Still we use the conclusion above. It shows that vectors in [[Math/Linear Algebra Done Right/Generalized Eigenspace\|$G(\lambda,T)$]] and $G(\overline{\lambda},T)$ come in pairs.
> 
> $\blacksquare$


