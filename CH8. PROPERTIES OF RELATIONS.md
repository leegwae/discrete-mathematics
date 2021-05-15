# CH8. PROPERTIES OF RELATIONS

## 8.1 Relations on Sets

- 두 집합의 카티전 곱의 부분집합을 **binary relation**이라고 한다.



### 8.1.1 The Inverse of a Relation

**Definition**

$R$이 $A$부터 $B$까지의 집합이라고 하자. 또한 $R^{-1}$이 $B$부터 $A$까지의 inverse relation이며, 다음과 같다고 하자.
$$
R^{-1}=\{(y,\ x)\in B\times A|(x,y)\in R\}
$$


### 8.1.2 Directed Graph of a Relation

**Definition[Relation]**

집합 $A$에 대한 relation은 $A$부터 $A$까지의 relation이다.



- relation $R$이 집합 $A$에 대한 것으로 정의되면, relation의 arrow diagram은 수정될 수 있어 **directed graph**가 된다.



### 8.1.3 N-ary Relations and Relational Databases

**Definition**

주어진 집합들 $A_1,\ A_2,\ ...,\ A_n$에 대하여, $A_1\times A_2\times ...\times A_n$에 대한 **$n$-ary relation** $R$은 $A_1\times A_2\times ...\times A_n$의 부분집합이다. 2-ary, 3-ary, 4-ary relation은 **binary**, **ternary**, 그리고 **quaternary relations**라고 부른다.



## 8.2 Reflexivity, Symmetry, and Transitivity

**Definition[reflexive, symmetric, transitive]**

$R$이 집합 $A$에 대한 relation이라고 하자.

1. $R$은 모든 $x\in A,\ x\ R\ x$에 대하여, 그리고 오직 이 경우에만 **reflexive**라고 한다.
2. $R$은 모든 $x\in A,\ x\ R\ x$에 대하여 $x\ R\ y$이면 $y\ R\ x$인 경우, 그리고 오직 이 경우에만 **symmetric**하다.
3. $R$은 모든 $x,\ y,\ z\ \in A,\ x\ R\ x$에 대하여 $x\ R\ y$이고 $y\ R\ z$이면 $x\ R\ z$인 경우, 그리고 오직 이 경우에만 **transitive**하다.



**informal terms**

1. **Reflexive**: 각각의 요소가 그 자체와 연관된다.
2. **Symmetric**: 어떤 요소이든지 다른 어떤 요소와 연관된다면, 후자의 요소는 전자의 요소와 연관된다.
3. **Transitive**: 어떤 요소이든지 두번째 요소와 연관되고, 그 두번째 요소가 세번째 요소와 연관되면, 첫번째 요소는 세번째 요소와 연관된다.



### 8.2.1 Properties of Relations on Infinite Sets

**Example 8.2.2 Properties of Equality**
$$
x\ R\ y\quad\Leftrightarrow\quad x=y
$$

1. reflexive

   $x\ R\ x$는 $x=x$를 의미하므로, 이것은 다음을 의미하는 것과 같다.
   $$
   모든\ x\in R,\ x=x
   $$
   따라서 reflexive

2. symmetric

   $R$의 정의에 따라, $x\ R\ y$는 $x=y$를 의미하고 $y\ R\ x$는 $y=x$임을 의미한다. 그러므로 $R$은 다음과 같은 경우 symmetric하다.
   $$
   모든\ x,\ y에\ 대하여,\ x=y이면\ y=x이다.
   $$
   따라서 symmetric

3. transitive

   $R$의 정의에 따라, $x\ R\ y$는 $x=y$를 의미하고 $y\ R\ z$는 $y=z$를, $x\ R\ z$는 $x=z$를 의미한다. 그러므로 $R$은 다음의 문장이 참일 때, 그리고 오직 이 경우에만 transitive하다.
   $$
   모든\ x,y,z\in R에\ 대하여,\ x=y이고\ y=z이면\ x=z이다.
   $$

**Example 8.2.3 Properties of Less Than**(풀어보기)
$$
x\ R\ y\quad\Leftrightarrow\quad x<y
$$

1. reflexive
2. symmetric
3. transitive



### 8.2.2 The Transitive Closure of a Relation

**Definition[Transitive Colsure]**

$A$가 집합이고 $R$이 $A$에 대한 relation이라고 하자.$R$의 **transitive closure**는 다음의 세 특징을 만족하는 $A$에 대한 relation $R^t$라고 한다.

1. $R^t$는 transitive하다.
2. $R \subseteq R^t$
3. $S$가 $R$을 포함하는 어떠한 relation이든 다른 transitive relation이면, $R^t\subseteq S$



## 8.3 Equivalence Relations

### 8.3.1 The Relation Induced by a Partition

집합 $A$의 **partition**은 유한하거나, 합집합이 $A$인 비어있지 않고 mutually disjoint한 부분집합의 무한한 collection이다.



**Definition**

주어진 집합 $A$의 partition에 대하여, **relation induced by the parition** $R$은 $A$에 대해 다음과 같이 정의된다: 모든 $x,\ y\in A$에 대하여,
$$
x\ R\ y\quad\Leftrightarrow\quad x와\ y가\ 모두\ A_i에\ 속하는\ \mathrm{partition}의\ 부분집합\ A_i가\ 있다.
$$


**Theorem 8.3.1**

$A$가 partition을 가진 집합이고, $R$이 relation induced by partition이라고 하자. $R$은 reflexive하고, symmetric하고, transitive하다.

**Proof**: $A$가 partition을 가진 집합이라고 하자. 표기를 단순화하기 위해, partition이 오직 유한한 수의 집합으로 이루어져있다고 생각한다. 유한한 partition에 대한 증명은 표기를 제외하면 동일하다. partition subset을 다음과 같이 표시한다.
$$
A_1,\ A_2,...,\ A_n
$$
$A_i\cap A_j=\varnothing$이며, $i\neq j$이다. 또한 $A_1\cup A_2\cup...\cup A_n=A$이다. relation $R$ induced by the partition은 다음과 같이 정의된다: 모든 $x,\ y\in A$에 대하여,
$$
x\ R\ y\quad\Leftrightarrow\quad x\in A_i\ 그리고\ y\in A_i인\ \mathrm{partition}의\ 부분집합\ A_i가\ 있다.
$$

**$R$ is reflexive:** $x\in A$라고 하자. $A_1,\ A_2,...,\ A_n$는 $A$의 partition이므로, 어떤 $i$에 대하여 $x \in A_i$이므로, 다음의 문장은 참이다.
$$
x\in A_i\ 그리고\ y\in A_i인\ \mathrm{partition}의\ 부분집합\ A_i가\ 있다.
$$

그러므로, $R$의 정의에 의하여, $x\ R\ x$이다.

**$R$ is symmetric:** $x\ R\ y$인 그러한 $A$의 요소인 $x$와 $y$가 있다고 하자. 그러면 $R$의 정의에 의해,
$$
x\in A_i\ 그리고\ y\in A_i인\ \mathrm{partition}의\ 부분집합\ A_i가\ 있다.
$$
위 문장은 참이다. 그러므로, $R$의 정의에 의해, $y\ R\ x$이다.

**$R$ is transitive:** $x,\ y,\ z$이 $A$에 속하고, $x\ R\ y$이고 $y\ R\ z$라고 하자. $R$의 정의에 의해, 다음을 만족하는 partition의 부분집합 $A_i$와 $A_j$가 있다고 하자.
$$
A_i에\ x와\ y가\ 속하고,\ A_j에\ y와\ z가\ 속한다.
$$
 $A_i\neq A_j$라고 하자. 그러면 ${A_1,\ A_2,\ A_3,...,A_n}$가 $A$의 partition이므로 $A_i\cap A_j=\varnothing$이다. 그런데 $y$는 $A_i$에 속하고 $A_j$도 속한다. 그러므로 $A_i\cap A_j\neq\varnothing$이다. 따라서 $A_i=A_j$이다. 그리하여 $x,y,z$가 모두 $A_i$에 속한다. 특히,
$$
x와\ z가\ A_i에\ 속한다.
$$
그러므로 $R$의 정의에 의해 $x\ R\ z$이다.




### 8.3.2 Definition of an Equivalence Relation

**Definition[Equivalence Relation]**

$A$가 집합이고 $R$이 $A$에 대한 relation이라고 하자. $R$은 $R$이 reflexive하고, symmetric하고, transitive한 경우, 그리고 오직 이 경우에만 **equivalence relation**이다.



### 8.3.3 Equivalence Classes of an Equivalence Relation

**Definition**

$A$가 집합이고 $R$이 $A$에 대한 equivalence relation이라고 하자. $A$의 각각의 요소 $a$에 대하여, **$a$의 equivalence class**는 $[a]$로 표기하며 **class of $a$**라고 축약하여 부른다. 이것은 $x$가 $R$에 의하여 $a$와 연관되는 그러한 $A$에 속하는 모든 요소 $x$의 집합이다. 기호화하면:
$$
[a]=\{x\in A|\ x\ R\ a\}
$$


**Lemma 8.3.2**

$A$가 집합이고 $R$이 $A$에 대한 equivalence relation이라고 하자. 또한 $a$와 $b$가 $A$의 요소라고 하자. $a\ R\ b$이면 $[a]=[b]$이다.



**Lemma 8.3.3**

$A$가 집합이고 $R$이 $A$에 대한 equivalence relation이라고 하자. 그러면
$$
[a]\cap [b]=\varnothing\quad 이거나\quad\ [a]=[b]
$$


**Theorem 8.3.4 The partition Induced by an Equivalence Relation**

$A$가 집합이고 $R$이 $A$에 대한 equivalence relation이면, $R$의 distinct equivalence calsses는 $A$의 partition을 구성한다(form); 즉, equivalence classes의 합집합은 $A$의 모든 것이고, 두 개의 distinct classes의 intersection은 empty이다.

**Proof**: ?? 명제 이해하고



**Definition[Representative]**

$R$이 집합 $A$에 대한 equivalence relation이고, $S$가 $R$의 equivalence class라고 하자. class $S$의 **representative**는 $[a]=S$인 모든 요소 $a$이다.



### 8.3.4 Congruence Modulo $n$

**Definition**

$m$과 $n$이 정수이고 $d$가 양수 정수라고 하자. **$m$은 $n$ modulo $d$와 일치한다**고 말할 때 다음과 같이 쓴다.
$$
m\equiv n(\mathrm{mod}\ d)
$$
다음과 같은 경우, 그리고 오직 이 경우에만 그러하다.
$$
d|(m-n)
$$
기호화하면
$$
m\equiv n(\mathrm{mod}\ d)\quad\Leftrightarrow\quad d|(m-n)
$$


### 8.3.5 A Definition for Rational Numbers

**Example 8.3.12 Rational Numbers Are Really Equivalnce Classes**

$A$가 두번째 요소가 nonzero인 정수의 모든 ordered pair라고 하자. 기호화하면:
$$
A=Z\times(Z-\{0\})
$$
$A$에 대한 relation $R$를 다음과 같이 정의한다: $A$에 속하는 모든 pairs $(a,b)$ 그리고 $(c,d)$에 대하여,
$$
(a,b)\ R\ (c,d) \Leftrightarrow\ ad=bc
$$
**Prove**

(1) $R$이 equivlance relation을 증명하라.

(2) $R$의 distinct equivalence classes를 기술하라.



## 8.5 Partial Order Relations

### 8.5.1 Antisymmetry

**Definition**

$R$이 집합 $A$에 대한 relation이라고 하자. $R$은 다음과 같은 경우, 그리고 오직 이 경우에만 **antisymmetric**하다.



$R$은 다음과 같은 경우, 그리고 오직 이 경우에만 ***not*** **antisymmetric**하다.



### 8.5.2 Partial Order Relations

**Definition[Partial Order Relation]**

$R$이 집합 $A$에 대한 relation이라고 하자. $R$은 reflexive, antisymmetric, transitive인 경우, 그리고 오직 이 경우에만 **partial order relation**이다.



**Notation**

- $\preceq$: general partial order relation
- $x\preceq y$: $x$는 $y$보다 작거나 같다. 혹은 $y$는 $x$는 크거나 같다.



### 8.5.3 Lexciographic Order

- $A$가 partial order relation을 가진다면, *dictionary* 혹은 *lexcicographic* order는 다음과 같은 정의로 나타낸 set of strings over $A$로 정의될 수 있다.



**Theorem 8.5.1 Lexicographic Order**

$A$가 partial order relation $R$을 가지는 집합이라고 하고, $S$가 set of strings over $A$라고 하자. $S$에 대한 relation $\preceq$는 다음과 같이 정의한다:

$s$와 $t$가 각각 길이가 $m$과 $n$인 $S$의 string이라고 하자. $m$과 $n$은 양의 정수이다. 그리고 $s_m$과 $t_m$이 $s$와 $t$에 대한 $m$번째 문자라고 하자.

1. $m\le n$이고 $s$와 $y$의 첫음 $m$ 문자가 같다면, $s\preceq t$이다.
2. $s$와 $y$의 처음 $m-1$ 문자가 같으며, $s_m\ R\ t_m$이고 $s_m\neq t_m$이면 $s\preceq t$이다.
3. $\lambda$가 null string이면 $\lambda \preceq s$이다.

이 세 조건 외에 $\preceq$에 의해 연관되는 strings가 없다면, $\preceq$는 $S$에 대한 partial order relation이다.



**Definition**

정리 8.5.1의 partial order relation은 **lexicographic order for $S$**라고 불리며, 이것은 $A$에 대한 partial order $R$에 대응한다.



### 8.5.4 Hasse Diagrams

- Hasse diagram: 모든 유한한 집합에 대해 정의된 partial order relation에 대하여, 다음과 같은 특징이 모두 만족된 directed graph를 간단하게 한 diagram
  - (1) 모든 점들에는 루프가 있다.
  - (2) 모든 화살표는 위쪽을 가리킨다.
  - (3) 화살표가 한 점에서 두번째 점, 두번째 점에서 세번째 점, ㅊ첫번째 점에서 세번째 점까지 있을 때마다 화살표가 있다.

Hasse diagram을 그리는 방법은 다음과 같다: relation의 directed graph에서, 모든 화살표가 위로 가도록 점을 찍는다. 그리고 다음을 제거한다.

1. 모든 점들에 있는 loop
2. transitive property에 의해 존재가 암시된 모든 화살표
3. 화살표의 방향 지시 기호



### 8.5.5 Partially and Totally Ordered Sets

**Definition[Comparable]**

$\preceq$가 집합 $A$에 대한 partial order relation이라고 하자. 집합 $A$의 요소 $a$와 $b$는 $a\preceq b$이거나 $b\preceq a$인 경우, 그리고 오직 이 경우에만 **comparable**하다고 한다. 그렇지 않은 경우, $a$와 $b$는 **nonomparable**하다.



**Definition[Total Order Relation]**

$R$이 집합 $A$에 대해 partial order relation하고, $A$의 두 요소 $a$와 $b$가 $a\ R\ b$하거나 $b\ R\ a$이라면, $R$은 $A$에 대해 **total order relation**이다.



- 집합 $A$는 $\preceq$가 $A$에 대한 partial order relation인 경우, 그리고 오직 이 경우에만 relation $\preceq$에 관하여 **partially ordered set**(혹은 **poset**)이라고 한다.
- 집합 $A$는 $A$가 $\preceq$에 관하여 partially ordered하거나 $\preceq$가 total order인 경우, 그리고 오직 이 경우에만 **totally ordered set**이라고 한다.



**Definition[length of a chain]**

$A$가 relation $\preceq$에 관하여 partially ordered라고 하자. $A$의 부분집합 $B$는 $B$의 각각의 요소의 쌍에 있는 요소가 comparable한 경우, 그리고 오직 이 경우에만 **chain**이라고 한다. 달리 말하여, $B$의 모든 $a$와 $b$에 대하여 $a\preceq b$나 $b\preceq a$이다. **length of a chain(체인의 길이)**는 chain의 요소의 개수보다 한 개 적다.



**Definition**

$A$가 relation $\preceq$에 관하여 partially ordered라고 하자.

1. $A$의 요소 $a$는 $A$의 각각의 요소 $b$에 대하여, $b\preceq a$이거나 $b$와 $a$가 not comparable한 경우, 그리고 오직 이 경우에만 **maximal element of $A$**라고 한다.
2. $A$의 요소 $a$는 $A$의 각각의 요소 $b$에 대하여, $b\preceq a$인 경우, 그리고 오직 이 경우에만 **greatest element of $A$**라고 한다.
3. $A$의 요소 $a$는 $A$의 각각의 요소 $b$에 대하여, a$\preceq b$이거나 $b$와 $a$가 not comparable한 경우, 그리고 오직 이 경우에만 **minimal element of $A$**라고 한다
4. $A$의 요소 $a$는 $A$의 각각의 요소 $b$에 대하여, $a\preceq b$인 경우, 그리고 오직 이 경우에만 **least element of $A$**라고 한다.



### 8.5.6 Topological Sorting

**Definition[Compatible]**

주어진  집합 $A$에 대한 partial order relation $\preceq$와 $\preceq^\prime$에 대하여, $\preceq^\prime$은 $A$의 모든 $a$와 $b$에 대해 $a\preceq b$이라면 $a\preceq^\prime b$인 경우, 그리고 오직 이 경우에만 $\preceq$와 **compatible**하다.



**Definition[Topological Sorting]**

주어진  집합 $A$에 대한 partial order relation $\preceq$와 $\preceq^\prime$에 대하여, $\preceq ^ \prime$은 $\preceq^\prime$이 $\preceq$와 compatible한 total order인 경우, 그리고 오직 이 경우에만 **topological sorting**이다.



**Construting a Topological Sorting**

$\preceq$가 비어있지 않고 유한한 집합 $A$에 대한 partial order이라고 하자. topological sorting을 구성하려면,

1. 모든 minimal element $x$를 $A$에서 찾아라.
2. 집합 $A^\prime:=A-\{x\}$이다.
3. $A\prime \neq \varnothing$인 동안 다음 단계들을 반복한다.
   1. $A^\prime$에서 모든 minimal element를 찾아라.
   2. $x\preceq ^\prime y$를 정의하라.
   3. 집합 $A:=A^\prime -{y}$그리고 $x:=y$



### 8.5.7 An Application



### 8.5.8 PERT and CPM

- PERT(Program Evalutaion and Review Technique)
- CPM(Critical Path Method)





