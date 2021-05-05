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



## 7.2 One-to-One, Onto, and Inverse Functions

### 7.2.1 One-to-One Functions

**Definition[one-to-one]**

$F$가 집합 $X$부터 집합 $Y$까지의 함수라고 하자. $F$는 모든 요소 $x_1$그리고 $x_2$가 $X$에 속하는 경우, 그리고 오직 이 경우에만 **one-to-one**(**일대일**; 혹은** **injective**)이다.
$$
F(x_1)=F(x_2)이면,\ x_1=x+2 \\
x_1\neq x_2이면,\ F(x_1)\neq F(x_2)
$$
위 두 문장은 동치이다.

기호화하면
$$
F:X\rightarrow Y는\ 일대일대응이다\Leftrightarrow \forall x_1,x_2 \in X,\ F(x_1)=F(x_2)이면\ x_1=x_2
$$


### 7.2.2 One-to-One Functions on Infinite Sets

$f$가 일대일임을 증명하려면 method of direct proof를 사용한다.

$x_1, x_2$가 $f(x_1)=f(x_2)$를 만족하는 $X$의 요소라고 **가정한다**.

$x_1=x_2$라고 **보인다**.

일대일이 아님을 증명하려면 다음과 같이 한다.

$f(x_1)=f(x_2)$이지만 $x_1 \neq x_2$인 $X$의 요소 $x_1$과 $x_2$를 **찾는다.**



### 7.2.3 Application: Hash Functions

**Definition[Hash Function]**

**hash function(해쉬 함수)**는 아주 큰, 아마 무한한 데이터의 집합부터 작고 고정된 크기의 정수의 집합까지의 함수로 정의되었다.



- 두 개의 입력값이 **collide**하면, 즉, 같은 출력값을 가진다. 다양한 방법이 이러한 **collision**을 피하기 위해 사용된다.



### 7.2.4 Onto Functions

**Definition[onto]**

$F$가 집합 $X$부터 집합 $Y$까지의 함수라고 하자. $F$는 $Y$에 속하는 요소 $y$가 주어졌을 때, $y=F(x)$라는 특성으로 $X$에 속하는 $x$를 찾을 수 있는 경우, 그리고 오직 이 경우에만 **onto**(혹은 **surjective**)이다. 기호화하면:
$$
F:X\rightarrow Y는\ \mathrm{onto}이다\quad\Leftrightarrow\quad \forall y \in Y,\ F(x)=y인\ 그러한\  \exists x \in X
$$

- 공역과 치역이 같은 함수이다.



### 7.2.5 Onto Functions on Infinite Sets

$F$가 onto라는 것을 증명하려면, method of generalizing form generic particular를 사용한다.

$y$가 $Y$의 요소라고 **가정한다**.

$F(x)=y$인 $x$가 $X$에 있음을 **보인다**.

$F$가 onto가 아니라는 것을 증명하려면, 다음과 같이 한다.

$X$의 모든 $x$에 대하여 $y\neq F(x)$인 $y$가 $Y$에 속하는지 **찾는다**



### 7.2.6 Relations between Exponential and Logarithmic Functions

양의 수 $b\ne1$에 대하여, **exponential function with base $b$(밑이 $b$인 지수 함수)**는 $\mathrm{exp}_b$라고 표기하며, $R$부터 $R^+$까지의 함수이며 다음과 같이 정의된다: 모든 실수 $x$에 대하여,
$$
\mathrm{exp}_b(x)=b^x
$$
이때 $b^0=1$이며 $b^{-x}=1/b^x$이다.



**Laws of Exponents**

$b$와 $c$가 양의 실수이고 $y$와 $v$가 실수이면, 다음의 exponents의 법칙은 참이다.
$$
\begin{align*}
b^ub^v &=b^{u+v}&7.2.1\\
(b^u)^v&=b^{uv}&7.2.2\\
\frac{b^u}{b^v}&=b^{u-v}&7.2.3\\
(bc)^u&=b^uc^u&7.2.4
\end{align*}
$$


**Theorem 7.2.1 Properties of Logarithms**

$b\ne1$이고 $c\ne1$인 양의 실수 $b,c,x$와 실수 $a$에 대하여:

1. $log_b(xy)=log_bx+log_by$
2. $log_b\left(\frac{x}{y}\right)=log_bx-log_by$
3. $log_b(x^a)=alog_bx$
4. $log_cx=\frac{log_bx}{log_bc}$



**Examples 7.2.7 Computing Logarithms with Base 2 on a Calculator**

- **common logarithms**는 log라고 표기하며, 밑으로 10을 가진다.
- **natural logarithms**는 ln으로 표기하며, 밑으로 $e$를 가진다.



### 7.2.7 One-to-One Correspondences

**Definition[one-to-one correspondence]**

집합 $X$부터 집합 $Y$까지의 **one-to-one correspondence**(**일대일대응**; 혹은 **bijection**)는 $F:X\rightarrow Y$가 one-to-one이면서 onto인 함수이다.



### 7.2.8 Inverse Functions

**Theorem 7.2.2**

$F:X\rightarrow Y$가 일대일대응이라고 가정하자; 즉, $F$가 one-to-one이면서 onto라고 하자. $F^{-1}:Y\rightarrow X$가 다음과 같이 정의된다: 주어진 $Y$의 요소 $y$에 대하여,
$$
F^{-1}(y)=F(x)가\ y와\ 같은\ 그러한\ 유일한\ x
$$
혹은 동등하게,
$$
F^{-1}(y)=x\Leftrightarrow y=F(x)
$$
**Definition[inverse function]**

Theorem 7.2.2의 $F^{-1}$는 $F$이 **inverse function(역함수)**이다.



**Theorem 7.2.3**

$X$와 $Y$가 집합이고 $F:X\rightarrow Y$가 one-to-one이면서 onto이면, $F^{-1}:Y\rightarrow X$도 one-to-one이면서 onto이다.

**Proof**  

(1) $F^{-1}$는 one-to-one이다.

$F^{-1}(y_1)=F^{-1}(y_2)인 그러한 $ $y_1$과 $y_2$가 $Y$이 요소라고 하자. $x=F^{-1}(y_1)=F^{-1}(y_2)$라고 하자. $x\in X$이며, $F^{-1}$의 정의에 이ㅡ해,
$$
\begin{align*}
F(x)&=y_1 &x=F^{-1}(y_1)이므로\\
F(x)&=y_2 &x=F^{-1}(y_2)이므로\\
\end{align*}
$$
결론적으로, $y1,\ y2$가 각각 $F(x)$와 같으므로 $y_1=y_2$이다.

(2) $F^{-1}$는 onto이다.

$x\in X$라고 가정하자. $y=F(x)$라고 하자. $y \in Y$이며, $F^{-1}$의 정의에 의해, $F^{-1}(y)=x$이다.



## 7.3 Composition of Functions

**Definition[composition]**

$f:X\rightarrow Y$이고 $g:Y'\rightarrow Z$가 $f$의 범위가 $g$의 domain의 부분집합인 특성을 가진 함수라고 하자. 새로운 함수 $g\circ f:X\rightarrow Y$를 다음과같이 정의한다:
$$
(g\circ f)(x)=g(f(x))\quad(각각의\ x\in X에\ 대하여)
$$
이때 $g\circ f$는 $g$ circle $f$라고 읽으며, $g(f(x))$는 $x$의 $f$의 $g$라고 읽는다. $g\circ f$는 **$f$와 $g$의 composition(합성)**이라고 한다.



**Theorem 7.3.1 Composition with an  Identity Function**

$f$가 집합 $X$부터 집합 $Y$까지의 함수이며 $I_X$가 $X$에 대한 identity function, $I_Y$가 $Y$에 대한 identity function이면,
$$
(a)f\circ I_X=f\quad그리고\quad(b)I_Y\circ f=f
$$
**Proof**

**Part(a)**: $f$가 집합 $X$부터 집합 $Y$까지의 함수이며 $I_X$가 $X$에 대한 identity function라고 가정하자. $X$의 각각의 $x$에 대하여,
$$
(f\circ I_X)(x)=f(I_X(x))=f(x)
$$
그러므로, equality of functions의 정의에 의하여, $f\circ I_X=f$는 참이다.

**Part(b)**: 직접 해보라



**Theorem 7.3.2 Composition of a Function with Its Inverse**

$f:X\rightarrow Y$가 one-to-one이고 onto 함수이며, 역함수 $f^{-1}:Y\rightarrow X$를 가진다면,
$$
(a)f\circ I_X=f\quad그리고\quad(b)I_Y\circ f=f
$$
**Proof**

**Part(a)**: $f:X\rightarrow Y$가 one-to-one이고 onto 함수이며, 역함수 $f^{-1}:Y\rightarrow X$를 가진다고 한다. $x$가 $X$에 속하는 요소라고 하자. 그러면 함수의 합성의 정의에 의하여,
$$
(f^{-1}\circ f)(x)=f^{-1}(f(x))
$$
이때 $z=f^{-1}(f(x))$라고 가정하자. 역함수의 정의에 의해,
$$
f(z)=f(x)
$$
$f$가 one-to-one이고 이것은 $z=x$임을 암시하기 때문이다.

$z=f^{-1}(f(x))$도 치환에 의하여
$$
f^{-1}(f(x))=x
$$
혹은, 동등하게,
$$
(f^{-1}\circ f)(x)=x
$$
$x$가 $X$의 요소이며 $I_X(x)=x$이므로, $f^{-1}\circ f=I_X$임을 증명한다.

**Part(b)**: 직접 해보라.



### 7.3.1 Composition of One-to-One Functions

**Theorem 7.3.3**

$f:X\rightarrow Y$그리고 $g:Y\rightarrow Z$가 모두 one-to-one 함수이면, $g\circ f$는 one-to-one이다.

**Proof**

$f:X\rightarrow Y$그리고 $g:Y\rightarrow Z$가 모두 one-to-one function라고 가정하자. $x_1$과 $x_2$가 다음과 같은 $X$의 요소라고 가정하자.
$$
(g\circ f)(x_1)=(g\circ f)(x_2)
$$
합성 함수의 정의에 의하여,
$$
g(f(x_1))=g(f(x_2))
$$
$g$는 one-to-one이므로, $f(x_1)=f(x_2)$이다.

$f$는 one-to-one이므로, $x_1=x_2$이다.

따라서 $g\circ f$는 one-to-one이다.



### 7.3.2 Composition of Onto Functions

**Theorem 7.3.4**

$f:X\rightarrow Y$ 그리고 $g:Y\rightarrow Z$가 모두 onto 함수이면, $g\circ f$은 onto이다.

**Proof**

$f:X\rightarrow Y$ 그리고 $g:Y\rightarrow Z$가 모두 onto 함수라고 가정하자. $z$가 $Z$의 요소이다. $g$가 onto이므로, $g(y)=z$인 $Y$의 요소 $y$가 있다. 그리고 $f$가 onto이므로, $f(x)=y$인 $X$의 요소 $x$가 있다. 그러므로 다음과 같은 $X$의 요소 $x$가 있다.
$$
(g\circ f)(x)=g(f(x))=g(y)=z
$$
그러므로 $g\circ f$는 onto이다.



## 7.4 Cardinality with Applications to Computability

**Definition**

$A$와 $B$가 집합이라고 하자. $A$는 $A$부터 $B$까지 일대일하는 경우, 그리고 오직 이 경우에만 **has the same cardinality as B**라고 한다. 다른 말로, $A$는 $A$부터 $B$까지의 함수 $f$가 one-to-one하고 onto인 경우, 그리고 오직 이 경우에만 has the same cardinality as $B$라고 한다.



**Theorem 7.4.1 Properties of Cardinality**

집합 $A,\ B,\ C$에 대하여,

1. **Reflexive property of cardinality**: $A$는 $A$와 같은 cardinality를 가진다.
2. **Symmetric property of cardinality**: $A$가 $B$와 같은 cardinality를 가지면, $B$는 $A$와 같은 cardinality를 가진다. 
3. **Transitive property of cardinality**: $A$가 $B$와 같은 cardinality를 가지고 $B$가 $C$와 같은 cardinality를 가지면, $A$는 $C$와 같은 cardinality를 가진다.



**Definition**

$A$와 $B$는 $A$가 $B$와 같은 cardinality를 가지거나 $B$가 $A$와 같은 cardinality를 가지는 경우, 그리고 오직 이 경우에만 **같은 cardinality**를 가진다고 한다.



### 7.4.1 Countable Sets

**Definition**

집합은 공집합이거나 어떤 양의 정수 $n$에 대해 ${1,2,...,n}$과 같은 형태의 집합이고 일대일대응할 수 있을 때 **유한(finite)**하다고 한다. 집합은 양의 정수의 집합 $Z^+$과 같은 cardinality를 가지고 있는 경우, 그리고 오직 이 경우에만 **countably infinite**라고 한다. 집합은 유한하거나 countably infinite인 경우, 그리고 오직 이 경우에만 **countable**이라고 한다. countable하지 않은 집합은 **uncountable**하다고 한다.



### 7.4.2 The Search for Larger Infinites: The Cantor Diagonalization Process



### 7.4.3 Application: Cardinality and COmputability

