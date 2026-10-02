---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/dual-map/","dg-note-properties":{}}
---

# Dual Map

>[!example] Dual Map
>If [[Math/Linear Algebra Done Right/Linear Map\|$T$]]$\in$[[Math/Linear Algebra Done Right/L(V,W)\|$\mathcal{L}(V,W)$]], then the dual map $T':W'\to V'$ is defined as:
> $$
> T'(\varphi)=\varphi \circ T
> $$

Just like [[Math/Linear Algebra Done Right/Linear Map\|linear maps]], it has its own algebraic properties.

>[!info] Algebraic properties
>1. $(S+T)'=S'+T'$
>2. $(\lambda T)'=\lambda T'$
>3. $(ST)'=T'S'$
>   
>Proof:
>No need to prove 1 and 2
>For 3:
> $$
> (ST)'\varphi=\varphi \circ ST=(\varphi \circ S)T=S'(\varphi)\circ T=T' S'
> 
> $$
> $\blacksquare$



