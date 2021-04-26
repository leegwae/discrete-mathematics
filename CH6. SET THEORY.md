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

