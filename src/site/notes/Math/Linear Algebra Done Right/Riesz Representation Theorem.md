---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/riesz-representation-theorem/","dg-note-properties":{}}
---

# Riesz Representation Theorem
> [!info]  Riesz Representation Theorem
> Suppose [[Math/Linear Algebra Done Right/Vector Space\|$V$]] is [[Math/Linear Algebra Done Right/Finite-dimensional Vector Space\|finite-dimensional]] and $\varphi$ is a [[Math/Linear Algebra Done Right/Linear Functional\|linear functional]] on $V$. Then there is a unique vector $u\in V$ such that
> $$
> \varphi(v)=\langle v,u \rangle
> $$
> for every $v\in V$.
> 
> Proof:
> 
> Let $e_{1},\dots,e_{n}$ be an othornormal basis of $V$ and $u=a_{1}e_{1}+\dots+a_{n}e_{n}$. We want to find out the coeiffients $a_{j}$. Let $v=e_{1},\dots,e_{n}$ and we get $\varphi(e_{j})=\langle e_{j},a_{j}e_{j} \rangle$ where $j=1,\dots,n$. Thus, 
> $$u=\overline{\varphi(e_{1})}e_{1}+\dots+\overline{\varphi (e_{n})}e_{n}$$
> Now we prove that $u$ is unique, we prove by contradiction. If $u_{1}\neq u_{2}$ and $\varphi(v)=\langle v,u_{1} \rangle=\langle v,u_{2} \rangle$. where $v\neq_{0}$. $\langle v,u_{1}-u_{2} \rangle=0$. Thus, $u_{1}-u_{2}=0$, which is $u_{1}=u_{2}$. This contradicts our assumption. Therefore, $u$ is unique.
> 
> $\blacksquare$


