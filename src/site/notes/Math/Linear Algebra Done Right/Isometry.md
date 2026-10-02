---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/isometry/","dg-note-properties":{}}
---

# Isometry
> [!example] Definition of isometry
> An [[Math/Linear Algebra Done Right/Operator\|operator]] $S\in$[[Math/Linear Algebra Done Right/L(V)\|L(V)]] is called an isometry if 
> $$
> \lVert Sv \rVert=\lVert v \rVert  
> $$
> for all $v\in$[[Math/Linear Algebra Done Right/Vector Space\|$V$]].
> In other words, an operator is an isometry if it preserves [[Math/Linear Algebra Done Right/Norm\|norms]].

> [!info] Characterization of isometries
> 
Suppose $S \in \mathcal{L}(V)$. Then the following are equivalent:
>
(a) $S$ is an isometry;
>
(b) $\langle Su, Sv \rangle = \langle u, v \rangle$ for all $u, v \in V$;
>
(c) $Se_1, \dots, Se_n$ is orthonormal for every orthonormal list of vectors $e_1, \dots, e_n$ in $V$;
>
(d) there exists an orthonormal basis $e_1, \dots, e_n$ of $V$ such that $Se_1, \dots, Se_n$ is orthonormal;
>
(e) $S^*S = I$;
>
(f) $SS^* = I$;
>
(g) $S^*$ is an isometry;
>
(h) $S$ is invertible and $S^{-1} = S^*$.
>
>Proof:
>
>b,c,...,h should be obiously equivalent, we now proof (a) and (d) are equivalent.
>
>Suppose (d) holds, Then $\forall v\in V$, $v=a_{1}e_{1}+\dots+a_{n}e_{n}$ and $Sv=a_{1}Se_{1}+\dots+a_{n}S_{n}$. We have
> $$
> \begin{align}
\lVert Sv \rVert^2 & =\lVert a_{1}Se_{1}+\dots+a_{n}Se_{n} \rVert^2 \\
 & =\lVert a_{1}Se_{1} \rVert^2+\dots+\lVert a_{n}Se_{n} \rVert^2 \\
 & =\lVert a_{1} \rVert^2+\dots+\lVert a_{n} \rVert^2 \\
 & =\lVert v \rVert^2
\end{align}
> $$
> Which leads to $S$ is an isometry.
> 
> Suppose (a) holds. Let $e_{1},\dots,e_{n}$ is an orthonormal basis of $V$. We have 
> $$
> \lVert S(e_{i}+e_{j}) \rVert^2=\lVert Se_{i}+Se_{j} \rVert^2=\lVert e_{i}+e_{j} \rVert^2=\lVert Se_{i} \rVert^2+\lVert Se_{j} \rVert^2
> $$
> Which implies that $\langle Se_{i},Se_{j} \rangle+\langle Se_{j},Se_{i} \rangle=0=\mathrm{Re}(\langle Se_{j},Se_{i} \rangle)=0$.
> 
> Now we check $S(e_{i}+ie_{j})$,
> $$
> \lVert S(e_{i}+ie_{j}) \rVert ^2=\lVert e_{i}+ie_{j} \rVert ^2=\lVert e_{i}^2 \rVert -\lVert e_{j} \rVert ^2=\lVert Se_{i} \rVert ^2-\lVert Se_{j} \rVert
{ #2}

> $$
> Which impies that $\langle Se_{i},Se_{j} \rangle-\langle Se_{j},Se_{i} \rangle=\mathrm{Im}(\langle Se_{j},Se_{i} \rangle)=0$
> 
> Put the two conclustions together we get $\langle Se_{j},Se_{i} \rangle=0$.
> 
> $\blacksquare$


> [!info]  Description of isonmetries when $\mathbf{F}=\mathbb{R}$
> Suppose $V$ is a real inner product space and $S\in \mathcal{L}(V)$. Then the following are equivalent.
> 
> (a) $S$ is an isometry
> 
> (b) There is an orthonormal basis of $V$ with respect to which $S$ has a block diagonal matrix such that each block on the diagonal is a 1-by-1 matrix containing 1 or -1 or is a 2-by-2 matrix of the form
> $$
> \begin{pmatrix}
\cos \theta & -\sin \theta \\
\sin \theta & \cos \theta
\end{pmatrix}
> $$
> with $\theta \in(0,\pi)$.
> 
> Proof:
> 
> See the proof we did in the note [[Math/Linear Algebra Done Right/Normal\|normal operators]],  because every isometry is normal, it generally follows the proof. Since every isomertry restricted on a smaller invariant subspace is also isometric, all the 1-by-1 matrices contain only 1 or -1 and all the 2-by-2 matrices of the form 
> $$
> \begin{pmatrix}a & -b \\ b & a\end{pmatrix}
> $$
  satisfy $a^2+b^2=1$. Therefore, let $\cos \theta=a$ and $\sin \theta=b$, we get the matrix form of $\begin{pmatrix}\cos \theta & -\sin \theta \\ \sin \theta & \cos \theta  \end{pmatrix}$.
>
>$\blacksquare$


  
  
 
 

