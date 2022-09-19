> Mathematical Logic and Graph Theory 2022 Homework 3 Answers
>
> By [Jingyi Chen](chenjingyi071@mail.ustc.edu.cn) with C and [Songxiao Guo](logname@mail.ustc.edu.cn) with G after each question number.

[TOC]

#### 1.8.5 C

假设$x\geq y$，则$max(x,y)=x,min(x,y)=y$；假设$x\leq y$，则$max(x,y)=y,min(x,y)=x$，$\therefore x+y=max(x,y)+min(x,y)$。

#### 1.8.13 C

8和9。

#### 2.1.11 G

>Determine whether each of these statements is true or false.
>a) $0 ∈ ∅$
>b) $∅ ∈ \{0\}$
>c) $\{0\} ⊂ ∅$
>d) $ ∅ ⊂ \{0\}$
>e) $\{0\} ∈ \{0\}$
>f ) $\{0\} ⊂ \{0\}$
>g) $\{∅\} ⊆ \{∅\}$

- a) F
- b) F
- c) F
- d) T
- e) F
- f) F
- g) T

#### 2.1.27 G

> Prove that $\mathcal P(A) ⊆ \mathcal P(B)$ if and only if $A ⊆ B$.

- 充分性：已知 $A\subseteq B$，对 $\forall x\in\mathcal P(A)$，有 $x\subseteq A\subseteq B$，故有 $x\in \mathcal P(B)$。由 $x$ 的任意性得 $\mathcal P(A)\subseteq \mathcal P(B)$.
- 必要性：已知 $\mathcal P(A)\subseteq\mathcal P(B)$，对 $\forall x\in A$，有 $\{x\}\in\mathcal P(A)\subseteq\mathcal P(B)$，故有 $x\in B$。由 $x$ 的任意性得 $A\subseteq B$.

#### 2.1.41 G

> Explain why $A × B × C$ and $(A × B) × C$ are not the same.

$$
A\times B\times C=\{(a,b,c)|a\in A,b\in B,c\in C\},\\
(A\times B)\times C=\{((a,b),c)|a\in A,b\in B,c\in C\}.
$$

#### 2.1.43 G

>Prove or disprove that if $A$ and $B$ are sets, then $\mathcal P(A × B) =\mathcal P(A) × \mathcal P(B)$.

结论错误。设 $A=B=\empty$，则 $\mathcal P(A\times B)=\{\empty\}$，$\mathcal P(A)\times\mathcal P(B)=\{(\empty,\empty)\}$，二者明显不相等。

#### 2.1.49 G

>The deﬁning property of an ordered pair is that two ordered pairs are equal if and only if their ﬁrst elements are
>equal and their second elements are equal. Surprisingly, instead of taking the ordered pair as a primitive concept, we can construct ordered pairs using basic notions from set theory. Show that if we deﬁne the ordered pair $(a, b)$ to be $\{\{a\}, \{a, b\}\}$, then $(a, b) = (c, d)$ if and only if $a = c$ and $b = d$. 

- 充分性：已知 $a=c,b=d$ 时，$\{\{a\},\{a,b\}\}=\{\{c\},\{c,d\}\}$ 显然成立。
- 必要性：已知 $\{\{a\},\{a,b\}\}=\{\{c\},\{c,d\}\}$ 时，
  - $a=b$，则 $\{\{a\},\{a,b\}\}=\{a\}$，$\{\{c\},\{c,d\}\}=\{c\}$，即已知 $\{a\}=\{c\}$，便有 $a=c$，推知 $b=d$。
    - $a\neq b$，则 $\{\{a\},\{a,b\}\}$ 是二元集，含有一个一元集和一个二元集。两集合相等，故 $\{\{c\},\{c,d\}\}$ 也含有一个一元集和一个二元集。这样便有 $c\ne d$。故 $\{a\}=\{c\}\Rightarrow a=c$。又$\{a,b\}=\{c,d\}$，易得 $b=d$。

#### 2.2.19 G

>Show that if $A$, $B$, and $C$ are sets, then $\overline{A ∩ B ∩ C} = \overline A ∪\overline B ∪ \overline C$
>a) by showing each side is a subset of the other side.
>b) using a membership table.

- a) 
  $$
  \begin{align}
  x\in \overline{A ∩ B ∩ C} &\equiv x\in \overline A ∪\overline B ∪ \overline C\\
  &\equiv x\notin A\or x\notin B\or x\notin C\\
  &\equiv x\in \overline A\or x\in\overline B\or x\in\overline C\\
  &\equiv x\in \overline A ∪\overline B ∪ \overline C.
  \end{align}
  $$

- 

| $A$  | $B$  | $C$  | $A\cap B\cap C$ | $\overline {A\cap B\cap C}$ | $\overline A$ | $\overline B$ | $\overline C$ | $\overline A ∪\overline B ∪ \overline C$ |
| :--: | :--: | :--: | :-------------: | :-------------------------: | :-----------: | :-----------: | :-----------: | :--------------------------------------: |
|  1   |  1   |  1   |        1        |              0              |       0       |       0       |       0       |                    0                     |
|  1   |  1   |  0   |        0        |              1              |       0       |       0       |       1       |                    1                     |
|  1   |  0   |  1   |        0        |              1              |       0       |       1       |       0       |                    1                     |
|  1   |  0   |  0   |        0        |              1              |       0       |       1       |       1       |                    1                     |
|  0   |  1   |  1   |        0        |              1              |       1       |       0       |       0       |                    1                     |
|  0   |  1   |  0   |        0        |              1              |       1       |       0       |       1       |                    1                     |
|  0   |  0   |  1   |        0        |              1              |       1       |       1       |       0       |                    1                     |
|  0   |  0   |  0   |        0        |              1              |       1       |       1       |       1       |                    1                     |

#### 2.2.35 G

>Let $A$, $B$, and $C$ be sets. Use the identities in Table 1 to show that $\overline{(A ∪ B)} ∩\overline{ (B ∪ C)} ∩\overline{ (A ∪ C)} = \overline A ∩ \overline B ∩\overline C$.

$$
\begin{align}
\overline{(A ∪ B)} ∩\overline{ (B ∪ C)} ∩\overline{ (A ∪ C)} 
&=\overline A\cap\overline B\cap\overline B\cap\overline C\cap\overline A\cap\overline C& 德\cdot 摩根律\\
&=\overline A\cap(\overline B\cap\overline B)\cap\overline C\cap\overline A\cap\overline C&结合律\\
&=\overline A\cap\overline B\cap\overline C\cap\overline A\cap\overline C&幂等律\\
&=\overline A\cap\overline B\cap(\overline C\cap\overline A)\cap\overline C&结合律\\
&=\overline A\cap\overline B\cap(\overline A\cap\overline C)\cap\overline C&交换律\\
&=\overline A\cap\overline B\cap\overline A\cap(\overline C\cap\overline C)&结合律\\
&=\overline A\cap\overline B\cap\overline A\cap\overline C&幂等律\\
&=\overline B\cap\overline A\cap\overline A\cap\overline C&交换律\\
&=\overline B\cap(\overline A\cap\overline A)\cap\overline C&结合律\\
&=\overline B\cap\overline A\cap\overline C&幂等律\\
&=\overline A\cap\overline B\cap\overline C&交换律.
\end{align}
$$

#### 2.2.47 C

>Suppose that $A$, $B$, and $C$ are sets such that $A ⊕ C =B ⊕ C$. Must it be the case that $A = B$?

是的。

对$\forall x\in A$，如果$x\in C$则有$x\notin A\oplus C$，因此$x\notin B\oplus C$，从而$x\in B$；

如果$x\notin C$则有$x\in A\oplus C$，因此$x\in B\oplus C$，从而$x\in B$；

对$\forall x\in B$，同理有$x\in A$，所以$A=B$。

#### 2.3.3 C

>Determine whether $f$ is a function from the set of all bit strings to the set of integers if
>a) $f (S)$ is the position of a $0$ bit in $S$.
>b) $f (S)$ is the number of $1$ bits in $S$.
>c) $f (S)$ is the smallest integer $i$ such that the $i$th bit of $S$ is $1$ and $f (S) = 0$ when $S$ is the empty string, the string with no bits.

a) 不是，因为“某个0”的位置是不确定的。

b)是的，1的个数由S确定。

c)是的，i的只由S确定。

#### 2.3.21 C

>Give an explicit formula for a function from the set of integers to the set of positive integers that is
>a) one-to-one, but not onto.
>b) onto, but not one-to-one.
>c) one-to-one and onto.
>d) neither one-to-one nor onto.

a)例如$f(x)=3x+1(x\geq 0),f(x)=-3x+2(x<0)$。

b)例如$f(x)=|x|+1$。

c)例如$f(x)=2x+1(x\geq 0),f(x)=-2x(x<0)$。

d)例如$f(x)=x^2+1$。

#### 2.3.37 C

>If $f$ and $f ◦g$ are onto, does it follow that $g$ is onto? Justify your answer.

不一定，比如A={a},B={b,c},C={d},g(a)=b,f(b)=d,f(c)=d。类似这样构造一个中间的较大的集合和两侧较小的集合，使得g不能映上即可。

#### 2.4.27 C

>Show that if $a_n$ denotes the $n$th positive integer that is not a perfect square, then $a_n = n + \{\sqrt n\}$, where $\{x\}$ denotes the integer closest to the real number $x$.

把正整数分成两部分，一部分是完全平方数$1^2,2^2,...,k^2$，另一部分是去掉完全平方数后的序列$a_1,a_2,...,a_n$，这时$k^2<n+k<(k+1)^2$，

即$(k-1/2)^2+3/4=k^2-k+1\leq n\leq(k+1/2)^2-1/4$，

因此$k=\left\{\sqrt n\right\}$，$a_n=n+\left\{\sqrt n\right\}$。

#### 2.5.11 C

>Give an example of two uncountable sets $A$ and $B$ such that $A ∩ B$ is
>a) ﬁnite.
>b) countably inﬁnite.
>c) uncountable.

a)例如$A=[0,1], B=[2,3],$ 直接没交集。

b)例如$A=[0,1]\cup Z,B=[2,3]\cup Z$，交集把不可数的去掉了。

c)例如$A=B=[0,1]$，交集有一段不可数的即可。

#### 2.5.17 C

>If $A$ is an uncountable set and $B$ is a countable set, must $A − B$ be uncountable?

是的。如果A-B可数，则$(A-B)+(A\cap B)=A$可数；A不可数，所以A-B不可数。

#### 2.5.37 C

>Show that the set of all computer programs in a particular programming language is countable.

例如这个程序只能使用80种不同符号，我们将它们记为101,102，...，180，然后对于一个程序，我们分析其符号串并产生对应的一个数字串，这样就映射到了自然数的子集。自然数是可数集，因此所有程序的集合也是可数集。