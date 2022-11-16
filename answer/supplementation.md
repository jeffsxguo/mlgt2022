> - MLGT 2022 Supplementary Questions
> - [Songxiao Guo](logname@mail.ustc.edu.cn)
> - v1.0 2022-11-15 Add raw questions.
> - v1.1 2022-11-15 Remove some questions lacking in requirements.
> - v2.0 2022-11-15 Add solutions to questions.
> - v2.1 2022-11-16 Fix bugs.
> - v3.0 2022-11-16 Add wrong solutions to questions.

[TOC]

### 树

>1、设树的 $i$ 次顶的个数为 $n_i,i\geq2$，求 $1$ 次顶的个数。

对边数算两次：
$$
\frac12\sum_{k=1}^m kn_k=\varepsilon(T)=\sum_{k=1}^mn_k-1
$$

$$
n_1=\sum_{k=2}^m(k-2)n_k+2.
$$

----

> 2、$n$ 个顶的树的最大度数最小是多少，最大是多少？

==错误解答之一==

最大度数的最小值是 $2$。在一棵 $2$ 个顶的树的唯一的边上，放 $n-2$ 个点，将其分成 $n-1$ 段。

最大度数的最大值为 $n-1$。任取一个顶点，与其他所有顶点相邻。

==错误解答之二==

**当 $n=1$ 时，二者显然均为 $0$。**

**当 $n=2$ 时，最大度数的最小值显然是 $1$。**

最大度数的最小值是 $2$。在一棵 $2$ 个顶的树的唯一的边上，放 $n-2$ 个点，将其分成 $n-1$ 段。

最大度数的最大值为 $n-1$。任取一个顶点，与其他所有顶点相邻。

==正确解答==

**当 $n=1$ 时，二者显然均为 $0$。**

**当 $n=2$ 时，最大度数的最小值显然是 $1$。**

当 $n\geq2$​ 时，最大度数的最小值是 $2$。

- **给出取到最值的构造**：在一棵 $2$ 个顶的树的唯一的边上，放 $n-2$ 个点，将其分成 $n-1$ 段。
- **证明不可以更小**：如果最大度数为 $1$，则所有的顶点度数都为 $1$。对边数算两次有 $n/2\nu(T)/2=\varepsilon(T)=\nu(T)-1=n-1$，在 $n\geq2$时不成立。

当 $n\geq1$ 时，最大度数的最大值为 $n-1$。

- **给出取到最值的构造**：任取一个顶点，与其他所有顶点相邻。
- **证明不可以更大**：如果最大度数为 $n$ 说明至少需要 $n+1$ 个顶点，与题意不符。

----

> 3、证明树的最长轨道的端点为叶。

==错误解答==

设 $P=v_0v_1\dots v_n$ 是树 $T$ 的最长轨道，假设 $v_0$ 不是叶，则 $v_0$ 有除了 $v_1$ 以外的邻顶 $u$。故找到了比 $P$ 更长的轨道 $uv_0\dots v_n$，与 $P$ 是最长轨道矛盾。故 $v_0$ 是叶。同理 $v_n$ 也是叶。

==正确解答==

设 $P=v_0v_1\dots v_n$ 是树 $T$ 的最长轨道，假设 $v_0$ 不是叶，则 $v_0$ 有除了 $v_1$ 以外的邻顶 $u$。**如果 $\exist i,i\neq0,u=v_i$ ，则形成环 $uv_0\dots v_iu$，与 $T$ 是树矛盾。**故找到了比 $P$ 更长的轨道 $uv_0\dots v_n$，与 $P$ 是最长轨道矛盾。故 $v_0$ 是叶。同理 $v_n$ 也是叶。

----

### 图的连通性

> 1、证明：若 $G$ 是 $k-$边连通图，$E'$ 是 $G$ 中 $k$ 条边集合，则有 $\omega(G-E')\leq 2$。

假设 $\omega(G-E')> 2$，则说明将 $E'$ 中的边从 $G$ 中去掉后，$G$ 形成至少 $3$ 个连通片。**由于去掉一条边最多使连通片个数加 $1$**，我们一条一条从 $G$ 中去掉 $E'$ 中的边，当刚好使 $G$ 不连通时，去掉的边小于 $|E'|=k$ 条。这样 $G$ 的边连通度小于 $k$ ，与原提设矛盾。故原结论成立。

----

### 平面图

> 1、若 $G$ 是连通平面图，没有奇圈，且顶点数大于等于 $3$，证明：$\varepsilon\leq 2\nu-4$。

没有奇圈，则 $G$ 的**平面嵌入**的每个面的边数至少是 $4$。$1$ 条边对应 $1$ 个面 $2$ 次，有 $4\phi\leq 2\varepsilon$。 由 Euler 公式，$2=\nu-\varepsilon+\phi\leq \nu-\varepsilon+2\varepsilon/4$，即 $\varepsilon\leq 2\nu-4$。

----

### 匹配理论

>1、二分图 $G$ 满足 $|X|=|Y|=n$，且 $\delta(G)\geq n/2$，证明 $G$ 有完备匹配。

任取 $S\subseteq X$，

- $|S|\leq n/2$：则 $|N(S)|\ge\delta(G)\ge n/2\ge|S|$，由 Hall 定理知 $G$ 有完备匹配。

- $|S|> n/2$：考虑 $Y$ 中的顶点 $y$，如果 $N(\{y\})\cap S=\empty$，则
  $$
  n=|X|\ge|S\cup N(\{y\})|=|S|+| N(\{y\})|-|S\cap N(\{y\})|=|S|+| N(\{y\})|\ge|S|+\delta(G)>n/2+n/2=n,
  $$
  产生矛盾，故 $\forall y\in Y$，都有 $ y\in N(S)$，即 $|N(S)|=n=|X|\ge|S|$，由 Hall 定理知 $G$ 有完备匹配。

----

### Euler 图与 Hamilton 图

> 1、假设 $P=v_1v_2\dots v_k$ 是简单图 $G$ 中的最长轨道，且 $\deg(v_1)+\deg(v_k)\geq k$。证明：存在 $2\leq i\leq k$，使得 $v_1v_i$ 与 $v_{i-1}v_k$ 都是简单图的边。

==错误解答==

令 $S=\{i|v_1v_i\in E(G)\}$，$T=\{i|v_{i-1}v_k\in E(G)\}$。若 $S\cap T=\empty$，则 $|S\cap T|=0$，所以有
$$
k\leq\deg(v_1)+\deg(v_k)=|S|+|T|=|S\cap T|+|S\cup T|=|S\cup T|\leq k-1,
$$
产生矛盾，故 $\exist i\in S\cap T $。故存在 $i$，使得 $v_1v_i$ 与 $v_{i-1}v_k$ 都是简单图的边。

==正确解答==

令 $S=\{i|v_1v_i\in E(G)\}$，$T=\{i|v_{i-1}v_k\in E(G)\}$。**$v_1,v_k$ 的邻顶都属于 $P$，**否则与 $P$ 是最长轨道矛盾。若 $S\cap T=\empty$，则 $|S\cap T|=0$，所以有
$$
k\leq\deg(v_1)+\deg(v_k)=|S|+|T|=|S\cap T|+|S\cup T|=|S\cup T|\leq k-1,
$$
产生矛盾，故 $\exist i\in S\cap T $。**由于 $1\notin S$，**故存在 $2\leq i\leq k$，使得 $v_1v_i$ 与 $v_{i-1}v_k$ 都是简单图的边。

----

> 2、证明 $n\geq5$ 时，$(C_n)^c$ 是 Hamilton 图。

$(C_n)^c$ 是简单图，在 $n\geq5$ 时，$\nu(G)\geq3$，$\delta(G)=\nu(G)\geq\nu(G)/2$，**由 Dirac 定理**知 $G$ 是Hamilton 图。

----

### 图的着色

> 1、对于不是奇圈的 Euler 图，存在 $2-$边着色方案，使得两种颜色，在所有顶点出现。

==错误解答==

**$G$ 是欧拉图，则可以表示成若⼲个⽆公共边的圈之并。**

1. 若 $G$ 没有度数⼤于等于 $4$​ 的点，则 $G$ 是⼀个圈，且是偶圈。易知偶圈可以 $2-$边正常着色。
2. 若 $G$ 有度数⼤于等于 $4$ 的点 。则从该顶点开始，选择⼀个该顶点所在的圈 $C_i$ ，使用两种颜色，交替边着色。重复上述步骤直至所有边都被染色。

==正确解答==

**$G$ 是欧拉图，则可以表示成若⼲个⽆公共边的圈之并。**

1. 若 $G$ 没有度数⼤于等于 $4$​ 的点，则 $G$ 是⼀个圈，且是偶圈。易知偶圈可以 $2-$边正常着色。
2. 若 $G$ 有度数⼤于等于 $4$ 的点 。则从该顶点开始，选择⼀个该顶点所在的圈 $C_i$ ，使用两种颜色，交替边着色。
   - **若 $C_i$ 是偶圈**，则 $C_i$ 上的顶点已满⾜条件；
   - **若 $C_i$ 是奇圈**，则 $C_i$ 中只有 $v_i$ ⽬前只有⼀种颜⾊。
3. 对剩余的圈，从圈上⼀个度数⼤于等于 $4$ 的顶点开始交替着⾊。若该顶点相关连的边只有⼀种颜⾊，则起始⾊使⽤另⼀种颜⾊，否则起始色任选。

----

> 2、证明：任意图 $G$ ，有 $\chi(G)\leq\Delta(G)+1$。

给 $G$ 的任意一个顶点 $v$ 着色时，$ v$ 最多有 $∆(G)$ 个邻点，至多使用了 $∆(G)$ 种颜色， 则 $v$ 可使用第 $∆(G) + 1$ 种颜色，所以 $G$ 是可 $(∆(G) + 1)-$顶点着色的。