# CH9. COUNTING AND PROBABILITY

## 9.1 Introduction to Probability

- **random**: 프로세스가 실행될 때, outcome의 집합으로부터 한 outcome가 생성되는 것은 확실하지만, 어떠한 outcome인지 확실히 예측할 수 없다.



**Definition[sample space]**

**sample space**는 random 프로세스나 경험으로부터 얻을 수 있는 모든 가능한 결과의 집합이다. **event**는 sample space의 집합이다.



**Equally Likely Probability Formula**

$S$가 모든 결과가 동일한 가능성을 가지는 유한한 sample space이고 $E$가 $S$에 속하는 event일 때, **E**의 **probability**는 $P(E)$로 표기하며
$$
P(E)=\frac{E에\ 속하는\ 결과의\ 개수}{S에\ 속하는\ 결과의\ 총개수}
$$



**Notation[N(A)]**

유한한 집합 $A$에 대하여, $N(A)$는 $A$의 요소의 개수를 표기한다.


$$
P(E)=\frac{N(E)}{N(A)}
$$



### 9.1.1 Counting the Elements of a List

**Theorem 9.1.1 The Number of Elements in a List**

$m$과 $n$이 정수이고 $m\le n$이면, $m$부터 $n$까지 $n-m+1$개의 정수가 있다.



## 9.2 Possibility Tress and the Multiplication Rule

### 9.2.1 The Multiplication Rule

**Theorem 9.2.1 The Multiplication Rule**

연산이 $k$개의 단계로 이루어져있고,

첫번째 단계가 $n_1$에서 수행되고

두번째 단계가 $n_2$에서 수행되고 ...

$k$번째 단계가 $n_k$에서 수행된다면,

전체 연산은 $n_1n_2n_3...n_k$에서 이루어질 수 있다.



### 9.2.2 When the Multiplication Rule Is Difficult or Impossible to Apply



### 9.2.3 Permutations

**Theorem 9.2.2**

$n\ge 1$인 모든 정수 $n$에 대하여, $n$개의 요소로 이루어진 집합의 순열의 수는 $n!$이다.



### 9.2.4 Permutations of Selected Elements

**Definition[$r$-permutation]**

$n$개의 element를 가진 집합의 **$r$-permutation**은 $n$개의 element를 가진 집합으로부터 $r$개의 element를 순서를 가지고 택하는 것이다. $n$개의 element를 가진 집합의 **$r$-permutation**의 수는 $P(n,r)$로 표기한다.



**Theorem 9.2.3**

$n$과 $r$이 정수이고 $1\le r \le n$이면, $n$개의 요소를 가진 집합의 $r$-permutation의 수는 다음의 공식으로 얻을 수 있다.
$$
P(n,r)=n(n-1)(n-2)...(n-r+1)
$$
이는 다음과 같다.
$$
P(n-r)=\frac{n!}{(n-r)!}
$$




## 9.3 Counting Elements of Disjoint Sets: The Addition Rule

**Theorem 9.3.1 The Addition Rule**

유한한 집합 $A$가 $k$개의 distinct mutually disjoint subset $A_1, A_2, ..., A_k$의 합집합(union)이라고 한다.
$$
N(A)=N(A_1)+N(A_2)+...+N(A_k)
$$


### 9.3.1 The Difference Rule

**Theorem 9.3.2 The Difference Rule**

$A$가 유한 집합이고 $B$가 $A$의 부분집합이면,
$$
N(A-B)=N(A)-N(B)
$$


**Formula for the Probabiality of the Complements of an Event**

$S$가 finite sample space이고 $A$가 $S$에 속하는 사건(event)이면, $S$에 속하는 $A$의 여집합 $A^c=S-A$에 대하여
$$
P(A^c)=1-P(A)
$$


### 9.3.2 The Inclusion/Exculsion Rule

**Theorem 9.3.3 The Inclusion/Exclusion Rule for Two or Three Sets**

$A$, $B$, $C$가 유한 집합이면, 다음 두 가지가 성립한다.
$$
N(A\cup B) = N(A)+N(B)-N(A\cap B) \\
N(A\cup B\cup C) = N(A)+N(B)+N(C)-N(A\cap B)-N(A\cap C) - N(B\cap C) + N(A\cap B\cap C)
$$
