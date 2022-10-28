>​	Mathematical Logic and Graph Theory 2022 Homework 8 Answers
>
>By [Jingyi Chen](chenjingyi071@mail.ustc.edu.cn) with C and [Songxiao Guo](logname@mail.ustc.edu.cn) with G after each question number.

[TOC]

#### 6.4.15 C

>Find the strongly connected components of each of these graphs.
>
><img src="../asserts/6_4_15.png" style="zoom: 50%;" />

a){a,b,f}和{c,d,e}

b){a,b,c,d,e,h},{f}和{g}（不要漏掉后两个）

c){a,b,d,e,f,g,h,i}和{c}

#### 6.4.23 C

>Use paths either to show that these graphs are not isomorphic or to ﬁnd an isomorphism between them.
>
><img src="../asserts/6_4_23.png" style="zoom:50%;" />

是同构的，左边的12765834和右边的56783412。

#### 6.4.37 C

>Show that a simple graph with at least two vertices has at least two vertices that are not cut vertices.

（最长边法）定义顶点u,v之间的距离d(u,v)是它们之间最短通路的长度，设图中s,t是使d(s,t)最大的两个顶点（即最长边的两个端点）。如果s和t不都不是割点，比如s是割点，那么割出的至少两个连通片中，记w为不在t的连通片内的一个点。因为从t到w的任一通路都经过s，所以d(w,t)>d(s,t)，矛盾！所以s和t都是割点。

#### 6.4.45 G

>Show that a simple graph $G$ with $n$ vertices is connected if it has more than $(n − 1)(n − 2)∕2$ edges.

#### 6.4.47 G

>How many nonisomorphic connected simple graphs are there with n vertices when n is
>a) 2?
>b) 3?
>c) 4?
>d) 5?

#### 6.4.53 G

>Find $𝜅(K_{ m,n} )$ and $𝜆(K_{ m,n} )$, where m and n are positive integers.
