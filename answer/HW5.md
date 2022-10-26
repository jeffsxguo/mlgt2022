>Mathematical Logic and Graph Theory 2022 Homework 5 Answers
>
>By [Jingyi Chen](chenjingyi071@mail.ustc.edu.cn) with C and [Songxiao Guo](logname@mail.ustc.edu.cn) with G after each question number.

[TOC]

#### 3.3.23 G

>How many ways are there for eight men and ﬁve women to stand in a line so that no two women stand next to each other?

用插空法，先组合再排列，将 $8$ 个男士排成一排，算上首尾，共 $9$ 个空。在其中选择 $5$ 个放女士，再考虑人的不同，共 $A_8^8A_5^5C_{9}^5=609638400$ 种。

#### 3.3.31 G

>How many $4-$permutations of the positive integers not exceeding $100$ contain three consecutive integers $k, k + 1,k + 2$, in the correct order
>
>- a) where these consecutive integers can perhaps be separated by other integers in the permutation?
>- b) where they are in consecutive positions in the permutation?

- a) 

  1. 包含恰好 $3$ 个连续的整数：在前 $100$ 个数中选择连续的 $3$ 个数，有 $100-3+1=98$ 种。根据本题的需要，分成两类：$1,2,3$、$98,99,100$ 为第 $1$ 类，其他 $96$ 种为第 $2$ 类。对于第 $1$ 类，再选出一个与已选出的 $3$ 个数不相连的种类有 $96$ 种，而对于第 $2$ 类，有 $95$ 种。组合后再排列，每种选出的 $4$ 个数，都有 $4$ 种方式使其顺序相同。这种情况有 $(2\times 96+96\times95)\times 4=37248$ 种。
  2. 包含 $4$ 个连续的整数：在前 $100$ 个数中选择连续的 $4$ 个数，有 $100-4+1=97$ 种。每种选出的 $4$ 个数，都含有 $2$ 种连续的 $3$ 个数，故有 $4\times2-1=7$ 种方式使其中有连续的 $3$ 个数顺序相同。（排除重复情况）。这种情况有 $97\times7=679$ 种。

  共有 $37248+679=37927$ 种。

- b)

  1. 包含恰好 $3$ 个连续的整数：在前 $100$ 个数中选择连续的 $3$ 个数，有 $100-3+1=98$ 种。根据本题的需要，分成两类：$1,2,3$、$98,99,100$ 为第一类，其他 $96$ 种为第 $2$ 类。对于第 $1$ 类，再选出一个与已选出的 $3$ 个数不相连的种类有 $96$ 种，而对于第 $2$ 类，有 $95$ 种。组合后再排列，每种选出的 $4$ 个数，都有 $2$ 种方式使其顺序相同且连续。这种情况有 $(2\times 96+96\times95)\times 2=18624$ 种。
  2. 包含 $4$ 个连续的整数：在前 $100$ 个数中选择连续的 $4$ 个数，有 $100-4+1=97$ 种。每种选出的 $4$ 个数，都含有 $2$ 种连续的 $3$ 个数，故有 $2\times2-1=3$ 种方式使其中有连续的 $3$ 个数顺序相同。（排除重复情况）。这种情况有 $97\times3=291$ 种。

  共有 $18624+291=18915$ 种。

#### 4.1.17 G

>- a) Find a recurrence relation for the number of ternary strings of length $n$ that do not contain consecutive
> symbols that are the same.
>- b) What are the initial conditions?
>- c) How many ternary strings of length six do not contain consecutive symbols that are the same?

- a) 考虑长为 $n-1$ 的串，与其最后一位不同的符号有两个，从中选择一个，并加在长为 $n-1$ 的串后面，就得到了长为  $n$ 的满足要求的串。另一方面，对每个长为 $n$ 的满足要求的串，减去其末尾，都能得到一个对应的长为 $n-1$ 的满足要求的串。设长为 $n$ 的满足要求的串的个数为 $a_n$ ，则 $a_n=2 a_{n-1},n\geq2$。
- b) $a_1=3$。
- c) $a_n=2^{n-1}\times 3\Rightarrow a_6=96$。

#### 4.1.27 G

> - a) Find a recurrence relation for the number of ways to lay out a walkway with slate tiles if the tiles are red, green, or gray, so that no two red tiles are adjacent and tiles of the same color are considered indistinguishable.
> - b) What are the initial conditions for the recurrence relation in part (a)?
> - c) How many ways are there to lay out a path of seven tiles as described in p  art (a)?

- a) 设 $a_n$ 表示没有红色砖相邻的用 $n$ 块砖铺路的方式， $b_n$ 表示没有红色砖相邻，且最后一块为红色的用 $n$ 块砖铺路的方式。易知 $a_n=2b_{n-1}+3(a_{n-1}-b_{n-1})$，$b_n=a_{n-1}-b_{n-1}$，得到 $a_n=2a_{n-1}+2a_{n-2},n\geq3$。
- b) $a_1=3,a_2=8.$
- c) 利用特征方程法求得 $a_n=\frac{\sqrt3+2}{2\sqrt3}(1+\sqrt3)^n+\frac{\sqrt3-2}{2\sqrt3}(1-\sqrt3)^n$。故 $a_7=1224$。

#### 4.1.29 G

> Let $S(m, n)$ denote the number of onto functions from a set with $m$ elements to a set with $n$ elements. Show that $S(m, n)$ satisﬁes the recurrence relation
> $$
> S(m,n)=n^m-\sum_{k=1}^{n-1}C_n^kS(m,k)
> $$
> whenever $m ≥ n$ and $n > 1$, with the initial condition $S(m, 1) = 1$.

$n=1$ 时，易知$S(m,1)=1$。$n\geq2$ 时，考虑从 $m$ 元集到 $n$ 元集的所有映射，共有 $n^m$ 个，如果一个映射不是映上的，等价于它的值域可以取 $1,2,\cdots,n-1$。对每个 $i\in\{1,2,\cdots,n-1\}$ ，从 $n$ 元集中取 $i$ 个的种类有 $C_n^k$ 种。这样便有 $S(m,n)=n^m-\sum_{k=1}^{n-1}C_n^kS(m,k),m\geq n,n>1$。

#### 4.1.35 G

>This problem is based on an account by the historian Flavius Josephus, who was part of a band of 41 Jewish rebels trapped in a cave by the Romans during the Jewish-Roman war of the ﬁrst century. The rebels preferred suicide to capture; they decided to form a circle and to repeatedly count oﬀ around the circle, killing every third rebel left alive. However, Josephus and another rebel did not want to be killed this way; they determined the positions where they should stand to be the last two rebels remaining alive. The variation we consider begins with n people, numbered 1 to n, standing around a circle. In each stage, every second person still left alive is eliminated until only one survives. We denote the number of the survivor by $J(n)$.
>
>Show that $J(n)$ satisﬁes the recurrence relation $J(2n) = 2J(n) − 1$ and $J(2n + 1) = 2J(n) + 1$, for $n ≥ 1$, and $J(1) = 1$.

- 当人数是偶数时，首先偶数位置的人被排除，则原来站在 $2i-1$ 位置的人，现在站在 $i$ 位置（$i=1,2,\cdots,n$）。此时剩下 $n$ 人。那么最后剩下的人在 $J(n)$ 位置的人，原来站在 $2J(n)-1$ 位置。
- 当人数是奇数时，首先偶数位置的人被排除，再排除 $1$ 号位置的人，则原来站在 $2i+1$ 位置的人，现在站在 $i$ 位置$i=1,2,\cdots,n$）。此时剩下 $n$ 人。那么最后剩下的人在 $J(n)$ 位置的人，原来站在 $2J(n)+1$ 位置。

#### 4.5.17 G

>How many permutations of the $10$ digits either begin with the $3$ digits $987$, contain the digits $45$ in the ﬁfth and sixth positions, or end with the $3$ digits $123$?

根据容斥原理，满足条件的排列数为 
$$
A_7^7+A_8^8+A_7^7-A_5^5-A_5^5-A_4^4+A_2^2=50138.
$$

#### 4.6.15 C

>A machine that inserts letters into envelopes goes haywire and inserts letters randomly into envelopes. What is
>the probability that in a group of $100$ letters
>
>- a) no letter is put into the correct envelope?
>- b) exactly one letter is put into the correct envelope?
>- c) exactly $98$ letters are put into the correct envelopes?
>- d) exactly $99$ letters are put into the correct envelopes?
>- e) all letters are put into the correct envelopes?

- a) $D_{100}/100!.$
- b) $100D_{99}/100!.$
- c) $C(100,2)/100!.$
- d) $0.$
- e) $1/100!.$

#### 4.6.17 C

>How many ways can the digits $0, 1, 2, 3, 4, 5, 6, 7, 8, 9$ be arranged so that no even digit is in its original position?

由逐步淘汰原理：
$$
A_{10}^{10}-C_5^1A_9^9+C_5^2A_8^8-C_5^3A_7^7+C_5^4A_6^6-C_5^5A^5_5=2170680.
$$

#### 5.1.5 C

>Determine whether the relation $R$ on the set of all Web pages is reﬂexive, symmetric, antisymmetric, and/or
>transitive, where $(a, b) ∈ R$ if and only if
>
>- a) everyone who has visited Web page $a$ has also visited Web page $b$.
>- b) there are no common links found on both Web page $a$ and Web page $b$.
>- c) there is at least one common link on Web page $a$ and Web page $b$.
>- d) there is a Web page that includes links to both Web page $a$ and Web page $b$.

- a) 自反的，传递的。
- b) 对称的。
- c) 对称的。
- d) 对称的。

#### 5.1.9 C 

>Show that the relation $R = ∅$ on the empty set $S = ∅$ is reﬂexive, symmetric, and transitive.

自反性$\forall a((a,a)\in R)$对，因为没这个a；对称性和传递性也对，也是因为没有a,b。（否定前件律）

#### 5.1.49 C

>How many relations are there on a set with n elements that are
>
>- a) symmetric?
>- b) antisymmetric?
>- c) asymmetric?
>- d) irreﬂexive?
>- e) reﬂexive and symmetric?
>- f ) neither reﬂexive nor irreﬂexive?

- a)$2^{n(n+1)/2}$，因为每两者（包括自己和自己）之间可能有这个对称关系。
- b)$2^n3^{n(n-1)/2}$，因为每个元素都可以和自己有该关系也可以没有，同时，每两不同元素之间可能有两种方向的关系或没有关系。
- c)$3^{n(n-1)/2}$，因为每不同两者之间可能有两种方向的该关系或者没有关系。
- d)$2^{n(n-1)}$，因为自己和自己没有，每有序两者之间可能有该关系或没有。
- e)$2^{n(n-1)/2}$，因为自己和自己只能有，每无序两者之间可能有关系或没有。
- f)$2^{n^2}-2\times2^{n(n-1)}$，所有关系减去自反的、反自反的，自反的和反自反的一样多。

#### 5.1.57 C

>Let $R$ be a relation that is reﬂexive and transitive. Prove that $R ^n = R$ for all positive integers $n$.

归纳法，如果$R^n$是自反的、传递的，则因为是传递的，$R^{n+1}\subseteq R$；$(a,b)\in R$时，$(b,b)\in R^n$，所以$(a,b)\in R^{n+1}$。

#### 5.2.23 C

>Show that if $C$ is a condition that elements of the $n-$ary relations $R$ and $S$ may satisfy, then
>$s C (R ∩ S) = s C (R) ∩ s C (S)$.

如果一个$n$元组在$R\cap S$中且满足条件$C$，那么它或者在R中或者在$S$中且满足条件$C$，因此它也属于右侧；类似的如果一个$n$元组属于右侧，则它既在$R$中且满足条件$C$又在$S$中且满足条件$C$，因此它在$R\cap S$中且满足条件$C$，因此它也属于左侧。
