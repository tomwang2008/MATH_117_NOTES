---
{"dg-publish":true,"permalink":"/math/linear-algebra-done-right/sign/","dg-note-properties":{}}
---

# Sign
> [!example] Definition of sign 
> The sign of a [[Math/Linear Algebra Done Right/Permutation\|permutation]] $(m_{1},\dots,m_{n})$ is defined to be $1$ if the number of pairs of integers $(j,k)$ with $1\leq j<k\leq n$ such that $j$ appears after $k$ in the list $(m_{1},\dots,m_{n})$ is even and $-1$ if the number of such pairs is odd.|
> 
> In other words, the sign of a permutation equals $1$ if the natural order has been changed an even number of times and equals $-1$ if the natural order has changed an odd number of times.


 > [!info]  Interchanging two entries in a permutation 
 > Interchanging two entries in a permutation multiplies the sign of the permutation by -1.
 > 
 > Proof:
 > 
 > We prove it by induction and we induct by $\text{perm }n$.
 > 
 > Suppose $n=2$, this case is trivial. Therefore, we assume that our conclusion works for every $k$ which $k\leq n$. We now prove that the conclusion works for $n+1$.
 > 
 > For every permutation $(m_{1},\dots,m_{n},m_{n+1})$, by our assumption, interchanging two entries in the first $n$ entries multiplies the sign of the permutation by $-1$. Suppose now we interchange $m_{n+1}$ with $m_{j}$. This process can be seen as change $m_{n+1}$ with $m_{n}$, then change $m_{n}$ with $m_{j}$, then change $m_{j}$ with $m_{n}$. We only need to prove change any two entries that have a distance of $1$ multiplies the sign by $1$. This should be trivial because changing these two entries only adds one or minus one from the total count. Therefore, the overall of the sign change is $(-1)\cdot(-1)\cdot(-1)=-1$. 
 > 
 > $\blacksquare$
 
 