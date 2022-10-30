>​	Mathematical Logic and Graph Theory 2022 Homework 8 Answers
>
>By [Jingyi Chen](chenjingyi071@mail.ustc.edu.cn) with C and [Songxiao Guo](logname@mail.ustc.edu.cn) with G after each question number.

[TOC]

#### 6.4.15 C

>Find the strongly connected components of each of these graphs.
>
><img src="../asserts/6_4_15.png" style="zoom: 50%;" />

#### 6.4.23 C

>Use paths either to show that these graphs are not isomorphic or to ﬁnd an isomorphism between them.
>
><img src="../asserts/6_4_23.png" style="zoom:50%;" />

#### 6.4.37 C

>Show that a simple graph with at least two vertices has at least two vertices that are not cut vertices.

#### 6.4.45 G

>Show that a simple graph $G$ with $n$ vertices is connected if it has more than $(n − 1)(n − 2)∕2$ edges.

假设图 $G$ 不是连通的，设 $H_1,H_2,\cdots,H_m$ 是 $G$ 的 $m\geq2$ 个连通片 。考虑 $|E(G)|$：
$$
(n-1)(n-2)/2<|E(G)|=\sum_{i=1}^m(|H_i|)(|H_i|-1)/2\leq (n-1)(n-2)/2,
$$
矛盾！故 $m=1$，即 $G$ 连通。这里用到凸函数的性质：$f(x)$是凸函数，则对$\forall x\leq y$,$f(x)+f(y)\leq f(x-1)+f(y+1).$

#### 6.4.47 G

>How many nonisomorphic connected simple graphs are there with $n$ vertices when $n$ is
>a) 2?
>b) 3?
>c) 4?
>d) 5?

- a) 1
- b) 2
- c) 6
- d) 21

#### 6.4.53 G

>Find $𝜅(K_{ m,n} )$ and $𝜆(K_{ m,n} )$, where $m$ and $n$ are positive integers.

由 Whiteny 定理，$𝜅(K_{ m,n} )=\min\{p(u,v)|u,v\in V(G),u\neq v\}$；由 Merge 定理，$p(u,v)=c(u,v)$；考虑 $K_{ m,n} $ 中任意不相邻两点 $u,v$ 形成的割集，当 $u,v$ 属于 $K_{ m,n} $ 的同一部时， $u,v$ 间有 $\min\{m,n\}$ 条除顶点以外无公共顶点的路径；当 $u,v$ 属于 $K_{ m,n} $ 的不同一部时， $u,v$ 一定相邻，不需要考虑，故 $𝜅(K_{ m,n} )=\min\{m,n\}$。

由两种连通度的关系，$𝜅(K_{ m,n} )\leq \lambda(K_{ m,n} )\leq\delta(K_{ m,n} )$，又因为 $𝜅(K_{ m,n} )=\delta(K_{ m,n} )=\min\{m,n\}$，故不等号取等，即 $\lambda (K_{ m,n} )=\min\{m,n\}.$
