>Mathematical Logic and Graph Theory 2022 Homework 4 Answers
>
>By [Jingyi Chen](chenjingyi071@mail.ustc.edu.cn) with C and [Songxiao Guo](logname@mail.ustc.edu.cn) with G after each question number.

[TOC]

#### 3.1.41 C

> A palindrome is a string whose reversal is identical to the string. How many bit strings of length n are palindromes?

$n$为偶数时，$2^{n/2}$；$n$为奇数时，$2^{(n+1)/2}$。

#### 3.1.53 C

>How many bit strings of length eight contain either three consecutive 0s or four consecutive 1s?

$147$个。

包含$3$个连续的$0$的个数是$107$，$4$个连续$1$的个数是$48$，都包含的个数是$8$，容斥原理得$147$。

#### 3.1.77 C

>How many diagonals does a convex polygon with n sides have? (Recall that a polygon is convex if every line segment connecting two points in the interior or boundary of the polygon lies entirely within this set and that a diagonal of a polygon is a line segment connecting two vertices that are not adjacent.)

$n(n-3)/2$，从每个顶点往另外$n-3$个顶点连线，每条线都重复了一次。

#### 3.2.13 C

>Let $(x_i , y_ i , z_ i ), i = 1, 2, 3, 4, 5, 6, 7, 8, 9$, be a set of nined istinct points with integer coordinates in xyz space.
>Show that the midpoint of at least one pair of these points has integer coordinates.

一对点的$3$个维度分别有相同的奇偶性，他们的中点坐标就是整数的；每个点的$3$个维度的奇偶性一共有8中情况，鸽巢原理必有$2$个点的坐标奇偶性一致，中点坐标为整数。

#### 3.2.15 G

>- a) Show that if ﬁve integers are selected from the ﬁrst eight positive integers, there must be a pair of these
> integers with a sum equal to 9.
>- b) Is the conclusion in part (a) true if four integers are selected rather than ﬁve?

- a) 将集合 $\{1,2\cdots 8\}$ 划分成 $\{1,8\}$、$\{2,7\}$、$\{3,6\}$ 和 $\{4,5\}$ 4个不相交的集合。由抽屉原理，在 $\{1,2\cdots 8\}$ 中任取 $5$ 个元素，必有至少 $2$ 个元素在被划分成的某个集合中。另一方面，被划分成的任意集合，里的两个元素的和为 $9$ ，故结论成立。
- b) 不成立。如 $\{1,2,3,4\}$，可以枚举验证其中没有两个数的和为 $9$ 。

#### 3.2.25 G

>Show that whenever 25 girls and 25 boys are seated around a circular table there is always a person both of
>whose neighbors are boys.

将圆桌的座位从 $1～50$ 编号， $50$ 号座位与 $1$ 号座位相邻。有 $25$ 个奇数号座位， $25$ 个偶数号座位。如果最多有 $12$ 个男生获得了奇数号座位，那么至少有 $13$ 个男生获得了偶数号座位。反之亦然。故不失一般性，假设至少有 $13$ 个男生获得了 $25$ 个奇数座位中的一些位置，那么这些男生中至少有 $2$ 个会获得连续的奇数号，这样坐在他们中间的人就会是左右都与一个男生相邻。

#### 3.2.49 G

>An alternative proof of Theorem 3 based on the generalized pigeonhole principle is outlined in this exercise. The
>notation used is the same as that used in the proof in the text.
>
>- a) Assume that $i_k ≤ n$ for $k = 1, 2, … , n^ 2 + 1$. Use the generalized pigeonhole principle to show that there are $n + 1$ terms $a _{k_ 1} , a _{k_ 2} , \cdots, a _{k_ {n+1}}$ with $i _{k _1} = i_{ k _2} = \cdots = i_ {k_ n}+1$ , where $1 ≤ k_ 1 < k_ 2 < ⋯ < k _{n+1}$ .
>- b) Show that $a _{k _j} > a _{k _{j+1}}$ for $j = 1, 2, \cdots , n$. 
>- c) Use parts (a) and (b) to show that if there is no increasing subsequence of length $n + 1$, then there must be a decreasing subsequence of this length.

- a) 根据广义鸽巢原理，至少有 $\lceil(n^2+1)/n\rceil=n+1$ 个数字 $i_{k_1},i_{k_2},\cdots,i_{k_{n+1}}$ 相等。
- b) 如果 $a_{k_j}<a_{k_{j+1}}$ ，那么长度为 $i_{k_j}$ 以 $a_{k_j}$ 开头的子序列包含长度为 $i_{k_j+1}$ ，以 $a_{k_{j+1}}$ 开头的递增子序列。这与 $i_{k_j}=i_{k_{j+1}}$ 矛盾。
- c) 如果没有长度超过 $n$ 的递增子序列，那么就有 $i_k\leq n$ ，便满足 a) 的条件。根据 b) ，有 $a _{k_ 1} > a _{k_ 2} > \cdots> a _{k_ {n+1}}$，构造出了长度为 $n+1$ 的递减子序列。