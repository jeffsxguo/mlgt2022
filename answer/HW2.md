>  Mathematical Logic and Graph Theory 2022 Homework 2 Answers
>
>By [Jingyi Chen](chenjingyi071@mail.ustc.edu.cn) with C and [Songxiao Guo](logname@mail.ustc.edu.cn) with G after each question number.

[TOC]

#### 1.4.7 C

>Translate these statements into English, where $C(x)$ is “$x$ is a comedian” and $F(x)$ is “$x$ is funny” and the domain consists of all people.
>a) $∀x(C(x) → F(x))$
>b) $∀x(C(x) ∧ F(x))$
>c) $∃x(C(x) → F(x))$
>d) $∃x(C(x) ∧ F(x))$

- a)每个喜剧演员都很有趣；
- b)每个人都是很有趣的喜剧演员；
- c)存在某个人，如果他是喜剧演员，那么他是很有趣的；
- d)某些喜剧演员是很有趣的（某些很有趣的人是喜剧演员）。

#### 1.4.27 C

>Translate each of these statements into logical expressions in three diﬀerent ways by varying the domain and by using predicates with one and with two variables.
>a) A student in your school has lived in Vietnam.
>b) There is a student in your school who cannot speak Hindi.
>c) A student in your school knows Java, Prolog, and C++.
>d) Everyone in your class enjoys Thai food.
>e) Someone in your class does not play hockey.

- a)令谓词 $Y(x)$ 表示语句“$x$ 是在你学校上的学生”。
  - 如果我们令 $V(x)$ 为“$x$ 曾在越南居住”，则
    - 论域是你学校同学时：$\exist xV(x).$
    - 论域是所有人时：$\exist x(Y(x)\and V(x)).$
  - 如果令 $D(x,y)$ 表示 $x$ 曾在国家 $y$ 居住，论域是所有人时：$\exist x(Y(x)\and D(x,越南)).$
- b)令谓词 $Y(x)$ 表示语句“$x$ 是在你学校上的学生”。
  - 如果我们令 $V(x)$ 为“$x$ 会说印地语”，则
    - 论域是你学校同学时：$\exist x\neg V(x).$
    - 论域是所有人时：$\exist x(Y(x)\and\neg V(x)).$
  - 如果令 $D(x,y)$ 表示 $x$ 会说语言 $y$，论域是所有人时：$\exist x(Y(x)\and\neg D(x,印地语)).$
- c)令谓词 $Y(x)$ 表示语句“$x$ 是在你学校上的学生”。
  - 如果我们令 $V(x)$ 为“$x$ 会用 Java、Prolog、C++”，则
    - 论域是你学校同学时：$\exist xV(x).$
    - 论域是所有人时：$\exist x(Y(x)\and V(x)).$
  - 如果令 $D(x,y)$ 表示 $x$ 会用语言 $y$，论域是所有人时：$\exist x(Y(x)\and D(x,Java)\and D(x,Prolog)\and D(x,C++)).$
- d)令谓词 $Y(x)$ 表示语句“$x$ 是在你班上的学生”。
  - 如果我们令 $V(x)$ 为“$x$ 喜欢泰国食物”，则
    - 论域是你班同学时：$\forall x V(x).$
    - 论域是所有人时：$\forall x(Y(x)\to V(x)).$
  - 如果令 $D(x,y)$ 表示 $x$ 喜欢食物 $y$，论域是所有人时：$\forall x(Y(x)\to D(x,泰国)).$
- e)令谓词 $Y(x)$ 表示语句“$x$ 是在你班上的学生”。
  - 如果我们令 $V(x)$ 为“$x$ 打曲棍球”，则
    - 论域是你班同学时：$\exist x\neg V(x).$
    - 论域是所有人时：$\exist x(Y(x)\and\neg V(x)).$
  - 如果令 $D(x,y)$ 表示 $x$ 玩游戏 $y$，论域是所有人时：$\exist x(Y(x)\and\neg D(x,曲棍球)).$

#### 1.4.63 C

>Let $P(x)$, $Q(x)$, $R(x)$, and $S(x)$ be the statements “$x$ is a baby,” “$x$ is logical,” “$x$ is able to manage a crocodile,” and “$x$ is despised,” respectively. Suppose that the domain consists of all people. Express each of these statements using quantiﬁers; logical connectives; and $P(x)$, $Q(x)$, $R(x)$, and $S(x)$.
>a) Babies are illogical.
>b) Nobody is despised who can manage a crocodile.
>c) Illogical persons are despised.
>d) Babies cannot manage crocodiles.
>e) Does (d) follow from (a), (b), and (c)? If not, is there a correct conclusion?

- a)$\forall x(P(x)\to\neg Q(x))$
- b)$\forall x(R(x)\to\neg S(x))$
- c)$\forall x(\neg Q(x)\to S(x))$
- d)$\forall x(P(x)\to\neg R(x))$
- e)可以得出结论。把b)变为$\forall x(S(x)\to \neg R(x))$，反复利用$(p\to q)\and(q\to r)\to(p\to r)$即可由a、b、c得到d。

#### 1.5.7 C

>Let $T(x, y)$ mean that student $x$ likes cuisine $y$, where the domain for $x$ consists of all students at your school andt he domain for $y$ consists of all cuisines. Express each of these statements by a simple English sentence.
>a) $¬T(Abdallah Hussein, Japanese)$
>b) $∃xT(x, Korean) ∧ ∀xT(x, Mexican)$
>c) $∃y(T(Monique Arsenault, y) ∨T(Jay Johnson, y))$
>d) $∀x∀z∃y((x ≠ z) → ¬(T(x, y) ∧ T(z, y)))$
>e) $∃x∃z∀y(T(x, y) ↔ T(z, y))$
>f ) $∀x∀z∃y(T(x, y) ↔ T(z, y))$

- a)Abdallah Hussein 不喜欢日本菜。
- b)学校的某些学生喜欢韩国菜，并且学校的每个人都喜欢墨西哥菜。
- c)存在一些菜，不是 Monique Arsenault 喜欢，就是 Jay Johnson 喜欢。
- d)学校中每一对不同的学生，总有一种菜，他们不都喜欢。
- e)\*
- f)学校中任意两个学生（可能相同），总有一种菜，他们有相同的看法。

#### 1.5.11 C

>Let $S(x)$ be the predicate “$x$ is a student,” $F(x)$ the predicate “$x$ is a faculty member,” and $A(x, y)$ the predicate“$x$ has asked $y$ a question,” where the domain consists of all people associated with your school. Use quantiﬁers to express each of these statements.
>a) Lois has asked Professor Michaels a question.
>b) Every student has asked Professor Gross a question.
>c) Every faculty member has either asked Professor Miller a question or been asked a question by Professor Miller.
>d) Some student has not asked any faculty member a question.
>e) There is a faculty member who has never been asked a question by a student.
>f ) Some student has asked every faculty member a question.
>g) There is a faculty member who has asked every other faculty member a question.
>h) Some student has never been asked a question by a faculty member.

- a)$A(Lois,Michaels 教授).$
- b)$\forall x(S(x)\to A(x,Gross教授)).$
- c)$\forall x(F(x)\to(A(x,Miller教授)\or A(Miller教授,x))).$
- d)$\exist x(S(x)\and\forall y(F(y)\to\neg A(x,y))).$
- e)$\exist x(F(x)\and\forall y(S(y)\to\neg A(y,x))).$
- f)$\forall y(F(u)\to\exist x(S(x)\and A(x,y))).$
- g)$\exist x(F(x)\and\forall y((F(y)\and(y\neq x))\to A(x,y))).$
- h)$\exist x(S(x)\and\forall y(F(y)\to\neg A(y,x))).$

#### 1.5.21 C

>Use predicates, quantiﬁers, logical connectives, and mathematical operators to express the statement that every positive integer is the sum of the squares of four integers.

$$
\forall x\exist a\exist b\exist c\exist d((x>0)\to x=a^2+b^2+c^2+d^2),
$$

论域为全体整数。

#### 1.5.35 C

>Find a common domain for the variables $x$, $y$, $z$, and $w$ for which the statement $∀x∀y∀z∃w((w ≠ x) ∧ (w ≠ y) ∧ (w ≠ z))$ is true and another common domain for these variables for which it is false.

任意具有4个或更多不同成员的论域会使命题为真，任意具有3个或更少成员的论域会使命题为假。

#### 1.6.11 G

>Show that the argument form with premises $p_1 ,p_2 ,\cdots,p_ n$ and conclusion $q → r$ is valid if the argument form with premises $p _1 ,p_ 2 ,…,p _n$ ,$q$, and conclusion $r$ is valid.

当 $q$ 为真时，由给定论证形式的有效性（$p_1\and p_2\cdots \and p_n\and q\to r$）知当 $p_1,p_2,\cdots,p_n$ 为真时，$r$ 为真，故 $q\to r$ 为真。

当 $q$ 为假时，$q\to r$ 为真自然成立。

综上可知结论成立。

#### 1.6.23 G

> Identify the error or errors in this argument that supposedly shows that if $∃xP(x) ∧ ∃xQ(x)$ is true then $∃x(P(x) ∧ Q(x))$ is true.
>
> 1.$∃xP(x) \and ∃xQ(x)$ Premise
> 2.$∃xP(x)$ Simplification from (1)
> 3.$P(c)$ Existential instantiation from (2)
> 4.$∃xQ(x)$ Simplification from (1)
> 5.$Q(c)$ Existential instantiation from (4)
> 6.$P(c) ∧ Q(c)$ Conjunction from (3) and (5)
> 7.$∃x(P(x) ∧ Q(x))$ Existential generalization

第 5 步存在实例错误。$c$ 已经被使用过，在此处的 $c$ 没有理由是第 3 步所使用的 $c$ 。

#### 1.6.29 G

>Use rules of inference to show that if $∀x(P(x) ∨ Q(x))$,$∀x(¬Q(x) ∨ S(x))$, $∀x(R(x) → ¬S(x))$, and $∃x¬P(x)$ are true, then $∃x¬R(x)$ is true.

$$
\begin{align}
&1.\exist x\neg P(x)&前提引入\\
&2.\neg P(c)&存在实例，由(1)\\
&3.\forall x(P(x)\or Q(x))&前提引入\\
&4.P(c)\or Q(c)&全称实例，由(3)\\
&5.Q(c)&析取三段论，由(2)和(4)\\
&6.\forall x(\neg Q(x)\or S(x))&前提引入\\
&7.\neg Q(c)\or S(c)&全称实例，由(6)\\
&8.\neg(\neg Q(c))&双重否定律，由(5)\\
&9.S(c)&析取三段论，由(7)和(8)\\
&10.\forall x(R(x)\to\neg S(x))&前提引入\\
&11.R(c)\to\neg S(c)&存在实例，由(10)\\
&12.\neg(\neg S(c))&双重否定律，由(9)\\
&13.\neg R(c)&取拒式，由(11)和(12)\\
&14.\exist x\neg R(x)&存在引入，由(13)
\end{align}
$$

#### 1.6.35 G

>Determine whether this argument, taken from Kalish and Montague [KaMo64], is valid. If Superman were able and willing to prevent evil, he would do so. If Superman were unable to prevent evil,he would be impotent; if he were unwilling to prevent evil, he would be malevolent. Superman does not prevent evil. If Superman exists, he is neither impotent nor malevolent. Therefore, Superman does not exist.

用 $x_1$ 表示超人能够防止邪恶，用 $x_2$ 表示超人愿意防止邪恶，用 $x_3$ 表示超人防止邪恶，用 $x_4$ 表示超人是无能的，用 $x_5$ 表示超人是恶意的，用 $x_6$ 表示超人存在。则该论证的前提是
$$
x_1\and x_2\to x_3,\neg x_1\to x_4,\neg x_2\to x_5,\neg x_3,x_6\to(\neg x_4\and\neg x_5),
$$
期望的结论是 
$$
\neg x_6.
$$
这样的论证形式证明这些前提导出期望的结论：
$$
\begin{align}
&1.x_1\and x_2\to x_3&前提引入\\
&2.\neg x_3&前提引入\\
&3.\neg(x_1\and x_2)&取拒式，由(1)和(2)\\
&4.\neg(\neg(x_1\to \neg x_2))&条件命题的逻辑等价式，由(3)\\
&5.x_1\to\neg x_2&双重否定律，由(4)\\
&6.\neg x_2\to x_5&前提引入\\
&7.x_1\to x_5&假言三段论，由(5)和(6)\\
&8.\neg x_5\to \neg x_1& 条件命题的逻辑等价式，由(7)\\
&9.\neg x_1\to x_4& 前提引入\\
&10.\neg x_5\to x_4&假言三段论，由(8)和(9)\\
&11.x_5\or x_4&条件命题的逻辑等价式，由(10)\\
&12.\neg(\neg x_5\and \neg x_4)& 德\cdot 摩根律，由(11)\\
&13.x_6\to(\neg x_4\and\neg x_5)&前提引入\\
&14.\neg x_6&取拒式，由(13)
\end{align}
$$

#### 1.7.15 G

> Prove that if $x$ is an irrational number and $x > 0$, then $\sqrt x$ is also irrational.

假设结论不成立，即 $\sqrt x$ 是有理数。由 $x>0$，可设 $\sqrt x=\frac pq,p,q\in \mathbb Z^*$，故有 $x=\sqrt x\sqrt x=\frac{p^2}{q^2},p^2,q^2\in\mathbb Z^*$，即 $x$ 是有理数，矛盾！故结论成立。

#### 1.7.19 G

> Show that if $n$ is an integer and $n^3 + 5$ is odd, then $n$ is even using
> a) a proof by contraposition.
> b) a proof by contradiction.

- a)假设 $n$ 是奇数。则 $n^3+5\equiv1+5\equiv0(\mod 2)$，即 $n^3+5$ 不是奇数，原条件也不成立。故结论成立。
- b)假设 $n$ 是奇数，并且 $n^3+5$ 也是奇数，则 $1\equiv n^3+5\equiv1+5\equiv0(\mod 2)$，矛盾！故结论成立。

#### 1.7.41 G

> Prove that at least one of the real numbers $a_ 1 , a _2 ,\cdots,a_ n$ is greater than or equal to the average of these numbers. What kind of proof did you use?

设这些数的平均值为 $A$，假设结论不成立，即 $a_i<A,i=1,\cdots,n$。由 $A=\frac 1n\sum_{i=1}^na_i<\frac{nA}n=A$，矛盾！故结论成立。

我使用的是归谬法证明。