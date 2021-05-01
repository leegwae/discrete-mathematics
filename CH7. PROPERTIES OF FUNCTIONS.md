# CH7. PROPERTIES OF FUNCTIONS

- floor, ceiling: functions from $R$ to $Z$



## 7.1 Functions Defined on General Sets

- 특정합 타입의 관계로서의 함수

**Definition[Function]**

**집합 $X$부터 집합 $Y$까지의 함수 $f$**는 $f:X\rightarrow Y$로 표기하며, $f$의 **domain(정의역)** $X$부터 $f$의 **co-domain** $Y$까지의 relation이다. 다음 두 가지 특징을 만족한다. (1) $X$의 모든 요소는 $Y$의 어떤 요소와 연관된다(related to). 그리고 (2) $X$의 어떤 요소도 $Y$의 요소 중 두 개 이상 연관되어 있지 않다. 그러므로, 주어진 $X$의 모든 요소 $x$에 대하여, $f$에 의해 $x$에 연관되는 요소가 $Y$에 단 한 개 존재한다. 이 요소를 $y$라 한다면, $f$가 $x$를 $y$로 보낸다(sends to)라고 하거나 $f$가 $x$를 $y$에 연결짓는다(map to)라고 하며, $x\overset{f}{\rightarrow} y$ 혹은 $f:x\rightarrow y$라고 적는다. $f$가 $x$를 보내는 유일한 요소를 $f(x)$로 표기한다. 그리고 다음과 같이 부른다.

- $x$의 $f$
- input $x$에 대한 output의 $f$
- $x$에서 $f$의 값
- the image of $x$ under $f$

$f$의 가지는 모든 값의 집합은 *$f$의 범위(range)*나 *image of $X$ under $f$*라고 부른다. 기호화하면:
$$
f의\ 범위=\mathrm{image\ of\ }X\mathrm{\ under\ }f=\{y\in Y|y=f(x),\ X\ 안의\ 어떤\ 값 x에\ 대하여\}
$$
$Y$의 주어진 요소 $y$에 대하여, $X$에 $y$에 대한 image로서의 요소가 존재할 수도 있다. $x$가 $f(x)=y$를 만족하는 요소이면, $x$의 $y$의 **preimage** 혹은 $y$의 inverse image라고 한다. $y$의 모든 inverse image의 집합은 *$y$의 inverse image*라고 한다. 기호화하면:
$$
\mathrm{the\ invrse\ image\ of\ }y=\{x\in X|f(x)=y\}
$$

### 7.1.2 Arrow Diagrams

**Theorem 7.1.1 A Test for Function Equality**

$F:X\rightarrow Y$ 그리고 $G:X\rightarrow Y$가 함수이면, 모든 $x\in X$에 대하여 $F(x)=G(x)$인 경우, 그리고 오직 이 경우에만 $F=G$이다.

**Proof**

$F:X\rightarrow Y$이고 $G:X\rightarrow Y$가 함수라고 가정하자; 즉, $F$와 $G$는 $X$부터 $Y$까지의 관계이며 두 가지 특징을 만족한다. $F$와 $G$가 $X\times Y$의 부분집합들이고, $(x,y)$가 $F$에 속하면 $y$는 $F$에 의해 $x$와 연관되는 유일한 요소이며, $F(x)$와 같이 표기한다. 비슷하게, $(x,y)가 $$G$에 속하면 $y$는 $G$에 의해 $x$와 연관되는 유일한 요소이며, $G(x)$와 같이 표기한다.

이제 모든 $x\in X$에 대하여 $F(x)=G(x)$라고 가정하자. $x$가 $X$의 요소이면,
$$
(x,y) \in F \Leftrightarrow y=F(x)\Leftrightarrow y=G(x)\Leftrightarrow(x,y)\in G
$$
그러므로 $F$와 $G$는 정확히 같은 요소로 구성되어 있으며 따라서 $F=G$이다.

반대로, $F=G$이면, 모든 $x\in X$에 댛여
$$
y=F(x)\Leftrightarrow(x,y)\in F\Leftrightarrow (x,y)\in G\Leftrightarrow y=G(x)
$$
그러므로, $F(x)$와 $G(x)$는 $y$와 같으므로, 
$$
F(x)=G(x)
$$


**Example 7.1.4 The Identity Function on a Set**

주어진 집합 $X$에 대하여, $X$부터 $X$까지의 함수 $I_X$를 다음과 같이 정의한다.
$$
I_X(x)=x\quad(X의\ 각각의\ x에\ 대하여)
$$
함수 $I_X$는 **X에 대한 항등함수**(identity function on X)라고 한다. 함수가 $X$의 각각의 요소를 그것과 동일한 요소로 보내기(send) 때문이다.



**Definition Logarithms and Logarithmic Functions**

$b$가 $b\neq 1$인 양의 실수라고 하자. 각각의 양의 실수 $x$에 대하여, **$x$의 밑(base)이 $b$인 로그(logarithm)**는 $log_bx$라고 쓰며, $b$가 $x$를 얻을 수 있도록 raised 해야하는 지수(exponent)이다. 기호화하면:
$$
log_bx=y\Leftrightarrow b^y=x
$$
**밑이 $b$인 로그 함수**는 $R^+$부터 $R$까지의 함수이며, 각각의 양의 실수 $x$를 $log_bx$로 연관짓는다.



### 7.1.3 Boolean Functions

**Definition[Boolean function]**

**$n$-place Boolean function(불 함수) $f$**는 정의역이 0과 1의 모든 ordered $n$-튜플을 정의역으로, 집합 ${0,1}$을 co-domain으로 가지는 함수이다. 더 형식적으로, 불 함수의 정의역은 집합 ${0,1}의$ Cartesian product of $n$ copies로 표현할 수 있으며, ${0,1}^n$으로 표기한다. 그러므로 $f:{0,1}^n\rightarrow {0,1}$



### 7.1.4 Checking Whether a Function Is Well Defined

"함수"는 함수가 되기 위한 조건을 하나라도 만족하지 못한다면 **잘 정의되지 않았다(not well defined).**



### 7.1.5 Functions Acting on Sets

**Definition**

$f:X\rightarrow Y$가 함수이고 $A\subseteq X$이며 $X\subseteq Y$이면,
$$
f(A)=\{y\in Y|y=f(x)\ (A의\ x에\ 대하여)\}
$$

$$
f^{-1}(C)=\{x\in X|f(x) \in C\}
$$

이다. $f(A)$는 **$A$의 image**라고 부르며, $f^{-1}$은 **$C$의 inverse image**라고 부른다.

