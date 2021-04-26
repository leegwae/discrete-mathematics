# CH6. SET THEORY

## 6.1 Set Theory: Definitions and the Element Method of Proof

$$
A=\{x\in S|P(x)\}
$$

$A$는 $x$의 $P$를 참이게 하는 $S$의 모든 $x$의 집합이다.



### 6.1.1 Subsets: Proof and Disproof

집합 $A$가 집합 $B$의 부분집합임을 formal universal conditional statement로 쓸 수 있다.
$$
A\subseteq B\Leftrightarrow \forall x,\ x\in A이면\ x\in B
$$
부정은 existential로 쓸 수 있다.
$$
A\nsubseteq B\Leftrightarrow \exists x\ 그러한\ x\in A이고\ x\in B가\ 있다.
$$
집합의 진부분집합은 그것의 containing set과 같지 않다. 즉:
$$
\begin{align*}
&A는\ B의\ 진부분집합이다.\Leftrightarrow \\
&(1)\ A\subseteq B\\
&(2)\ B의\ 요소\ 중\ 적어도\ 하나가\ A에\ 속하지\ 않았다.
\end{align*}
$$


**Element Argument: The Basic Method for Proving That One Set is a Subset of Another**

주어진 집합 $X,Y$가 있다. $X\subseteq Y$임을 증명하려면,

1. $x$가 $X$의 특정 요소이지만 임의로 선택된 요소라고 **가정한다**
2. $x$가 $Y$의 요소임을 **보인다**



### 6.1.2 Set Equality

**Definition[equals]**

주어진 집합 $A$와 $B$에 대하여, $A$는 $B$와 **동일하다(equals)**는 $A=B$라고 쓰며, $A$의 모든 요소가 $B$에 속하고 $B$의 모든 요소가 $A$에 속하는 경우, 그리고 오직 이 경우에만 그렇하다. 기호화하면,
$$
A=B\Leftrightarrow A\subseteq B\ 그리고\ B\subseteq A
$$


### 6.1.3 Venn Diagrams



### 6.1.4 Operations on Sets

어떤 상황에서, 모든 집합이 실수의 집합으로 여길 수 있을 때 실수의 집합은 **universal set(전체 집합)** 또는 **universe of discourse**라고 부르겠다.

**Definition[union, intersection, difference, complement]**

$A$와 $B$가 가 전체 집합 $U$의 부분집합이라고 하자.

1. $A$와 $B$의 **union(합집합)**은 $A\cup B$라고 표기하며, 적어도 $A$와 $B$ 중 하나에 속하는 모든 요소의 집합이다.
2. $A$와 $B$의 **intersection(교집합)**은 $A\cap B$라고 표기하며, $A$와 $B$에 모두 공통인 모든 요소의 집합이다.
3. $B$에서 $A$의 차 집합은 (혹은 $B$안의 $A$의 **relative compelement**)는 $B-A$로 표기하며, $B$에는 있지만 $A$에 있지 않은 모든 요소의 집합이다.
4. $A$의 **complement(여집합)**은 $A^c$로 표기하며, $A$에 속하지 않는 $U$의 모든 집합이다. 

기호화하면,
$$
\begin{align*}
A\cup B&=\{x\in U|\ x\in A\ 혹은\ x\in B\} \\
A\cap B&=\{x\in U|\ x\in A\ 그리고\ x\in B\} \\
B-A&=\{x\in U|\ x\in B\ 그리고\ x\notin A\} \\
A^c&=\{x\in U|\ x\notin A\} \\
\end{align*}
$$


**Interval Notation**

주어진 실수 $a$와 $b$가 $a\le b$에 대하여:
$$
\begin{align*}
(a,b)&=\{x\in R|\ a<x< b\}	&(a,b)=\{x\in R|\ a\le x\le b\} \\
(a,b]&=\{x\in R|\ a<x\le b\}	&(a,b]=\{x\in R|\ a\le x< b\}
\end{align*}
$$
기호 $\infty$와 $-\infty$는 왼쪽이나 오른쪽으로 제한되지 않은 간격을 나타내는데 사용한다.
$$
\begin{align*}
(a,\infty)&=\{x\in R|x>a\} &(a,\infty]=\{x\in R|x\ge a\} \\
(-\infty, b)&=\{x\in R|x<b\} &(-\infty, b]=\{x\in R|x\le b\} \\
\end{align*}
$$


**Definition[Unions and Intersections of an Indexed Collection of Sets]**

주어진 집합 $A_0,A_1,A_2...$이 전체 집합 $U$의 부분집합이고 $n$이 nonnegative 정수라고 할 때,
$$
\begin{align*}
\bigcup_{i=0}^{n}A_i&=\{x\in U|x\in A_i(i=0,1,2,...,중\ 적어도\ 하나에\ 대하여)\} \\
\bigcup_{i=0}^{\infty}A_i&=\{x\in U|x\in A_i(적어도\ 하나의\ \mathrm{nonnegative}\ 정수\ i에\ 대하여)\} \\
\bigcap_{i=0}^{n}A_i&=\{x\in U|x\in A_i(모든\ i=0,1,2,...,n에\ 대하여)\} \\
\bigcap_{\infty}^{\infty}A_i&=\{x\in U|x\in A_i(모든\ \mathrm{nonnegative}\ 정수\ i에\ 대하여)\} \\
\end{align*}
$$


### 6.1.5 Empty Set

요소가 하나도 없는 집합은 유일하며, **empty set**(혹은 **null set; 공집합**)이라고 부른다. $\varnothing$으로 표기한다.



### 6.1.6 Paritions of Sets

**Definition[disjoint]**

두 집합은 공통으로 가지는 요소가 하나도 없는 경우, 그리고 오직 이 경우에만 **disjoint**하다고 한다. 기호화하면,
$$
A와\ B\ 는\ \mathrm{disjoint}하다.\Leftrightarrow A\cap B=\varnothing
$$


**Definition[mutually disjoint]**

집합 $A_1,A_2,A_3...$은 어떤 서로 다른 두 개의 집합 $A_i$과 $A_j$도 공통으로 요소를 가지지 않는 경우, 그리고 오직 이 경우에만 **mutually disjoint**(혹은 **pairwise disjoint** 혹은 **nonoverlapping**)하다. 더 정확히 말해, 모든 정수 $i,j=1,2,3,...$에 대하여,
$$
A_i\cap A_j=\varnothing\quad(i\ne j)
$$




**Definition[parition]**

공집합이 아닌 집합의 무한하거나 무한하지 않은 collection $\{A_1,A_2,A_3...\}$는 다음과 같은 경우, 그리고 오직 이 경우에만 집합 $A$의 **partition**이다.

1. $A$는 모든 $A_i$의 합집합이다.
2. 집합 $A_1,A_2,A_3...$은 mutually disjoint하다.



### 6.1.7 Power Sets

**Definition[power set]**

주어진 집합 $A$에 대하여, $A$의 **power set(멱집합)**은 $\mathscr{P}(X)$로 표기하며, $A$의 모든 부분집합의 집합이다.



## 6.2 Properties of Sets

**Theorem 6.2.1 [Some Subset Relations]**

1. Inclusion of Intersection: 집합 $A$와 $B$에 대하여,
   $$
   (a)\ A\cap B\subseteq A\quad 그리고\quad (b)\ A\cap B\subseteq B
   $$
   

2. Inclustion in Union: 집합 $A$와 $B$에 대하여,

$$
(a)\ A\subseteq A \cup B\quad (b)\ B\subseteq A\cup B
$$

3. Transitivie Property of Subsets: 집합 $A$, $B$, 그리고 $C$에 대하여,
   $$
   A\subseteq B\ 그리고\ B\subseteq C이면,\ A\subseteq C
   $$



**Procedural Versions of Set Definitions**

$X$와 $Y$가 전체 집합 $U$의 부분집합이며 $x$가 $y$가 $U$의 요소라고 하자.
$$
\begin{align*}
1.&\ x\in X\cup Y\Leftrightarrow x\in X\ 혹은\ x\in Y \\
2.&\ x\in X\cap Y\Leftrightarrow x\in X\ 그리고\ x\in Y \\
3.&\ x\in X- Y\Leftrightarrow x\in X\ 그리고\ x\notin Y \\
4.&\ x\in X^c\Leftrightarrow x\notin X \\
5.&\ (x,y)\in X\times Y \Leftrightarrow x\in X\ 그리고\ y\in Y
\end{align*}
$$


### 6.1 Proving a Subset Relation

*Starting Point*: $A$와 $B$가 집합이라고 하자.

*To Show*: $A\cap B\subseteq A$
$$
\forall x,\ x\in A\cap B이면,\ x\in A이다.
$$
먼저, $x$가 $A\cap B$의 요소라고 **가정한다.** 그리고 $x$가 $A$에 속함을 **보인다.**



### 6.2 Set Indentities

**Theorem 6.2.2 [Set Identities]**

아래의 모든 집합이 전체 집합 $U$의 부분집합이라고 하자.

1. *Commuatiative Laws*: 집합 $A$와 $B$에 대하여,

$$
(a)\ A\cup B=B\cup A\quad그리고\ (b)\ A\cap B=B\cap A
$$

2. *Associative Laws*: 집합 $A, B,C$에 대하여,
   $$
   \begin{align*}
   (a)&\ (A\cup B)\cup C=A\cup(B\cup C)\ 그리고\\
   (b)&\ (A\cap B)\cap C=A\cap(B\cap C)
   \end{align*}
   $$
   

3. *Distributive Laws*: 집합 $A,B,C$에 대하여,
   $$
   \begin{align*}
   (a)&\ A\cup (B\cap C)=(A\cup B)\cap(A\cup C)\ 그리고\\
   (b)&\ A\cap (B\cup C)=(A\cap B)\cup(A\cap C)
   \end{align*}
   $$
   

4. *Identity Laws*: 집합 $A$에 대하여,
   $$
   (a)\ A\cup\varnothing=A\quad그리고\quad(b)\ A\cap U=A
   $$
   

5. *Complement Laws*: 집합 $A$에 대하여,
   $$
   (a)\ A\cup A^c=U\quad 그리고\quad (b)\ A\cap A^c=\varnothing
   $$
   

6. *Double Complement Law*: 집합 $A$에 대하여,
   $$
   (A^c)^c=A
   $$
   

7. *Idempotent Laws*: 집합 $A$에 대하여,
   $$
   (a)\ A\cup A=A\quad그리고\quad(b)\ A\cap A =A
   $$
   

8. *Universal Bound Laws*: 집합 $A$에 대하여,
   $$
   (a)\ A\cup U=U\quad그리고\quad(b)\ A\cap\varnothing=\varnothing
   $$
   

9. *De Morgan's Laws*: 집합 $A$와 $B$에 대하여,
   $$
   (a) (A\cup B)^c=A^c\cap B^c\quad그리고\quad(b)\ (A\cap B)^c=A^c\cup B^c
   $$

10. *Absorption Laws*: 집합 $A$와 $B$에 대하여,
    $$
    (a)\ A\cup(A\cap B)=A\quad그리고\quad(b)\ A\cap(A\cup B)=A
    $$

11. *Complements of $U$ and $\varnothing$*:
    $$
    (a)\ U^c=\varnothing\quad그리고\quad(b)\varnothing^c=U
    $$
    

12. *Set Difference Law*: 집합 $A$와 $B$에 대하여,
    $$
    A-B=A\cap B^c
    $$



**Basic Method for Proving That Sets Are Equal**

집합 $X$와 $Y$가 주어졌을 때, $X=Y$를 증명하려면,

1. $X\subseteq$ Y을 증명하라.
2. $Y\subseteq X$을 증명하라.



**Theorem 6.2.2(3)(a) A Distributive law for Sets**



**Theorem 6.2.2(9)(a) A De Morgan’s law for Sets**

집합 $A$와 $B$에 대하여, $(A\cup B)^c=A^c\cap B^c$

**Proof**: $A$와 $B$가 집합이라고 하자.

**$(A\cup B)^c=A^c\cap B^c$임을 증명하라:**

$x\in(A\cup B)^c$라고 가정하자. complement의 정의에 의하여,
$$
x\notin A\cup B
$$
한편 $x\in A\cup B$는 다음을 뜻한다.
$$
x가\ A에\ 속하거나\ x가\ B에\ 속하는\ 것은\ 거짓이다.
$$
드 모르간의 법칙에 의하여, 이것은 다음을 암시한다.
$$
x\ 가\ A에\ 속하지\ 않고,\ x가\ B에\ 속하지\ 않는다.
$$
또한 다음과 같이 쓸 수 있다.
$$
x\notin A\quad x\notin B
$$
따라서 complement의 정의에 의해 $x\in A^c$이고 $x\in B^c$이다. intersection의 정의에 의해, $x\in A^c\cap B^c$이다. 그러므로 부분집합의 정의에 의해 $(A\cup B)^c\subseteq A^c\cap B^c$이다.

**$A^c \cap B^c \subseteq (A\cup B)^c$을 증명하라:**

$x\in A^c\cap B^c$이라고 가정하자. intersection의 정의에 의하여, $x\in A^c$ 그리고 $x\in B^c$이며, complement의 정의에 의해,
$$
x\notin A\quad그리고\ x\notin B
$$
달리 말하여,
$$
x는\ A에\ 속하지\ 않으며,\ x는\ B에\ 속하지\ 않다.
$$
드 모르간의 법칙에 의하여, 이것은 다음을 암시한다.
$$
x\ 가\ A에\ 속하지\ 않고,\ x가\ B에\ 속하지\ 않는다.
$$
이는 union의 정의에 의하여 다음과 같이 쓸 수 있다.
$$
x\notin A\cup B
$$
그러나, complement의 정의에 의해, $x\in (A\cup B)^c$이다. 부분집합의 정의에 의해 $A^c\cap B^c \subseteq (A\cup B)^c$이다.



**Theorem 6.2.3 Intersection and Union with a Subset**

집합 $A$와 $B$에 대하여, $A\subseteq B$라면,
$$
(a)\ A\cap B=A\quad(b) A\cup B=B
$$
**Proof**

**Part(a):** $A$와 $B$가 $A\subseteq B$인 집합이라고 가정하자. (a)를 증명하려면 $A\cap B\subseteq A$이고 $A\subseteq A\cap B$임을 보여야한다. $A\cap B \subseteq A$는 inclusion of intersection property에 의해 증명되었다. $A\subseteq A\cap B$를 보이려면, $x$가 $A$의 요소임을 가정하자. $A\subseteq B$라고 가정하였으므로, $x$는 부분집합의 정의에 의하여 $B$의 요소이기도 하다. 그러므로.
$$
x\in A\quad그리고\quad x\in B
$$
그러므로 intersection의 정의에 의하여
$$
x\in A\cap B
$$


**Proof:**

**Part(b)** 해봐라.



### 6.3 The Empty Set

**Theorem 6.2.4 [A Set with No Elements Is a Subset of Every Set]**

$E$가 요소가 없는 집합이며, $A$가 집합이면, $E\subseteq A$라고 하자.

**Proof(by cotradiction)**: 부정을 취해보자. 요소가 없는 집합 $E$와 집합 $A$가 $E\subseteq A$라고 하자. 그러면 부분집합의 정의에 의해 $A$의 요소가 아닌 $E$의 요소가 있다. 그러나 $E$가 요소 없는 집합이므로 그러한 요소가 없다. 이는 모순이다.



**Corollary 6.2.5 Uniqueness of the Empty Set**

요소가 없는 집합은 유일하다.

**Proof**: $E_1$과 $E_2$가 요소가 없는 집합이라고 하자. Theorem 6.2.4에 의해, $E_1$은 요소가 없으므로 $E_1\subseteq E_2$이다. 또한 $E_2$는 요소가 없으므로 $E_2\subseteq E_1$이다. 그러므로 set equality의 정의에 의해 $E_1=E_2$이다.



**Element Method for Proving a Set Equals the Empty Set**

집합 $X$가 공집합 $\varnothing$과 같다는 것을 증명하려면, $X$가 요소가 없다는 것을 증명하면 된다. 이를 위해, $X$가 요소가 있다고 가정하여 모순을 이끌어낸다.



**Proposition 6.2.6**

집합 $A,B,C$에 대하여, $A\subseteq B$이고 $B\subseteq C^c$이면, $A\cap C=\varnothing$이다.

**Proof:** $A, B, C$가 $A\subseteq B$이고 $B\subseteq C^c$인 집합이라고 가정하자. $A\cap C=\varnothing$이 아니라고 가정하자. 즉, $A\cap C$에 속하는 요소 $x$가 있다고 하자. intersection의 정의에 의해, $x\in A$이고 $x\in C$이다. 그러면, $A\subseteq B$이므로, 부분집합의 정의에 의해 $x\in B$이다. 또한, $B\subseteq C^c$이므로, 부분집합의 정의에 의해 $X\in C^c$이다. complement의 정의에 의해 $x\notin C$임이 도출된다. 그러므로 $x \in C$이고 $x\notin C$이며, 이것은 모순이다. 따라서 $A\cap C$에 속하는 요소 $x$가 있다는 가정은 거짓이며, 따라서 $A\cap C=\varnothing$이다.

