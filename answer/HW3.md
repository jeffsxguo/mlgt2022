> Mathematical Logic and Graph Theory 2022 Homework 3 Answers
>
> By [Jingyi Chen](chenjingyi071@mail.ustc.edu.cn) with C and [Songxiao Guo](logname@mail.ustc.edu.cn) with G after each question number.

[TOC]

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



#### 2.2.19 G

>Show that if $A$, $B$, and $C$ are sets, then $A ∩ B ∩ C = A ∪B ∪ C$
>a) by showing each side is a subset of the other side.
>b) using a membership table.

#### 2.2.35 G

>Let $A$, $B$, and $C$ be sets. Use the identities in Table 1 to show that $(A ∪ B) ∩ (B ∪ C) ∩ (A ∪ C) = A ∩ B ∩ C$.

#### 2.2.47 C

>Suppose that $A$, $B$, and $C$ are sets such that $A ⊕ C =B ⊕ C$. Must it be the case that $A = B$?

#### 2.3.3 C

>Determine whether $f$ is a function from the set of all bit strings to the set of integers if
>a) $f (S)$ is the position of a $0$ bit in $S$.
>b) $f (S)$ is the number of $1$ bits in $S$.
>c) $f (S)$ is the smallest integer $i$ such that the $i$th bit of $S$ is $1$ and $f (S) = 0$ when $S$ is the empty string, the string with no bits.

#### 2.3.21 C

>Give an explicit formula for a function from the set of integers to the set of positive integers that is
>a) one-to-one, but not onto.
>b) onto, but not one-to-one.
>c) one-to-one and onto.
>d) neither one-to-one nor onto.

#### 2.3.37 C

>If $f$ and $f ◦g$ are onto, does it follow that $g$ is onto? Justify your answer.

#### 2.4.27 C

>Show that if $a_n$ denotes the $n$th positive integer that is not a perfect square, then $a_n = n + \{\sqrt n\}$, where $\{x\}$ denotes the integer closest to the real number $x$.

#### 2.5.11 C

>Give an example of two uncountable sets $A$ and $B$ such that $A ∩ B$ is
>a) ﬁnite.
>b) countably inﬁnite.
>c) uncountable.

#### 2.5.17 C

>If $A$ is an uncountable set and $B$ is a countable set, must $A − B$ be uncountable?

#### 2.5.37 C

>Show that the set of all computer programs in a particular programming language is countable.