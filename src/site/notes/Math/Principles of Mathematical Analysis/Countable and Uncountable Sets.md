---
{"dg-publish":true,"permalink":"/math/principles-of-mathematical-analysis/countable-and-uncountable-sets/","dg-note-properties":{}}
---

# Countable and Uncountable Sets

> [!example] Definition of finite, infinite, coutable, uncountable
> For any positive integer $n$, let $J_{n}$ be the set whose elements are the integers $1,2,\dots,n$: let $J$ be the set consisiting of all positive integers. For any set $A$, we say
> 
> - (a) $A$ is finite if [[Math/Principles of Mathematical Analysis/Correspondence\|$A\sim J_{n}$]] for some $n$ (the empty set is also considered to be finite)
> - (b) $A$ is infinite if $A$ is not finite
> - (c) $A$ is coutable if $A\sim J$.
> - (d) $A$ is uncountable if $A$ is neither finite nor countable.
> - (e) $A$ is at most countable if $A$ is finite or countable.

Countable sets are sometimes called enumerable or demumerable.


> [!info]  Every infinite subset of a countable set $A$ is countable
> 
> Proof:
> 
> Suppose $E\subset A$ and $E$ is infinite. Since $A$ is countable, there exits a 1-1 mapping such that $f(A)=J$. Therefore, we obtain a sequence $\{ x_{n} \}$, we construct a new sequence $\{ n_{k} \}$ as follows: Let $n_{1}$ be the smallest positiive integer such that $x_{n_{1}}\in E$, continuing this fasion, let $n_{k}$ be the $k^{th}$ smallest positive integer such that $x_{n_{k}}\in E$. Let $g(k)=n_{k}$, we've created a new 1-1 [[Math/Principles of Mathematical Analysis/Correspondence\|correspondence]]. This shows that $E$ is countable.


> [!info]  [[Math/Principles of Mathematical Analysis/Union and Intersection\|Union]] of countable sets are countable
> Let $\{ E_{n} \}$, $n=1,2,3,\dots$ be a sequence of countable sets, and put 
> $$
> S=\bigcup_{n=1}^{\infty}E_{n}
> $$
> Then $S$ is countable
> 
> Proof:
>
Let every set $E_n$ be arranged in a sequence $\{x_{nk}\}$, $k = 1, 2, 3, \dots$, and consider the infinite array
>
$$\begin{array}{ccccc}x_{11} & x_{12} & x_{13} & x_{14} & \dots \\x_{21} & x_{22} & x_{23} & x_{24} & \dots \\x_{31} & x_{32} & x_{33} & x_{34} & \dots \\x_{41} & x_{42} & x_{43} & x_{44} & \dots \\\dots & \dots & \dots & \dots & \dots \end{array}$$
>
in which the elements of $E_n$ form the $n$th row. The array contains all elements of $S$.  These elements can be arranged in a sequence
>
$$x_{11}; x_{21}, x_{12}; x_{31}, x_{22}, x_{13}; x_{41}, x_{32}, x_{23}, x_{14}; \dots$$
>
If any two of the sets $E_n$ have elements in common, these will appear more than once in (17). Hence there is a subset $T$ of the set of all positive integers such that $S \sim T$, which shows that $S$ is at most countable (Theorem 2.8). Since $E_1 \subset S$, and $E_1$ is infinite, $S$ is infinite, and thus countable.
>
>$\blacksquare$

> [!info] The set of all  n-tuples of a countable set is countable
> Let $A$ be a countable set, and let $B_{n}$ be the set of all n-tuples $(a_{1},\dots,a_{n})$, where $a_{k}\in A$ and the elements $a_{1},\dots,a_{n}$ need not be distinct. Then $B_{n}$ is countble.
> 
> Proof:
> 
> Let $A$ be a countable set. Since $A$ is countable, its elements can be arranged in a definite sequence and indexed as $A = \{e_1, e_2, e_3, \dots\}$. Consequently, any $n$-tuple in $B_n$ can be uniquely represented as $(e_{k_1}, e_{k_2}, \dots, e_{k_n})$, where each index $k_i$ is a positive integer.
>
To prove $B_n$ is countable, we must establish a systematic order that lists every possible $n$-tuple without infinitely delaying any element. We achieve this by defining a "weight" $W$ for each $n$-tuple, calculated as the algebraic sum of its indices: $W = k_1 + k_2 + \dots + k_n$. Since each $k_i \ge 1$, the minimum possible weight for any tuple is $n$. For any fixed integer $S \ge n$, the algebraic equation $k_1 + k_2 + \dots + k_n = S$ possesses only a finite number of solutions in strictly positive integers. Therefore, the number of $n$-tuples sharing the exact same weight $S$ is strictly finite.
>
We can now arrange all elements of $B_n$ into a single, comprehensive sequence by listing them in order of strictly increasing weight. We begin by listing the finite group of tuples with weight $W = n$ (which contains exactly one element: $(e_1, e_1, \dots, e_1)$), followed by the finite group of tuples with weight $W = n+1$, then $W = n+2$, continuing this process indefinitely. Within each finite group sharing the same weight, we arrange the constituent tuples lexicographically based on their index sequences to guarantee an absolute, unambiguous order.
>
Through this explicit sorting rule, any arbitrary $n$-tuple in $B_n$ possesses a specific, finite weight $W$ and will consequently appear at a finite, calculable position within our master sequence. Since we have successfully mapped all elements of $B_n$ to the set of positive integers without omission, $B_n$ is countable. 
>
$\blacksquare$


Notice the similarities between this proof and the last proof, the are essentially the same but the proof for n-tuples extends it to a higher dimension.

> [!info]  Binary sequence is uncount
> Let $A$ be the set of all sequence whose elements are the digits 0 and 1. This set $A$ is uncountable.
> 
> Proof:
> 
> Suppose $A$ is countble, which there is a [[Math/Principles of Mathematical Analysis/Correspondence\|correspondence]] between $A$ and $J$. We can write $A$ into a sequence $\{ s_{n} \}$, so that every element in $A$ is assigned to a unique postitive integer. We now construct a new sequence $s$: flip the first digit of $s_{1}$ and let it be the first digit of $s$, flip the second digit of $s_{2}$ and let it be the second digit of $s$...... Continue this fasion and we get a new sequence that is different than any other sequnece in $\{ s_{n} \}$. Contradiction occurs, thus, $A$ is uncountable.
> 
> $\blacksquare$

