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


## 9.4 The Pigeonhole Principle

**The Pigeonghole Principle**

하나의 유한한 집합부터 그보다 작은 유한한 집합의 함수는 일대일(one-to-one)일 수 없다: 적어도 두 개의 요소가 co-comain 안에서 동일한 image를 가지는 domain 안에 존재한다(There must  be at least two elements in the domain that have the same image in the co-domain.).



### 9.4.1 Application to Decimal Expansions of Fractions



### 9.4.2 Generalized Pigeonhole Principle

**Generalized Pigeonhole Principle**

요소가 $n$개인 유한 집합 $X$부터 요소가 $m$개인 유한 집합 $Y$까지의 함수와 양의 정수 $k$에 대하여, $km<n$이면, $y$가 $X$의 서로 다른 요소 중 적어도 $k+1$개에서 image를 가지는 그러한 $y\in Y$ 가 있다.



**Generalized Pigeonhole Principle(Contrapositive Form)**

요소가 $n$개인 유한 집합 $X$부터 요소가 $m$개인 유한 집합 $Y$까지의 함수와 양의 정수 $k$에 대하여, 각각의 $y\in Y$에 대하여 $f^{-1}(y)$가 기껏해야 $k$개의 요소를 가지면, $X$는 기껏해야 $km$개의 요소를 가진다; 달리 말하여, $n\le km$이다.



### 9.4.3 Proof of the Pigeonhole Principle

- (7.4) 집합은 공집합이거나 $n$이 양의 정수이며 $\{1,2,...,n\}$부터 집합까지 일대일-대응할 경우(there  is a one-to-one correspondence from $\{1, 2, ... , n\}$ to it), 그리고 오직 이 경우에만 **유한하다**. 전자의 경우 **요소의 개수(number of elements)**가 0이며, 후자는 $n$개 라고 한다. 유한하지 않은 집합은 **무한하다.**



**Theorem 9.4.1 The Pigeonhole Principle**

요소가 $n$개인 유한 집합 $X$부터 요소가 $m$개인 유한 집합 $Y$까지의 함수와 양의 정수 $k$에 대하여, $n>m$이면 $f$는 일대일(one-to-one)이 아니다.

**Proof**: $f$가 요소가 $n$개인 유한 집합 $X$부터 요소가 $m$개인 유한 집합 $Y$까지의 함수이며, $n>m$이라고 하자. $Y$의 요소들을 $y_1,\ y_2,...,y_m$이라고 표기한다. 각각의 $y_i$에 대하여 inverset image set(역함수)는 $f^{-1}(y_i)=\{x\in X |f(x)=y_i\}$이다. $Y$의 모든 요소에 대한 inverser image set의 collection은 다음과 같다:
$$
f^{-1}(y_1),\ f^{-1}(y_2),\ ..., f^{-1}(y_m)
$$
함수의 정의에 의해, $X$의 각각의 요소는 $f$에 의해 $Y$의 어떤 요소와 연관된다(sent). 그러나 $X$의 각각의 요소가 inverse image sets 중 하나이므로, 그 집합들의 모든 합집합은 $X$와 같다. 또한, 함수의 정의에 의해, $X$의 어떤 요소도 $f$에 의해 $Y$의 요소를 한 개 이상 연관되지 않는다. 그러므로 $X$의 각각의 요소는 inverse image set 중 단 하나에 속하고, 따라서 inverse image sets은 mutally disjoint하다. 그러므로 addition rule에 의하여, 
$$
N(X)=N(f^{-1}(y_1))+N(f^{-1}(y_2))+...+N(f^{-1}(y_m))
$$
이제 $f$가 일대일이라고 가정하자. 그렇다면 각각의 집합 $f^{-1}(y_i)$는 기껏해야 하나의 요소를 가지므로,
$$
N(f^{-1}(y_1))+N(f^{-1}(y_2))+...+N(f^{-1}(y_m))\le1+1+...+1=m
$$
이를 치환하면 다음과 같다.
$$
n=N(X)\le m N(Y)
$$
이는 $n>m$이라는 사실에 모순되며, 따라서 $f$가 일대일이라는 가정은 거짓이다. 그러므로 $f$는 일대일이 아니다.



**Theorem 9.4.2 One-to-One and Onto for Finite Sets**

$X$와 $Y$가 동일한 개수의 요소를 가진 유한한 집합이고 $f$가 $X$부터 $Y$까지의 함수라고 하자. $f$는 $f$가 onto인 경우, 그리고 오직 이 경우에만 일대일이다.

**Proof**: $X$와 $Y$가 $m$의 요소를 가진 유한한 집합이고 $f$가 $X$부터 $Y$까지의 함수라고 하자. $X=\{x_1,\ x_2,...,x_m\}$로 $Y=\{y_1,\ y_2,...,y_m\}$로 표기한다.

**$f$가 일대일이면, $f$는 onto이다:** $f$가 일대일이다. 그렇다면 $f(x_1), f(x_2),...,f(x_m)$은 모두 서로 다르다. 어떤 요소도 $X$의 요소의 image가 아닌 $Y$의 모든 요소의 집합을 $S$라고 하자.

그렇다면 다음의 두 집합은 mutually disjoint하다.
$$
\{f(x_1)\}, \{f(x_2)\},...,\{f(x_m)\}\quad그리고\quad S
$$
addition rule에 의하여,
$$
\begin{align*}
N(Y) &= N(\{f(x_1)\})+ N(\{f(x_2)\})+...+N(\{f(x_m)\}) \\
&= 1+1+...+1+N(X) &(각각의\ \{f(x_i)\}는\ 싱글톤\ 집합이므로)\\
&= m+N(S)
\end{align*}
$$
그러므로

$$
\begin{align*}
m&=m+N(S) &(N(Y)=m이므로)\\
N(S) &= 0 &(양변에서\ m\ 뺌) \\
\end{align*}
$$
그리하여 $S$가 공집합이므로, $Y$의 어떤 요소도 $X$의 어떤 요소의 image가 아닌 요소가 없다. 결론적으로, $f$는 onto이다.



**$f$가 onto이면, $f$는 one-to-one이다:** $f$가 onto라고 가정하자. 각각의 정수 $i=1,2,...,m$에 대하여, $f^{-1}(y_i) \neq \varnothing$이고 따라서 $N(f^{-1}(y_i))\ge 1$이다. (9.4.1) proof of the pigeonhole pinciple에서처럼, $X$는 mutually disjoint set $f^{-1}(y_1),\ f^{-1}(y_2),\ ..., f^{-1}(y_m)$의 합집합이다. addition principle에 의하면,
$$
N(X)=N(f^{-1}(y_1))+N(f^{-1}(y_2))+...+N(f^{-1}(y_m))\ge m
$$
(각각의 항은 1보다 크다.) 집합들 중 하나인 $N(f^{-1}(y_i))$가 한 개 이상의 요소를 가지면, 위 항등식에서 $m$개의 항의 합은 $m$보다 크다. 그런데 $N(X)=m$이므로, 이 경우는 옳지 않다. 그러므로 각각의 집합 $f^{-1}(y_i)$가 정확히 한 개의 요소를 가며, 따라서 $f$는 일대일이다.

