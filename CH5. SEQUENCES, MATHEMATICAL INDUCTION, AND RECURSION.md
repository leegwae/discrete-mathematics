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