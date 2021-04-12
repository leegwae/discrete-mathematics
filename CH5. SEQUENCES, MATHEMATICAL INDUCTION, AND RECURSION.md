# CH5. SEQUENCES, MQTHEMATICAL INDUCTION, AND RECURSION

## 5.1 Sequences

**Definition[Sequence]**

**sequence**는 주어진 두 정수 사이의 모든 정수 혹은 주어진 정수보다 크거나 같은 모든 정수를 domain으로 가진 함수이다.



**sequence 표기하기**
$$
a_m,\ a_{m+1},\ a_{m+2},...,a_n
$$

- $a_k$: **term**, 개별적인 element
- $k$: **subscript** 혹은 **index**
- $m$: **initial term**의 subscript
- $n$: **final term**의 subscript

$$
a_m,\ a_{m+1},\ a_{m+2},...
$$

- **infinite sequence**를 표기함.
- 시퀀스에 대한 **explicit formula** 혹은 **general formula**는 $a_k$의 값이 어떻게 $k$에 의존하는지 보여주는 규칙이다.



**5.1.1 Summation Notation**

**Definition[Summation Notation]**

$m$과 $n$이 정수이고 $m\le n$일 때, 기호 $\sum_{k=m}^n a_k$는 **$m$과 같은 $k$부터 $a$-sub-$k$의 $n$까지의 summation**라고 읽으며, $a_m,\ a_{m+1},\ a_{m+2},...,a_n$의 모든 항의 합이다. $a_m+a_{m+1}+a_{m+2}+...+a_n$은 합의 **expanded form**이라고 하며 다음과 같이 쓴다.
$$
\sum_{k=m}^n a_k=a_m+a_{m+1}+a_{m+2}+...+a_n.
$$
$k$는 summation의 **index**, $m$은 summation의 **lower limit**, $n$을 summation의 **upper limit**라고 한다.



**A Telescoping Sum**
$$
\begin{align*}
\sum_{k=1}^n \frac{1}{k(k+1)}&=\sum_{k=1}^n (\frac{1}{k}-\frac{1}{k+1}) \\
&=(\frac{1}{1}-\frac{1}{2})+(\frac{1}{2}-\frac{1}{3})+...+(\frac{1}{n-1}-\frac{1}{n})+(\frac{1}{n}-\frac{1}{n+1}) \\
&=1-\frac{1}{n+1}
\end{align*}
$$


**5.1.2 Product Notation**

**Definition[Product Notation]**

$m$과 $n$이 정수이고 $m\le n$일 때, 기호 $\prod_{k-m}^n a_k$은 **$m$과 같은 $k$부터 $a$-sub-$k$의 $n$까지의 product**라고 읽으며, $a_m,\ a_{m+1},\ a_{m+2},...,a_n$의 모든 항의 곱이다. 다음과 같이 쓴다.
$$
\prod_{k=m}^n a_k=a_m\cdot a_{m+1}\cdot a_{m+2}\cdot \cdot \cdot a_n
$$


**Recursive Definition for the product notation**

$m$이 정수이면
$$
\prod_{k=m}^n a_k=a_m\quad혹은\quad \prod_{k=m}^n a_k=\left(\prod_{k=m}^{n-1} a_k\right)\cdot a_n
$$


**5.1.3 Properties of Summations and Products**

**Theorem 5.1.1**

$a_m,\ a_{m+1},\ a_{m+2},...$ 그리고 $b_m,\ b_{m+1},\ b_{m+2},...$은 실수의 sequences이며 $c$는 실수라고 하자. 다음 항등식은 모두 $n\ge m$을 만족한다.
$$
\begin{align*}
\sum_{k=m}^{n}a_k+\sum_{k=m}^{n}b_k&=\sum_{k=m}^{n}(a_k+b_k) \\
c\cdot\sum_{k=m}^{n}a_k &=\sum_{k=m}^{n}c\cdot a_k \\
\left(\prod_{n}^{k=m}a_k\right)\cdot \left(\prod_{n}^{k=m}a_k\right) &=\prod_{k=m}^n(a_k\cdot b_k)
\end{align*}
$$


**5.1.4 Change of Variable**

- summation의 index를 나타내는데 사용하는 기호는 **dummy variable**이라고 불리는 local variable이다.



**5.1.5 Factorial and "$n$ Choose $r$" Notation**

**Definition[Factorial]**

모든 양수 $n$에 대하여, $n!$이라고 표기되는 quantity $n$ **factorial**은 1부터 $n$까지의 모든 정수의 곱으로 정의된다.
$$
n!=n\cdot(n-1)\cdot\cdot\cdot3\cdot2\cdot1
$$
$0!$으로 표기되는 **zero factorial**은 1로 정의된다.
$$
0!=1
$$



**Recursive definition for factorial**
$$

$$



**Definition[$n$ choose $r$]**

$n$과 $r$이 $0\le r\le n$인 정수라고 하자.
$$
{n \choose r}
$$
은 **$n$ choose $r$**이라고 읽으며, $n$개의 element를 가진 집합으로부터 $r$개 만큼 선택한 부분집합의 수를 나타낸다.



- ${n \choose r}$은 combination이라고 불리며, binomial conefficient라고 하기도 한다.



**Formula for Computing ${n \choose r}$**

$0\le r\le n$인 정수 $n$과 $r$에 대하여,
$$
{n \choose r}=\frac{n!}{r!(n-r)!}
$$


**5.1.6 Sequences in Computer Programming**



**Algorithm 5.1.1 Decimal to Binary Conversion Using Repeated Division by 2**

input은 nonnegative 정수 $a$이다. 알고리즘의 목적은 $r[0],\ r[1],\ r[2],...,r[k]$라는 binary digits의 sequence를 만들어서 $n$을 $(r[k]r[k-1]\cdot\cdot\cdot r[2]r[1]r[0])_2$로 이진 표현하는 것이다. 즉,
$$
a=2^k\cdot r[k]+2^{k-1}\cdot r[k-1]+\cdot\cdot\cdot+2^2\cdot r[2]+2^1\cdot[1]+2^0\cdot r[0]
$$



intput: $q:=a, i:=0$

```
while (i = 0 or q != 0)
	r[i] := q mod 2
	q := q div 2
	i = i+ 1
end while
```

output: $r[0],\ r[1],\ r[2],...,r[i-1]$



## 5.2 Mathematical Induction 1: Proving Formulas

**Principle of Mathematical Indunction**

$P(n)$이 정수 $n$에 대해 정의된 property이고, $a$가 fixed integer라고 한다. 다음의 두 statement를 참이라고 가정한다.

(1) $P(a)$는 참이다.

(2) $k\ge a$($a$보다 크거나 같은 모든 정수 $k$)에 대하여, $P(k)$가 참이면 $P(k+1)$도 참이다.

그리하여 statement "정수 $n\ge a$($a$보다 크거나 같은 모든 정수 $n$)에 대하여, $P(n)$이다." 는 참이다.



**Method of Proof by Mathematical Induction**

"정수 $n\ge a$에 대하여, property $P(n)$은 참이다."라는 형태의 statement를 생각해보자. 이러한 statement를 증명하기 위해서 다음의 두 단계가 필요하다.

(1) $P(a)$가 참임을 보인다.

(2)  $k\ge a$($a$보다 크거나 같은 모든 정수 $k$)에 대하여, $P(k)$가 참이면 $P(k+1)$도 참임을 보인다. 이 단계를 수행하기 위해서

​	$P(k)$가 $k$가 $k\ge a$이며 any particular한 것이지면 임의로 특정된 참이라고 **가정한다.** 이러한 가정을 **inductive hypothesis(귀납적 가설)**이라고 한다.

 그리고 $P(k+1)$이 참임을 보여라.



**Theorem 5.2.1 Sum of the First $n$ Integers**

1보다 크거나 같은 모든 정수 $n$에 대하여(For every integer $n\ge1$) 다음이 성립한다.
$$
1+2+3+...+n=\frac{n(n+1)}{2}
$$
**Proof(ny mathematical induction)**: property $P(n)$이 다음 방정식이라고 하자.
$$
1+2+3+...+n=\frac{n(n+1)}{2}=P(n)
$$
**$P(1)$이 참임을 보여라**:

$P(1)$을 증명하기 위해 다음을 보여야한다.
$$
1=\frac{1(1+1)}{2}=P(1)
$$


좌변이 1이고
$$
\frac{1(1+1)}{2}=\frac{2}{2}
$$
우변이 1이다. 따라서 $P(1)$은 참이다.



**1보다 크거나 같은 모든 정수 $k$에 대하여, $P(k)$가 참이면 $P(k+1)$ 또한 참임을 보여라.**

$k$가 $k\ge 1$을 만족하는 정수라고 해보자. 그리하여
$$
1+2+3+...+n=\frac{k(k+1)}{2}=P(k)
$$
이다. 우리는 다음을 보여야한다.
$$
1+2+3+...+(k+1)=\frac{(k+1)[(k+1)+1]}{2}
$$

$$
1+2+3+...+(k+1)=\frac{(k+1)(k+2)}{2} = P(k+1)
$$

$P(k+1)$의 좌변은 다음과 같이 나타낼 수 있다.
$$
\begin{align*}
1+2+3+...+(k+1) &=1+2+...+k+(k+1)\\
&=\frac{k(k+1)}{2}+(k+1) &\mathrm{귀납적\ 가설로부터\ 치환}\\
&=\frac{k(k+1)}{2}+\frac{2(k+1)}{2} \\
&=\frac{k^2+k}{2}+\frac{2Kk+2}{2} \\
&=\frac{k^2+3k+2}{2} &대수학에\ 의하여 \\
\end{align*}
$$
우변은 다음과 같이 나타낼 수 있다.
$$
\frac{(k+1)(k+2)}{2}=\frac{k^2+3k+2}{2}
$$
$P(k+1)$의 양변이 같으므로, 항등식 $P(k+1)$은 참이다.



**Definition[Closed form]**

가변적인 수의 항으로 된 합이 ellipsis(...)이나 sumation symbol을 포함하지 않는 표현식과 동일하다면, 이 합은 **is closed form**라고 이야기한다.



c. For an integer $h\ge 2$, write $1+2+3+...+(h-1)$ in closed form.



**Theorem 5.2.2 Sum of a Geometric Sequence**

1을 제외한 실수(any real number) $r$과 $n\ge 0$에 대하여, 다음이 성립한다.
$$
\sum_{i=0}^n r^i=\frac{r^{n+1}-1}{r-1}
$$
**Proof(ny mathematical induction)**

$r$이 1과 같지 않은 실수라고 하자. property $P(n)$은 다음과 같은 항등식이다.
$$
\sum_{i=0}^n r^i=\frac{r^{n+1}-1}{r-1}
$$
$P(n)$이 0보다 크거나 같은 모든 정수 $n$에 대하여 참임을 보여야한다. $n$에 대하여 수학적 귀납을 진행할 것이다.

**P(0)이 참임을 보여라**: $P(0)$을 증명하기 위해, 다음을 보여야 한다.
$$
\sum_{i=0}^0 r^i=\frac{r^{0+1}-1}{r-1}
$$
항등식의 좌변은 $r^0=1$이고
$$
\frac{r^{0+1}-1}{r-1} =\frac{r-1}{r-1}
$$
$r\ne 1, r\ne0$이므로 $r^1=1$이고, 따라서 $r^1=1$우변은 1이다. 그러므로 $P(0)$은 참이다.

**0보다 크거나 같은 모든 정수 $k$에 대하여, $P(k)$가 참이면 $P(k+1)$도 참임을 보여라**:

$k$가 0보다 크거나 같은 정수라고 한다. 또한 $P(k)$가 다음과 같다고 하자.
$$
\sum_{i=0}^k r^i=\frac{r^{k+1}-1}{r-1}
$$
우리는 $P(k+1)$ 가 참임을 보여야한다.
$$
\begin{align*}
\sum_{i=0}^{k+1} r^i&=\frac{r^{(k+1)+1}-1}{r-1} \\
\sum_{i=0}^{k+1} r^i&=\frac{r^{k+2}-1}{r-1}
\end{align*}
$$
$P(k+1)$의 좌변은 다음과 같다.
$$
\begin{align*}
\sum_{i=0}^{k+1} r^i&=\sum_{i=0}^{k} r^i+r^{k+1} \\
&=\frac{r^{k+1}-1}{r-1}+r^{k+1} \\
&=\frac{r^{k+1}-1}{r-1}+\frac{r^{k+1}(k-1)}{r-1} \\
&=\frac{(r^{k+1}-1)+r^{k+1}(r-1)}{r-1} \\
&=\frac{r^{k+1}-1+r^{k+2}-r^{k+1}}{r-1} \\
&=\frac{r^{k+2}-1}{r-1}
\end{align*}
$$
이는 우변과 같다.



## 5.3 Mathematical Induction 2: Applications

**Proposition 5.3.1**

8보다 크거나 같은 모든 정수 $n$에 대하여, $n¢$는 $3¢$와 $5¢$ coin을 포함하여 표현할 수 있다.

**Proof (by matiematical induction)** 

$P(n)$을 다음과 같은 문장이라고 하자.
$$
P(n) = n¢은\ 3¢과\ 5¢을\ 포함하여\ 표현할\ 수\ 있다.
$$
**P(8)는 참임을 보여라**:

8코인은 5코인 하나와 3코인 하나로 표현할 수 있으므로 $P(8)$은 참이다.

**8보다 크거나 같은 모든 정수에 대하여, $P(k)$가 참일 떄 $P(k+1)$도 참임을 보여라**: $k$가 8보다 크거나 같은 모든 정수이며 $P(k)$가 참이라고 가정하자.
$$
P(k) = k¢은\ 3¢과\ 5¢을\ 포함하여\ 표현할\ 수\ 있다.
$$
우리는 $P(k+1)$이 참임을 보여야한다.
$$
P(k+1) = (k+1)¢은\ 3¢과\ 5¢을\ 포함하여\ 표현할\ 수\ 있다.
$$
**Case 1($k¢$를 만들기 위해 $5¢$가 필요한 경우)**

이 경우에서 $5¢$를 두 개의 $3¢$로 바꾼다. 결과는 $(k+1)¢$과 될 것이다.

**Case 2($k¢$를 만들기 위해 $5¢$가 필요하지 않은 경우)**

이 경우, $k$는 8보다 크거나 같으므로, 적어도 세 개의 $3¢$가 필요하다. 그래서 세 개의 $3¢$를 없애고 이것들을 $5¢$으로 바꾼다. 결과는 $(k+1)¢$이다.

그러므로 모든 경우에서 $(k+1)¢$은 $3¢$과 $5¢$로 표현할 수 있다.



**Proposition 5.3.2**

0보다 크거나 같은 정수 $n$에 대하여, $2^{2n}-1$은 3에 의해 divisible하다.



**Proof (by mathematical induction)**: property $P(n)$이 다음과 같은 문장이라고 하자.
$$
P(n)=2^{2n}-1\mathrm{은\ 3으로\ divisible하다.}
$$
**$P(0)$이 참임을 보여라**: $P(0)$를 증명하기 위하여, 다음이 참임을 보여야한다.
$$
P(0)=2^{2\cdot 0}-1은\ 3으로\mathrm{\ divisible}하다.
$$
계산하면
$$
2^{2\cdot 0}-1=2^0-1=1-1=0
$$
이다. 0은 $0=3\cdot 0$이므로 0은 $3$으로 divisible할 수 있다. 그러므로 $P(0)$은 참이다.



**0보다 크거나 같은 정수 $k$에 대하여, $P(k)$가 참이면 $P(k+1)$도 참임을 보여라**

$k$가 0보다 크거나 같은 정수이며, 다음이 참이라고 가정하자.
$$
P(k)=2^{2k}-1은\ 3으로\ \mathrm{divisible}하다.
$$
divisibility의 정의에 의하면, 이것은 다음을 뜻한다.
$$
2^{2k}-1=3r\quad어떤\ 정수\ r에\ 대하여
$$
우리는 $P(k+1)$이 참임을 보여야한다.
$$
P(k+1)=2^{2(k+1)}-1은\ 3으로\ \mathrm{divisible}하다.
$$

$$
\begin{align*}
2^{2(k+1)}-1&=2^{2k+2}-1 \\
&=2^{2k}\cdot 2^2-1 &지수\ 법칙에\ 의하여\\
&=2^{2k}\cdot 4-1 \\
&=2^{2k}(3|1)-1\\
&=2^{2k}\cdot 3+(2^{2k}-1) &대수학에\ 의하여\\
&=2^{2k}\cdot 3+3r &귀납적\ 가설에\ 의하여\\
&=3\cdot(2^{2k}+r) &3으로\ 묶는다.
\end{align*}
$$

$2^{2k}+1$은 정수의 합이므로 정수이며, divisibility의정의에 의하여 $2^{2(k+1)}-1$은 3으로 divisibile하다.



**Proposition 5.3.3**

3보다 크거나 같은 모든 정수 $n$에 대하여, $2n+1<2^n$이다.

**Proof (by mathematical induction)**: property $P(n)$이 다음과 같은 부등식이라고 하자.
$$
P(n)=2n+1<2^n
$$
**$P(3)$이 참임을 보여라**:

$P(3)$을 증명하려면 다음이 참임을 보여야한다.
$$
2\cdot 3+1<2^3
$$

$$
2\cdot3+1=7\quad 그리고\quad 2^3=8\quad 7<8
$$

그러므로 $P(3)$은 참이다.

**3보다 크거나 같은 모든 정수 $k$에 대하여, $P(k)$가 참이면 $P(k+1)$도 참임을 보여라**

$k$가 3보다 크거나 같은 정수라고 가정하여 $P(k)$가 참이라고 하자.
$$
2k+1<2^k
$$
우리는 $P(k+1)$가 참임을 보여야한다.
$$
2(k+1)+1<2^{(k+1)}
$$

$$
\begin{align*}
2(k+1)+1&=2k+1+2 &대수학에\ 의하여\\
&<2^k+2 &귀납적\ 가설에\ 의하여\ 2k+1<2^k이므로\\
&<2^k+2^k &k\ge3이므로\ 2<2^k\\
&=2\cdot 2^k &대수학에\ 의하여\\
&=2^{k+1} &지수법칙에\ 의하여
\end{align*}
$$

그러므로 $2(k+1)+1<2^{k+1}$이다.



**예시 5.3.3 Proving a Property of a Sequence**

sequence $a_1,a_2,a_3,...$이 다음과 같다:
$$
\begin{align*}
a_1&=2\\
a_k&=5a_{k-1} &(모든\ k\ge2에\ 대하여)
\end{align*}
$$

- $a_n=2\cdot 5^{n-1}$을 만족하는지 증명하라.



**Proof (by mathematical induction)**

$P(n)$이 다음과 같은 항등식이라고 하자.
$$
a_n=2\cdot5^{n-1}
$$
**$P(1)$가 참임을 보여라**

$P(1)$을 증명하려면 다음이 참임을 보여야한다.
$$
a_1=2\cdot5{1-1}
$$
$P(1)$의 좌변은 다음과 같다.
$$
a_1=2\quad (a_1,a_2, a_3,...의\ 정의에\ 의하여)
$$
$P(1)$의 우변은 다음과 같다.
$$
2\cdot5^{1-1}=2\cdot5^0=2\cdot1=2
$$
$P(1)$의 양변이 같으므로 $P(1)$은 참이다.

**1보다 크거나 같은 정수 $k$에 대하여, $P(k)$이면 $P(k+1)$도 참임을 보여라:**

$k$가 $k\ge1$을 만족하는 정수이며, 다음 $P(k)$가 참이라고 가정하자.
$$
a_k=2\cdot5^{k-1}
$$
우리는 $P(k+1)$가 참임을 보여야한다.
$$
a_{k+1}=2\cdot5^{(k+1)-1}
$$
은 다음과 같다.
$$
a_{k+1}=2\cdot5^k
$$
$P(k+1)$의 좌변은 다음과 같다.
$$
\begin{align*}
a_{k+1}&=5a_{(k+1)-1} &a_1,a_2,a_3,...의\ 정의에\ 의하여 \\
&=5a_{k} &(k-1)+1=1이므로\\
&=5\cdot(2\cdot5^{k-1}) &귀납적\ 추론에\ 의하여\\
&=2\cdot(5\cdot5^{k-1}) &\mathrm{regrouping에\ 의하여}\\
&=2\cdot5^k &지수\ 법칙에\ 의하여
\end{align*}
$$


**5.3.1 A Problem with Trominoes**

**Theorem 5.3.4 Covering a Board with Tromineos**

$n\ge1$인 정수 $n$에 대하여, $2^n \times 2^n$의 체크보드로부터 하나의 사각형을 제거한다면 남은 사각형들은 L자 모형의 trominoes로 완전히 감쌀 수 있다.

교재참고



## 5.4 Stong Mathematical Induction and the Well-Ordering Principle for the Integers

**Principle of Stong Mathematical Induction**

$P(n)$은 정수 $n$에 대한 property이며, $a$과 $b$는 $a\le b$인 fixed integers라고 하자. 다음의 두 statement가 참이라고 가정한다.

(1) $P(a),P(a+1),...,그리고\ P(b)는\ 참이다.$ (**basic step**)

(2) $k\ge b$를 만족하는 모든 정수 $k$에 대하여, $P(i)$가 $a$부터 $k$까지의 각각의 정수 $i$에 대하여 참이면, $P(k+1)$는 참이다. (**inductive step**)

이때 다음의 문장이 성립한다.
$$
n\ge a를\ 만족하는\ 모든\ 정수\ n에\ 대하여,\ P(n)
$$
$P(i)$가 $a$부터 $k$까지의 각각의 정수 $i$에 대하여 참이라고 가정하는 것을 **inductive hypothesis(귀납적 가설)**이라고 한다. 귀납적 가설을 표현하는 다른 방법은 $P(a),P(a+1),...,P(k)가\ 모두\ 참이다.$이다.



**5.4.1 Applying Strong Mathematical Induction**



**Theorem 4.4.4**

1보다 큰 정수는 소수로 divisible하다.



**Poorf (by strong mathematical induction)**

$P(n)$이 다음과 같은 문장이라고 하자.
$$
n은\ 소수로\ \mathrm{divisible}하다.
$$
**$P(2)$가 참임을 보여라:**

$P(2)$를 증명하기 위해, 다음이 참임을 보여야한다.
$$
2는\ 소수로\ \mathrm{divisible}하다.
$$
**2보다 크거나 같은 모든 정수 $k$에 대하여 $P(i)$가 2부터 $k$까지의 모든 정수에 대하여 참이면, $P(k+1)$도 참임을 보여라**:

$k\ge 2$을 만족하는 모든 정수 $k$에 대하여, 다음이 참이라고 가정한다.
$$
2부터\ k까지의\ 각각의\ 정수\ i는\ 소수로\ \mathrm{divisible}하다.
$$
우리는 $P(k+1)$가 참임을 보여야한다.
$$
k+1은\ 소수로\ \mathrm{divisible}하다.
$$
**Case 1($k+1$은 소수이다)**: 이 경우, $k+1$은 소수이므로, divisible하다.

**Case2($k+1$이 소수가 아니다)**: $a$와 $b$가 $1<a<k+1$와 $1<b<k+1$를 만족하는 정수이며 $k+1=ab$라고 가정한다. 그러므로, $2\le a\le k$이므로 귀납적 가설에 의하여, $a$는 소수 $p$로 divisible할 수 있다. 게다가 $k+1=ab$이므로, $k+1$은 $a$로 divisible하다. 그러므로, $k+1$은 $a$로 divisible하고 $a$는 $p$로 divisible하므로, transitivity of divisibility에 의하여, $k+1$은 소수 $p$로 divisible하다.

그러므로, $k+1$가 소수인지 아닌지에 상관없이, 이것은 소수로 divisible하다.



**예시 5.4.2 Proving a Property of a Sequence with String Induction**

sequence $s_0, s_1, s_2,...$를 다음과 같이 정의한다:
$$
s_0=0, s_1=4, s_k=6a_{k-1}-5a_{k-2}\quad 2보다\ 크거나\ 같은\ 모든\ 정수\ k에\ 대하여
$$

- sequence의 모든 항이 항등식 $s_n=5^n-1$을 만족하는지 증명하라.



**Proof**

$P(n)$이 다음과 같은 formula라고 하자.
$$
s_n=5^n-1
$$
**$P(0)$이 참이고 $P(1)$이 참임을 보여라**

$P(0), P(1)$을 증명하기 위하여, 다음을 보여야한다.
$$
s_0=5^0-1\quad그리고\quad s_1=5^1-1
$$
$s_0, s_1, s_2$의 정의에 의하여 $s_0=0$이고 $s_1=4$이다. $5^0-1=1-1=0$이고 $5^1-1=5-1=4$이므로 $s_0$과 $s_1$의 값은 formula에 의해 주어진 값과 일치한다.



**1보다 크거나 같은 모든 정수 $k$에 대하여 $P(i)$가 0부터 $k$까지의 모든 정수에 대하여 참이면, $P(k+1)$도 참임을 보여라**:

정수 $k$가 $k\ge1$을 만족하며, 다음이 참이라고 가정한다.
$$
s_i=5^i-1\quad(0\le i\le k를\ 만족하는\ 각각의\ 정수\ i에\ 대하여)
$$
우리는 $P(k+1)$가 참임을 보여야한다.
$$
s_{k+1}=5^{k+1}-1
$$
$k\ge1$이므로, $k+1\ge 2$이다. 따라서,
$$
\begin{align*}
s_{k+1}&=6s_k-5s_{k-1} & s_0, s_1, s_2의\ 정의에\ 의하여 \\
&=6(5^k-1)-5(5^{k-1}-1) & \mathrm{definition\ hypothesis}에\ 의하여\\
&=6\cdot 5^k-6-5^k+5 & 괄호를\ 풀고\ 지수법칙을\ 적용함. \\
&=(6-1)5^k-1 &\ 5^k로\ 묶고\ 산술연산 \\
&=5\cdot 5^k-1 &산술연산 \\
&=5^{k+1}-1
\end{align*}
$$





**예시 5.4.3 A Sequence That Involves the Floor Function**

sequence $a_1, a_2, a_3, ...$를 다음과 같이 정의한다:
$$
a_1=0,\ a_2=2,\ a_k=3a_{\lfloor k/2 \rfloor}+2
$$
$a_n$이 $n\ge1$을 만족하는 모든 정수 $n$에서 짝수임을 증명하라.



**$P(1)$과 $P(2)$가 참임을 보여라**: $a_0=0$이고 $a_1=0$이며 0과 2는 짝수 정수이므로 $n=1$과 $n=2$에서 참이다.



**1보다 크거나 같은 모든 정수 $k$에 대하여 $P(i)$가 1부터 $k$까지의 각각의 정수 $i$에 대해서 참이면, $P(k+1)$에서도 참임을 보여라:**

$k$는 $k\ge1$을 만족하는 정수이며, 다음이 성립한다고 가정하자.
$$
a_i는\ 1\le i\le k를\ 만족하는\ 각각의\ 정수\ i에\ 대하여\ 짝수이다.
$$
$a_1, a_2, a_3, ...$의 정의에 의하여,
$$
a_k=3a_{\lfloor k/2 \rfloor}+2\quad(k\ge3을\ 만족하는\ 모든\ 정수에서)
$$
$k\ge 1$이므로, $1\le \lfloor k/2 \rfloor \le k$이다. 귀납적 가설에 의하여 $a_{\lfloor k/2 \rfloor}$는 짝수이다. 홀수와 짝수의 곱은 짝수이므로, $3a_{\lfloor k/2 \rfloor}$는 짝수이다. 또한 짝수의 합은 짝수이므로 $3a_{\lfloor k/2 \rfloor}+2$도 짝수이다. 결론적으로, $a_k$는 짝수이다.



**Convention**

단일한 숫자 $x_1$은 하나의 인수로 된 곱이며 zero multiplications으로 계산될 수 있다.



**예시 5.4.4 The Number of Multiplications Needed to Multiply $n$ Numbers**

$n\ge1$을 만족하는 정수에 대하여, $x_1, x_2, ..., x_n$이 $n$개의 숫자라면, 이들의 곱 사이에 어떻게 괄호가 들어가든 곱을 계산하기 위해 사용하는 곱하기(multiplications)의 수는 $n-1$이다.



**Proof (by string mathematical induction)**

$P(n)$이 위 문장이라고 해보자.



**P(1)이 참임을 보여라:**

$P(1)$이 참이려면, 다음이 참임을 보여야한다.

$x_1$의 곱을 계산하기 위해 필요한 곱하기의 수는 1-1이다.

convenction에 의하여, $x_1$은 zero multiplications로 계산될 수 있는 product이고, $0=1-1$이므로 이것은 참이다.



**$k\ge1$을 만족하는 모든 정수 $k$에 대하여, $1$ 부터 $k$까지의 각각의 숫자 $i$에 대하여 $P(i)$가 참이면 $P(k+1)$ 역시 참임을 보여라.**

$k$가 $k\ge1$을 만족하는 정수이며, 다음 $P(k)$가 참이라고 가정한다.

1부터 $k$까지의 각각의 정수 $i$에 대하여, $x_1, x_2, ..., x_i$이 $i$개라면, 이들의 곱에 어떻게 괄호가 삽입되든, 이 곱을 계산하기 위해 필요한 곱하기의 수는 $i-1$이다.

우리는 다음 $P(k+1)$이 참임을 보여야한다.

1부터 $k+1$까지의 각각의 정수 $i$에 대하여, $x_1, x_2, ..., x_{k+1}$이 $k+1$개라면, 이들의 곱에 어떻게 괄호가 삽입되든, 이 곱을 계산하기 위해 필요한 곱하기의 수는 $(k+1)-1=k$개이다.

$k+1$의 곱의 인수가 $x_1, x_2, ..., x_{k+1}$이라고 하자. 곱은 계산하기 위하여 괄호가 삽입되었을 때, 어떤 곱하기는 마지막 곱하기이고, 마지막 곱하기를 구성하는 두 개의 인자는 $k+1$ 인자보다 작다. $L$이 좌변의 인자들의 곱이고 $R$이 우변의 인자들의 곱이라고 하자. 곱의 총 인자수는 $l+r=k+1$이고 $1\le l \le k$이고 $1\ge r \le k$이다.

귀납적 가설에 의하여, $L$을 계산하는 것은 $l-1$개의 곱하기를 취하고 $R$을 계산하는 것은 $r-1$개의 곱하기를 취한다. 최종 곱하기가 $L\cdot R$을 평가하는데 필요하므로, 모든 $k+1$ 개의 인자의 곱을 평가하는데 필요한 곱하기의 수는 다음과 같다.
$$
(l-1)+(r-1)+1=(l+r)-1=(k+1)-1=k
$$


**Theorem 5.4.1 Existence and Uniqueness of Binary Integer Representations**

주어진 양의 정수 $n$에 대하여, $n$은 다음의 형태로 unique하게 표현할 수 있다.
$$
n=c_r\cdot 2^r+c_{r-1}\cdot 2^{r-1}+...+c_2\cdot 2^2+c_1\cdot 2+c_0
$$
이때 $r$은 nonnegative intger이며, $j=0,1,2,...,r-1$인 각각의 $j$에 대하여 $c_r=1$이고 $c_j=1$이거나 0이다.

**Proof: **

**Existence (proof by strong mathematical induction)**: property $P(n)$이 다음과 같은 항등식이라고 하자.
$$
n=c_r\cdot 2^r+c_{r-1}\cdot 2^{r-1}+...+c_2\cdot 2^2+c_1\cdot 2+c_0
$$
이때 $r$은 nonnegative intger이며, $j=0,1,2,...,r-1$인 각각의 $j$에 대하여 $c_r=1$이고 $c_j=1$이거나 0이다.

**$P(1)$이 참임을 보여라:**

$r=0$이고 $c_0=1$이라고 하자. $1=c_r\cdot 2^r$이므로, $n=1$은 주어진 form으로 쓸 수 있다.



**$k\ge1$을 만족하는 모든 정수 $k$에 대하여, $1$ 부터 $k$까지의 각각의 숫자 $i$에 대하여 $P(i)$가 참이면 $P(k+1)$ 역시 참임을 보여라.**

$k$가 $k\ge1$을 만족하는 정수이며, 다음이 $1$부터 $k$까지의 각각의 정수 $i$에 대하여 참이라고 가정한다.
$$
i=c_r\cdot 2^r+c_{r-1}\cdot 2^{r-1}+...+c_2\cdot 2^2+c_1\cdot 2+c_0
$$
이때 $r$은 nonnegative intger이며, $j=0,1,2,...,r-1$인 각각의 $j$에 대하여 $c_r=1$이고 $c_j=1$이거나 0이다. 우리는 $k+1$이 주어진 form에서 2의 제곱의 합으로 쓸 수 있다고 증명해야한다.

**Case 1($k+1$이 짝수인 경우)**: 이 경우, $(k+1)/2$는 정수이며, 귀납적 가설에 의하여 $1\le(k+1)/2\le k$이므로
$$
\frac{k+1}{2}=c_r\cdot 2^r+c_{r-1}\cdot 2^{r-1}+...+c_2\cdot 2^2+c_1\cdot 2+c_0
$$
이때 $r$은 nonnegative intger이며, $j=0,1,2,...,r-1$인 각각의 $j$에 대하여 $c_r=1$이고 $c_j=1$이거나 0이다.  항등식의 양변을 2로 곱하면
$$
k+1=c_r\cdot 2^{r+1}+c_{r}\cdot 2^{r}+...+c_2\cdot 2^3+c_1\cdot 2^2+c_0\cdot2
$$
이것은 주어진 form의 2의 제곱의 합이다.



**Case 2($k+1$이 홀수인 경우)**: 이 경우, $k/2$는 정수이며, 귀납적 가설에 의하여 $1\le k/2 =k$이므로,
$$
\frac{k}{2}=c_r\cdot 2^r+c_{r-1}\cdot 2^{r-1}+...+c_2\cdot 2^2+c_1\cdot 2+c_0
$$
이때 $r$은 nonnegative intger이며, $j=0,1,2,...,r-1$인 각각의 $j$에 대하여 $c_r=1$이고 $c_j=1$이거나 0이다.  항등식의 양변을 2로 곱하고 1을 더하면
$$
k+1=c_r\cdot 2^{r+1}+c_{r}\cdot 2^{r}+...+c_2\cdot 2^3+c_1\cdot 2^2+c_0\cdot2+1
$$
이것은 주어진 form의 2의 제곱의 합이다.

$k+1$이 짝수인지 홀수인지에 상관없이 $k+1$은 주어진 형태로 표현할 수 있다.



**Uniqueness:** uniqueness를 증명하기 위해서, 정수 $n$이 2의 nonnegative integer 제곱의 합으로 된 표현을 서로 다른 두 개로 가질 수 있다고 하자. 두 식을 항등식으로 만들고, 동일한 항을 제거하면 다음과 같다.
$$
2^r+c_{r-1}\cdot 2^{r-1}+..c_1\cdot2+c_0=2^s+d_{s-1}\cdot2^{s-1}+...+d_1\cdot2+d_0
$$
이때 $r$과 $s$는 nonnegative intger이며, $c_i$과 $d_i$은 0이나 1과 같다. generality의 손실없이, $r<s$라고 하자. sum of geometric sequence(Theorem 5.2.2)에 대한 formula에 의하여, $r<s$는 $r+1\le s$를 암시하므로,
$$
\begin{align*}
2^r+c_{r-1}\cdot 2^{r-1}+..c_1\cdot2+c_0&\le 2^r+2^{r-1}+...+2+1=2^{r+1}-1 \\&<2^s
\end{align*}
$$
그러므로
$$
2^r+c_{r-1}\cdot 2^{r-1}+..c_1\cdot2+c_0\le 2^s+d_{s-1}\cdot2^{s-1}+...+d_1\cdot2+d_0
$$


**5.4.2 The Well-Ordering Principle for the Integers**

**Well-Ordering Principle for the Integers**

$s$는 하나 혹은 모두 어떤 fixed 정수보다 큰 정수들을 포함한 정수의 집합이라고 하자. 그렇다면 $S$는 적어도 하나의 element를 가진다.



**Quotient-Remainder Theorem (Existence Part)**

주어진 정수 $n$과 양의 정수 $d$에 대하여, 다음을 만족하는 정수 $q$와 $r$이 존재한다.
$$
n=dq+r\ 그리고\ 0\le r\le d
$$
**Proof**: $S$이 $n-dk$와 같은 형태의 모든 nonnegative 정수들의 집합이라고 하자. $k$는 정수이다. 

$n$이 nonnegative라면, $n-0\cdot =n\ge0$이므로 $n-0$은 $S$에 속한다. 또한, $n$이 nonnegative가 아니라도, $n-nd=n(1-d)\ge0$이므로 $n-nd$는 $S$에 속한다. 따라서 이 집합은 적어도 하나의 요소를 가진다. 이것은 $S$가 적어도 하나의 요소 $r$을 가진다는 well-ordering principle for the integers에 의하여 도출된다. 

$k$의 특정 명시적인 정수 값을 $q$라고 하면 $S$의 모든 정수는 $n-dk$과 같은 형태로 쓰일 수 있으므로 $n-dq=r$과 같이 쓸 수 있다. 양변에 $dq$를 더하면 $n=dq+r$이다.

$r\ge d$라고 가정했으므로, 다음은 참이다.
$$
n-d(q+1)=n-dq-d=r-d\ge0
$$
그러므로 $n-d(q+1)$은 $S$에 속하는 $r$보다 작은 nonnegative 정수이다. 그런데 $r$이 $S$에서 가장 작은 정수이다. 이는 모순이므로, $r\ge d$는 거짓이다. 따라서 $r<d$이다.

앞선 논증에 따라, 다음을 만족하는 정수 $q$와 $r$이 존재한다.
$$
n=dq+r\ 그리고\ 0\le r\le d
$$





## 5.6 Defining Sequences Recursively

**Definition[Recurrence relation]**

sequence $a_0, a_1, a_2,...$에 대한 **recurrence relation**은 각각의 항 $a_k$와 $i$가 $k-i\ge0$인 predecessors의 일부 $a_{k-1}, a_{k-2},...,a_{k-i}$를 연관짓는 formula이다. $i$가 fixed integer라면, 그러한 recurrence relation에 대한 **initial conditions**은 $a_0, a_1, a_2,...,a_{i-1}$의 값을 명시한다. $i$가 $k$에 의존한다면, initial conditions은  $m$이 $m\ge0$을 만족하는 정수인 $a_0, a_1, a_2,...,a_{m}$의 값을 명시한다.



**5.6.1 Examples of Recursively Defined Sequences**

하노이, 피보나치 수열

**5.6.2 Recursive Definitions of Sum and Product**

**Definition[Summation, Product]**

$n$이 양의 정수인 주어진 수 $a_1, a_2,..., a_n$에 대해, **$i$=1부터 $a_i$의 $n$까지의 summation**은 $\sum_{i=1}^{n}a_i$으로 표기하며, 다음과 같이 정의한다.
$$
\sum_{i=1}^1 a_i=1\quad그리고\sum_{i=1}^n a_i=\left(\sum_{i=1}^{n-1} a_i\right)+a_n\quad(만약\ n>1)
$$
**$i$=1부터 $a_i$의 $n$까지의 summation**은 $\prod_{i=1}^{n}a_i$으로 표기하며, 다음과 같이 정의한다.
$$
\prod_{i=1}^1 a_i=1\quad그리고\prod_{i=1}^n a_i=\left(\prod_{i=1}^{n-1} a_i\right)\cdot a_n\quad(만약\ n>1)
$$


## 5.7 Solving Recurrence Relations by Iteration

**5.7.1 The Method of Iteration**

- **iteration(반복, 순회)**: 재귀적으로 정의된 sequence에 대한 explicit formula를 찾는 기본적인 방법



**Definition[Arithmetic Sequence]**

sequence $a_0, a_1, a_2,...$는 다음을 만족시키는 constant(상수) $d$가 있는 경우, 그리고 오직 이 경우에만 **arithmetic sequence**라고 한다.
$$
a_k=a_{k-1}+d\quad(k\ge1인\ 각각의\ 정수에\ 대하여)
$$
이로부터 다음을 이끌어낼 수 있다.
$$
a_n = a_0 + dn\quad(n\ge0인\ 각각의\ 정수에\ 대하여)
$$


**Definition[Geometric Sequence]**

sequence $a_0, a_1, a_2,...$는 다음을 만족시키는 constant(상수) $r$이 있는 경우, 그리고 오직 이 경우에만 **geometric sequence**라고 한다.
$$
a_k=ra_{k-1}\quad(k\ge1인\ 각각의\ 정수에\ 대하여)
$$
이로부터 다음을 이끌어낼 수 있다.
$$
a_n=a_0r^{n}\quad(k\ge0인\ 각각의\ 정수에\ 대하여)
$$


**5.7.2 Using Formulas to Simlify Solutions Obtained by Iteration**



**5.7.3 Checking the Correctness of a Formula by Mathematical Induction**

**5.7.4 Discovering That an Explicit Formula Is Incorrect**



## 5.8 Second-Order Linear Homogeneous Recurrence Relations with Constant Coefficients

**Definition[Second-Order Linear Homogeneous Recurrence Relations with Constant Coefficients]**

**second-order linear homogeneous recurrence relation with constant coefficients**는 다음과 같은 form의 recurrence relation이다.
$$
a_k=Aa_{k-1}+Ba_{k-2}\quad(k\ge어떤\ \mathrm{fixed}\ 정수에\ 대하여)
$$
이때, $A$와 $B$는 fixed 실수이며, $B\ne0$이다.



**5.8.1 The Distinct-Roots Case**

**Lemma 5.8.1**

$A$와 $B$가 실수라고 하자.
$$
a_k=Aa_{k-1}+Ba_{k-2}\quad(k\ge어떤\ \mathrm{fixed}\ 정수에\ 대하여)\quad(5.8.1)
$$
와 같은 form의 recurrence relation는 다음과 같은 sequence에 의해 만족된다.
$$
1, t,t^2,t^3,...,t^n,...,
$$
여기서 $t$는 0이 아닌 실수이다. 이때, $t$가 다음의 방정식을 만족하는 경우, 그리고 오직 이 경우에만 그러하다.
$$
t^2-At-B=0\quad(5.8.2)
$$


**Definition[Characteristic equation of the relation]**

주어진 second-order linear homogeneous recurrence relation with constant coefficients
$$
a_k=Aa_{k-1}+Ba_{k-2}\quad(k\ge어떤\ \mathrm{fixed}\ 정수에\ 대하여)\quad(5.8.1)
$$
에 대하여, **characteristic equation of the relation**은 다음과 같다.
$$
t^2-At-B=0\quad(5.8.2)
$$


**Lemma 5.8.3 Distinct-Roots Theorem**

sequence $a_0, a_1, a_2,...$가 다음 recurrence relation을 만족한다고 가정하자.
$$
a_k=Aa_{k-1}+Ba_{k-2}\quad(5.8.2)
$$
이때 $A$와 $B$는 어떤 실수이며, $B\ne0$이다. 또한 $k\ge2$이다. 
$$
t^2-At-B=0\quad(5.8.2)
$$
인 characteristic equation이 서로 다른 roots $r$과 $s$를 가지면, $a_0, a_1, a_2,...$는 다음 explicit formula에 의해 주어진다.
$$
a_n=Cr^n+Ds^n
$$
여기서 $C$와 $D$는 $a_0$과 $a_1$의 값에 의해 그 값이 결정되는 수들이다.



**Proof**

어떤 실수 $A$와 $B$에 대하여, sequence $a_0, a_1, a_2,...$가 $k\ge0$인 각각의 정수에 대하여 recurrence relation $a_k=Aa_{k-1}+Ba_{k-2}$을 만족한다고 가정하자. 그리고 characteristic equation $t^2-At-B$가 서로 다른 roots $r$과 $s$를 가진다고 하자.

우리가 증명할 것은 다음과 같다.
$$
n\ge0인\ 각각의\ 정수에\ 대하여,\ a_n=Cr^n+Ds^n
$$
이때 $C$와 $D$는 다음과 같은 수들이다.
$$
a_0=Cr^0+Ds^0\quad그리고\quad a_1=Cr^1+Ds^1
$$


$P(n)$은 다음과 같은 항등식이라고 하자.
$$
a_n=Cr^n+Ds^n
$$
**$P(n)$과 $P(1)$이 참임을 보여라**: $P(0)$과 $P(1)$의 진리값은 자동적으로 정해지는데, 왜냐하면 $C$와 $D$가 다음의 항등식을 참이게 만드는 수이기 때문이다.
$$
a_0=Cr^0+Ds^0\quad그리고\quad a_1=Cr^1+Ds^1
$$


**$k\ge1$인 각각의 정수에 대하여, $P(i)$가 0부터 $k$까지의 각각의 정수 $i$에 대해 참이면, $k+1$도 참임을 보여라:**

$k$가 $k\ge1$을 만족하는 정수이며, 0부터 $k$까지의 각각의 정수 $i$에 대하여 다음이 참이라고 가정하자.
$$
a_i=Cr^i+Ds^i
$$
우리는 다음 $P(k+1)$을 증명해야 한다
$$
a_{k+1}=Cr^{k+1}+Ds^{k+1}
$$
inductive hypothesis에 의하여
$$
a_k=Cr^k+Ds^k\quad그리고\quad a_{k-1}=Cr^{k-1}+Ds^{k-1}
$$
따라서
$$
\begin{align*}
a_{k+1}&=Aa_k+Ba_{k-1} &a_0,\ a_1,\ a_2,...의\ 정의에\ 의하여\\ 
&=A(Cr^k+Ds^k)+B(Cr^{k-1}+Ds^{k-1}) &\mathrm{inductive\ hypothesis}에\ 의하여\\
&=C(Ar^k+Br^{k-1})+D(As^k+Bs^{k-1}) &항으로\ 묶기\\
&=Cr^{k+1}+Ds^{k+1} &\mathrm{Lemma}\ 5.8.1에\ 의하여\\
\end{align*}
$$


**5.8.1 The Single-Root Case**

**Lemma 5.8.4**

$A$와 $B$가 실수이며, characteristic equation
$$
t^2-At-B=0
$$
이 single root $r$을 가진다고 가정하자. sequences $1,\ r^1,\ r^2,\ r^3,...,\ r^n,...$그리고 $0,r,2k^2,3r^3,..,nr^n,...$ 모두 $k\ge2$인 각각의 정수에 대하여 다음 recurrence relation을 만족한다고 하자.
$$
a_k=Aa_{k-1}+Ba_{k-2}
$$


**Theorem 5.8.5 Single-Root Theorem**

sequence $a_0, a_1, a_2,...$가 다음 recurrence relation을 만족한다고 가정하자.
$$
a_k=Aa_{k-1}+Ba_{k-2}
$$
이때 $A$와 $B$는 어떤 실수이며, $B\ne0$이다. 또한 $k\ge2$이다. characteristic equation $t^2-At-B=0$이 single (real) root $r$을 가지면, $a_0, a_1, a_2,...$은 다음 explicit formula에 의해 주어진다.
$$
a_n=Cr^n+Dnr^n
$$
여기서 $C$와 $D$는 $a_0$의 값과 sequence의 다른 알려진 값들에 의해 그 값이 결정되는 실수이다.



## 5.9 General Recursive Definitions and Structural Induction

**5.9.1 Recursively Defined Sets**

집합에 대한 recursive definition은 다음의 세 component로 구성되어 있다.

- (1) **Base**: certain object가 집합에 속해있다는 statement
- (2) **Recursion**: 집합 안의 이미 알려진 객체로부터 어떻게 새로운 집합 객체를 구성하느냐(form)를 지시하는 rule의 collection
- (3) **Restriction**: base와 recursion으로부터 비롯된 객체 이외에는 어떤 객체도 집합에 속하지 않는다는 statement



**Recursive Definition for the Set of All Strings over al Finite Set**

$A$가 유한한 집합이라고 하자. $A$의 요소를 **Characters**라고 하고, **$A$에 대한 모든 문자열의 집합 $S$**를 다음과 같이 정의한다.

$\mathrm{I.}$ **Base: ** $\lambda$는 $S$의 문자열이며, $\lambda$는 문자가 없는 "문자열"인 **null string**이라고 나타낸다.

$\mathrm{II}. $**Recursion**: 새로운 문자열은 다음의 규칙을 따라 만든다.

​	$\mathrm{II(a)}$	$u$가 $S$의 문자열이고 $c$가 $A$의 문자이면, $uc$는 $S$의 문자열이다. $uc$는 **concatenation of $u$*and $c$**($u$와 $c$의 결합)이라고 하며, $u$의 오른편에 $c$를 추가(append)함으로써 얻어진다.

​	$\mathrm{II(b)}$	$u$가 $S$의 문자열이면, $\lambda u$로 표기하는 $\lambda$와 $u$의 concatenation와 $u\lambda$로 표기하는 $u$와 $\lambda$의 concatenation 모두 $u$와 동일한 것으로 정의된다. 기호화하면 다음과 같다.
$$
\lambda u=u\lambda=u
$$
​	$\mathrm{II(b)}$	$u$와 $v$가 $S$의 문자열이고, $c$가 $A$의 문자이면, $u$와 $vc$의 concatenation은 $uv$와 $c$의 concatenation과 동일한 것으로 정의된다. 기호화하면:
$$
u(vc)=(uv)c
$$
$\mathrm{II}. $ **Restriction**: base와 recursion으로부터 얻은 객체를 제외하고 어떤 것도 $S$의 문자열이 아니다.



**Theorem 5.9.1 Characters Are Strings**

$A$가 유한한 집합이고 $S$가 $A$에 대한 모든 문자열의 집합이면, $A$의 모든 문자는 $S$의 문자열이다.



**Proof:**

1. $c$가 $A$의 문자라고 가정하자.
2. $\mathrm{I}$의 문자열의 정의에 의하여, $\lambda$는 $S$의 문자열이다.
3. $\mathrm{II(a)}$의 문자열의 정의에 의하여, $\lambda c$는 $S$의 문자열이다.
4. $\mathrm{I}$의 문자열의 정의에 의하여, $\lambda c=c$이다.
5. 그러므로 $c$는 $S$의 문자열이다.



**Structural Induction for a Recursively Defined Set**

$S$가 재귀적으로 정의된 집합이며, $P(x)$가 $S$의 객체가 만족할 수도, 만족하지 않을 수도 있는 property라고 하자. $S$의 모든 객체가 $P(x)$를 만족한다고 증명하기 위해서, 다음의 두 단계를 수행해야 한다.

**Step 1(basic step)**: $P(a)$가 $S$에 기초하는 각각의 객체 $a$에 대하여 참임을 보여라.

**Step2 (inductive step)**: $S$의 각각의 $x$에 대하여, $P(x)$가 참이고 $y$가 recursion으로부터 규칙을 적용하여 $x$로부터 얻은 것이면, $P(y)$가 참임을 보여라. 이 단계를 수행하기 위해,

​			$x$가 $P(x)$가 참이게 하는 $S$의 임의로 선택된 요소라고 **가정하라.** (이 가정을 ***inductive hypothesis***라고 한다.) 그리고

​			$y$가 $S$에 대한 recursion으로부터 규칙을 적용하여 $x$로부터 얻은 것이면, $P(y)$가 참임을 **보여라.**

**Conclusion:** 그 어떤 객체도 base와 recursion으로부터 얻어진 객체 이외에 $S$에 포함되지 않으므로, step1과 step2는 $P(x)$가 $S$의 모든 객체 $x$에 대해 참임을 증명한다.



**Definition Length of a String**

유한한 집합 $A$에 대해 모든 문자열의 집합 $S$이 주어졌을 때, ***$S$의 문자열의 길이 $L$***은 다음과 같이 정의된다:

1. $L(\lambda)=0$
2. $S$의 모든 문자열 $u$과 $A$의 모든 문자 $a$에 대하여, $ua$의 길이는 $u$의 길이보다 1만큼 더 길다. 기호화하면,

$$
L(ua)=L(u)+1\quad(u\in S\ 그리고\ a\in A)
$$



**Theorem 5.9.2 Additive Property of String Length**

$S$가 유한한 집합 $A$에 대한 모든 문자열의 집합이면, $S$의 모든 문자열 $u$와 $v$에 대하여, $L(uv) = L(u)+L(v)$이다.



**Proof(by structural induction)**: $S$가 유한한 집합 $A$에 대한 모든 문자열의 집합이라고 하자. $S$의 주어진 모든 문자열 $v$에 대하여, $P(v)$가 다음과 같은 문장이라고 하자.
$$
S의\ 모든\ 문자열\ u에\ 대하여,\quad L(uv)=L(u)+L(v)
$$
$P(v)$는 $S$의 모든 문자열 $v$에 대하여  참이다.



**$P(a)$가 $S$에 기초한 각각의 문자열 $a$에 대하여 참임을 보여라:**

$S$에 기초한 유일한 문자열은 $\lambda$이고, $u$가 $S$의 모든 문자열이면,
$$
\begin{align*}
L(u\lambda)&=L(u) \\
&=L(u)+0 \\
&=L(u)+L(\lambda)
\end{align*}
$$
이것은 $P(\lambda)$가 참임을 보인다.



**$S$의 각각의 문자열 $x$에 대하여, $P(x)$가 참이고 $y$가 $S$에 대한 recursion으로부터 규칙을 적용하여 $x$로부터 얻은 것이면, $P(y)$가 참임을 보여라:**

$S$에 대한 recursion은 $\mathrm{II(a)}$, $\mathrm{II(b)}$, 그리고 $\mathrm{II(c)}$로 표기하는 세 개의 규칙으로 구성되어있다. 그러나 규칙 $\mathrm{II(a)}$만이 $S$의 새로운 문자열을 생성하는 규칙이다. $v$가 $P(v)$를 참이게 하는 그러한 $S$의 모든 문자열이라고 하자. 달리 말하여, $L(uv)=L(u)+L(v)$라고 가정하자.

$\mathrm{II(a)}$을 $v$에 적용했을 때, 결과는 $vc$이며, $c$는 $A$의 문자이다. 그러므로, inductive step을 완전히 하기 위해 $P(vc)$가 참임을 보여야한다.
$$
\begin{align*}
L(u(vc))&=L((uv)c) &\mathrm{II(a)}의\ 문자열의\ 정의에\ 의하여\\
&=L(uv)+1 &문자열의\ 길이의\ 정의에\ 의하여\\
&=(L(u)+L(v))+1 &u가\ P를\ 만족한다고\ 가정했으므로\\
&=L(u)+(L(v)+1) &덧셈\ 결합\ 법칙\\
&=L(u)+L(vc) &문자열의\ 길이의\ 정의에\ 의하여
\end{align*}
$$
그러므로 $P(vc)$는 참이다.

**Conclusion**:

$S$에 대한 recursion과 base로부터 얻은 문자열 이외에는 $S$에 어떤 문자열도 없으므로, $S$의 모든 문자열이 문자열 길에 대한 추가적인 property를 만족한다고 결론지을 수 있다.



**Theorem 5.9.3 Tjhe Concatenation of Any Tow Strings Is a String**

$S$가 유한한 집합 $A$에 대한 모든 문자열의 집합이고 $u$와 $v$가 $S$의 모든 문자열이면, $uv$는 $S$의 문자열이다.



**Proof (by structural indcution)**: $S$가 유한한 집합 $A$에 대한 모든 문자열의 집합이라고 하자. $S$의 모든 문자열 $v$에 대하여, $P(v)$가 다음과 같은 문장이라고 하자.
$$
S의\ 모든\ 문자열\ u에\ 대하여,\ uv는\ S의\ 문자열이다.
$$
$P(v)$가 $S$의 모든 문자열 $v$에 대하여 참임을 보여야 한다.



**$P(a)$가 $S$에 기초한 각각의 문자열 $a$에 대하여 참임을 보여라:**

$S$에 기초한 유일한 문자열은 $\lambda$이고 $u$가 $S$의 모든 문자열이면, 문자열의 정의 안의 규칙 $\mathrm{II(a)}$에 의하여, $u\lambda=u$이다. 그러므로 $u$와 $\lambda$의 conactenation은 $S$ 안의 문자열이고, 따라서 $P(\lambda)$는 참이다.



**$S$의 각각의 문자열 $x$에 대하여, $P(x)$가 참이고 $y$가 $S$에 대한 recursion으로부터 규칙을 적용하여 $x$로부터 얻은 것이면, $P(y)$가 참임을 보여라:**

$S$에 대한 recursion은 $\mathrm{II(a)}$, $\mathrm{II(b)}$, 그리고 $\mathrm{II(c)}$로 표기하는 세 개의 규칙으로 구성되어있다. 그러나 규칙 $\mathrm{II(a)}$만이 $S$의 새로운 문자열을 생성하는 규칙이다. $v$가 $P(v)$를 참이게 하는 그러한 $S$의 모든 문자열이라고 하자. 달리 말하여, $S$의 모든 문자열 $u$에 대하여, $uv$가 $S$의 문자열이라고 가정하자.

$\mathrm{II(a)}$을 $v$에 적용했을 때, 결과는 $vc$이며, $c$는 $A$의 문자이다. 그러므로, inductive step을 완전히 하기 위해 $P(vc)$가 참임을 보여야한다. 그러기 위해서, $u(vc)$가 $S$의 문자열임을 보여야 한다.

한편 $uv$는 $S$의 문자열이므로, 규칙 $\mathrm{II(a)}$에 의하여 $(uv)c$도 $S$의 문자열이다. 게다가, 규칙 $\mathrm{II(b)}$에 의하여,
$$
(uv)c=u(vc)
$$
그러므로, $u(vc)$는 $S$의 문자열이며, 이는 $P(vc)$가 참임을 의미한다.



**Conclusion**:

$S$에 대한 recursion과 base로부터 얻은 문자열 이외에는 $S$에 어떤 문자열도 없으므로, $S$ 안의 모든 두 개의 문자열의 concatenation이 $S$의 문자열이라고 결론지을 수 있다.



**Theorem 5.9.4 Concatenation of Strings Is Associative**

$S$가 유한한 집합 $A$에 대한 모든 문자열의 집합이고 $u$와 $v$, $w$가 $S$의 모든 문자열이면, $u(vw)=(uv)w$이다.



**Idea of a proof by structural induction:**

$S$가 유한한 집합 $A$에 대한 모든 문자열의 집합이라고 하자. $S$의 모든 문자열 $w$에 대하여, $P(w)$가 다음과 같은 문장이라고 하자.
$$
S의\ 모든\ 문자열\ w에\ 대하여,\ u(vw)=(uv)w
$$
증명은 (1) $P(\lambda)$가 참이다 그리고 (2) $w$가 $P(w)$를 만족시키는 그러한 $S$의 문자열이고 $y$가 $S$에 대한 recursion으로부터 규칙을 적용하여 $w$로부터 얻은 것이면, $P(y)$가 참이다 를 보여야 한다. 한편 규칙 $\mathrm{II(a)}$이 $w$에 적용되었을 때, 결과는 $A$ 안의 어떤 문자 $c$에 대한 $wc$이다. 중요한 단계는 $u(vw)=(uv)w$를 보이는 것이다. 이것은 $u$와 $vw$이 $S$에 속하고 $c$는 $A$에 속하므로 문자열의 정의로부터 비롯된다.

완전한 증명은 너가 써봐라.



**5.9.2 Recursive Functions**

- 함수는 그것의 정의의 규칙이 그 자신을 가리킬 때 **defined recursively(재귀적으로 정의되었다)** 거나 **recursive function(재귀적인 함수)**라고 불린다.

