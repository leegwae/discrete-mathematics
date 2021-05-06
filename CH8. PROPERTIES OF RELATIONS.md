# CH8. PROPERTIES OF RELATIONS

## 8.1 Relations on Sets

- 두 집합의 카티전 곱의 부분집합을 **binary relation**이라고 한다.



### 8.1.1 The Inverse of a Relation

**Definition**

$R$이 $A$부터 $B$까지의 집합이라고 하자. 또한 $R^{-1}$이 $B$부터 $A$까지의 inverse relation이며, 다음과 같다고 하자.
$$
R^{-1}=\{(ymx)\in B\times A|(x,y)\in R\}
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

$A$가 집합이고 $R$이 $A에 대한 relation이라고 하자.$ $R$의 **transitive closure**는 다음의 세 특징을 만족하는 $A$에 대한 relation $R^t$라고 한다.

1. $R^t$는 transitive하다.
2. $R \subseteq R^t$
3. $S$가 $R$을 포함하는 어떠한 relation이든 다른 transitive relation이면, $R^t\subseteq S$



