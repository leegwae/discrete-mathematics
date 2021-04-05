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


**Definition[$n$ choose $r$]**

$n$과 $r$이 $0\le r\le n$인 정수라고 하자.
$$
{n \choose r}
$$
은 **$n$ choose $r$**이라고 읽으며, $n$개의 element를 가진 집합으로부터 $r$개 만큼 선택한 부분집합의 수를 나타낸다.



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



## 5.2 Mathematical Induction 2: Proving Formulas

**Principle of Mathematical Indunction**

$P(n)$이 정수 $n$에 대해 정의된 property이고, $a$가 fixed integer라고 한다. 다음의 두 statement를 참이라고 가정한다.

(1) $P(a)$는 참이다.

(2) $k\ge a$($a$보다 큰 모든 정수 $k$)에 대하여, $P(k)$가 참이면 $P(k+1)$도 참이다.

그리하여 statement "정수 $n\ge a$($a$보다 큰 모든 정수 $n$)에 대하여, $P(n)$이다." 는 참이다.



**Method of Proof by Mathematical Induction**

"정수 $n\ge a$에 대하여, property $P(n)$은 참이다."라는 형태의 statement를 생각해보자. 이러한 statement를 증명하기 위해서 다음의 두 단계가 필요하다.

(1) $P(a)$가 참임을 보인다.

(2)  $k\ge a$($a$보다 큰 모든 정수 $k$)에 대하여, $P(k)$가 참이면 $P(k+1)$도 참임을 보인다. 이 단계를 수행하기 위해서

​	$P(k)$가 $k$가 $k\ge a$이며 any particular한 것이지면 임의로 특정된 참이라고 **가정한다.** 이러한 가정을 **inductive hypothesis(귀납적 가설)**이라고 한다.

 그리고 $P(k+1)$이 참임을 보여라.



**Theorem 5.2.1 Sum of the First $n$ Integers**

1보다 큰 모든 정수 $n$에 대하여(For every integer $n\ge1$) 다음이 성립한다.
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



**1보다 큰 모든 정수 $k$에 대하여, $P(k)$가 참이면 $P(k+1)$ 또한 참임을 보여라.**

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
$P(n)$이 0보다 큰 모든 정수 $n$에 대하여 참임을 보여야한다. $n$에 대하여 수학적 귀납을 진행할 것이다.

**P(0)이 참임을 보여라**: $P(0)$을 증명하기 위해, 다음을 보여야 한다.
$$
\sum_{i=0}^0 r^i=\frac{r^{0+1}-1}{r-1}
$$
항등식의 좌변은 $r^0=1$이고
$$
\frac{r^{0+1}-1}{r-1} =\frac{r-1}{r-1}
$$
$r\ne 1, r\ne0$이므로 $r^1=1$이고, 따라서 $r^1=1$우변은 1이다. 그러므로 $P(0)$은 참이다.

**0보다 큰 모든 정수 $k$에 대하여, $P(k)$가 참이면 $P(k+1)$도 참임을 보여라**:

$k$가 0보다 큰 정수라고 한다. 또한 $P(k)$가 다음과 같다고 하자.
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
