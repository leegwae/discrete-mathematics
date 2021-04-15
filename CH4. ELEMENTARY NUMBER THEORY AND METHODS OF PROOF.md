#  CH4. ELEMENTARY NUMBER  THEORY AND METHODS OF PROOF

**4.1 Direct Proof and Counterexample 1 : Introduction**

**4.1.1 Even, Odd, Prime, and Composite Integers**

**Definitions[Even, Odd]**

정수 $n$이 **even(짝수)**이다는 $n$이 어떤 정수의 두 배와 같을 때, 그리고 오직 이 경우에만 참이다. 정수 $n$이 **odd(홀수)**이다는 $n$이 어떤 정수의 두 배에 1을 더한 것과 같을 때, 그리고 오직 이 경우에만 참이다.

기호로 표현하면, 모든 정수 n에 대하여,
$$
\begin{align*}
n\mathrm{은\ 짝수다}
&\Leftrightarrow
\mathrm{어떤\ 정수\ }k\mathrm{에\ 대하여\ } n=2k\mathrm{이다}. \\

n\mathrm{은\ 홀수다}
&\Leftrightarrow
\mathrm{어떤\ 정수\ }k\mathrm{에\ 대하여\ } n=2k+1\mathrm{이다}.
\end{align*}
$$



**Definition[Prime, Composite]**

정수 $n$은 **prime(소수)**이다는 $n>1$이고 모든 양의 정수 $r$과 $s$에 대하여 $n=rs$일 때 $r$ 혹은 $s$이 $n$가 같은 경우, 그리고 오직 이 경우에만 참이다. 정수 $n$은 **composite(합성수)**이다는 $n>1$이고 어떤 정수 $r$과 $s$가 $1<r<n$이고 $1<s<n$인 경우, 그리고 오직 이 경우에만 참이다.

기호로 표현하면 다음과 같다: $n>1$인 정수 $n$에 대하여,
$$
\begin{align*}
n\mathrm{은\ 소수다}
&\Leftrightarrow \forall\ 양의\ 정수\ r과\ s에\ 대하여,\ n=rs이면\\
&\quad\quad r=1이고\ s=n이거나\ r=n이고\ s=1이다. \\

n\mathrm{은\ 합성수다}
&\Leftrightarrow \exist\ 양의\ 정수\ r과\ s에\ 대하여, n=rs이고 \\
&\quad\quad1<r<n이고\ 1<s<n이다.
\end{align*}
$$









**4.1.2 Proving Existential Statements**
$$
\exist x\in D\mathrm{\ such\ that\ }Q(x)
$$

- **constructive proofs**
  - 첫번째 방법: $Q(x)$를 참으로 만드는 $D$ 안의 $x$를 찾기
  - 두번째 방법: $x$과 같은 것을 가리키는 집합을 주기(to give a set  of directions for finding such an $x$)
- **existential generalization**
  - 위 증명에 기반한 논리 원칙을 **existential generalization**이라고 한다.

- **nonconstructive proof of existence**
  - nonconstructive proof of existence는 (a) 혹은 (b)를 보여주는 것을 포함한다.
  - (a) $Q(x)$를 참이게 하는 $x$의 값의 존재가 공리(axiom)나 증명된 정리(proved theorem)에 의해 보장된다.
  - (b) 그러한 $x$가 없는 가정(assumption)는 모순(contradiction)으로 이어진다.
  - 단점: $x$를 어디서 어떻게 찾을 수 있을 것인지에 대한 단서를 사실상 찾을 수 없을 것이다.



**4.1.3 Disproving Universal Statements by Counterexample**

**Disproof by Counterexample**

$\forall x\in D,\ P(x)이면\ Q(x)이다.$ 형태의 statement가 틀리다는 것을 증명하려면, 가설 $P(x)$가 참이고 결론 $Q(x)$가 거짓인 $D$ 안의 $x$를 찾아야한다. 이러한 $x$를 **counterexample(반례)**라고 한다.



**4.1.4 Proving Universal Statement**

예시



**Theorem 4.1.1**

두 짝수 정수(any two even integers)의 합은 짝수이다.

**Proof**

$m$과 $n$이 *[particular but arbitrarily chosen]* 짝수 정수라고 하자.

짝수의 정의에 의하여, 어떤 $r$와 $s$에 대하여 $m=2r$ 그리고 $n=2s$이다.
$$
\begin{align*}
m+n &= 2r+2s &치환\\
&= 2(r+s) &2로\ 묶기
\end{align*}
$$
$t=r+s$라고 하자. $t$는 정수의 합이므로 정수이다.
$$
m+n=2t\quad 여기서\ t는\ 정수이다.
$$
$m+n$가 짝수라는 짝수의 정의에 의하여 도출된다.



**Generalizing from the Generic Particular**

집합의 *every(모든)*  element가 특정 property를 만족한다는 것을 증명하려면, $x$를 집합의 *particular(특정)*하지만 *arbitrarily chosen(임의로 선택)* 한 element로 가정하고, $x$가 그 property를 만족한다는 것을 보여야한다.



**Existential Instantiation**

만약 특정 종류의 object의 존재가 가정되거나 추론되었다면, 동일한 논의에서 다른 것을 위하여 쓰이지 않는 한 어떠한 이름을 object에 붙일 수 있다.



예시



**4.2 Direct Proof and Counterexample 2: Writing Advice**

**4.2.1 Directions for Writing Proofs of Universal Statements**

**4.2.2 Variations among Proofs**

**4.2.3 Common Mistakes**

예제들



**Theorem 4.2.1**

홀수 정수(any odd integer)와 짝수 정수(any even integer)의 차는 홀수이다.

**proof**

1. $a$는 홀수 정수(any odd integer)이고 $b$는 짝수 정수(any even integer)라고 하자.

2. 홀수의 정의에 의하여 어떤 정수 $r$에 대하여 $a=2r+1$이고, 어떤 정수 $s$에 대하여 $b=2s$이다.

3. $$
   \begin{align*}
   a-b &= (2r+1) -2s &치환 \\
   &= 2r-2s+1 & \mbox{by combining like terms} \\
   &= 2(r-s)+1 & 2로 묶기 \\
   t &= r-s
   \end{align*}
   $$

4. $t$는 정수의 차이므로 정수이다.

5. 치환하면, $t$가 정수인 곳에서 $a-b=2t+1$

6. 그러므로 $a-b$는 홀수이다.



**4.3 Direct Proof and Counterexample 3: Rational Numbers**

**Definition[Rational]**

실수 $r$이 **rational(유리수)**이다는 0이 아닌 denominator(분모)를 가진 두 개의 quotient(몫)으로 표현될 수 있을 때, 그리고 오직 이 경우에만 참이다. 유리수가 아닌 실수는 **irrational(무리수)**이다. 

더 형식적으로, $r$이 실수이면,
$$
r은\ 실수이다\Leftrightarrow\exist\ 정수\ a와\ b에\ 대하여,\ r=\frac{a}{b}이고\ b\ne0이다.
$$

**Zero Product Property**

두 개의 실수 모두 0이 아니면, 이들의 곱 또한 0이 아니다.



**4.3.1 More on Generalizing from the Generic Particular**

- 논증을 증명하기 위해서, property가 domain의 *arbitrarily chosen(임의로 선택된)* element에 대해 참이라는 것을 증명해야한다.



**Theorem 4.3.1**

모든 정수는 유리수이다.



**4.3.2 Proving Properties of Rational Numbers**

예제들



**Theorem 4.3.2**

두 유리수(any tow rational)의 합은 유리수이다.

**Proof**

$r$과 $s$가 유리수(any rational numbers)라고 하자. 유리수의 정의에 의하여, $b\ne0$이고 $d\ne0$인 어떤 정수 $a,b,c,d$에 대하여 $r=a/b$이고  $s=c/d$이다. 그러므로
$$
\begin{align*}
r+s&=\frac{a}{b}+\frac{c}{d} &치환 \\
&=\frac{ad+bc}{bd}&대수학
\end{align*}
$$
$p=ad$이고 $q=bd$라고 하자. 정수의 곱과 합은 정수이고 $a,b,c,d$는 정수이므로 $p$와 $q$도 정수이다. 또한 zero product property에 의하여 $q\ne0$이다. 그러므로
$$
r+s=\frac{p}{q}\quad 여기서\ p와\ q는\ 정수이고\ q\ne0이다.
$$
그러므로, 유리수의 정의에 따라서 $r+s$는 유리수이다.



**4.3.3 Deriving New Mathematics from Old**

**corollary**는 이미 증명된 정리로부터 즉시 유도될 수 있는 참인 statement이다.



**예시 4.3.4 The Double of a rational Number**

**Corollary 4.2.3**

rational number의 두 배는 rational이다.



**4.4 Direct Proof and Counterexample 4: Divisibility**

가분성(divisibility)의 개념은 **number theory**의 중요한 개념 중 하나이다.



**Definition[divisible]**

$n$과 $d$가 정수이면

$n$은 0이 아닌 $d$와 어떤 정수를 곱한 것과 같은 경우, 그리고 오직 이 경우에만 $d$로 **나누어떨어진다(divisible by)**고 한다.

"$n$은 $d$에 의해 나누어떨어진다" 대신에 다음과 같이 말할 수 있다.

$n$은 $d$의 **배수이다(is a multiple of)** 

$d$는 $n$의 **인수이다(is a factor of)**

$d$는 $n$의 **약수(is a divisor of)**이다.

$d$는 $n$을 **나눈다(divides)**

**$d|n$**이라는 표기법은 "$n$은 $d$로 나누어떨어진다($d$ divides $n$)"로 읽는다. 기호화하면 다음과 같다. $n$과 $d$가 정수이면:
$$
d|n\quad\Leftrightarrow\quad\exist\ 정수\ k에\ 대하여,\ n=dk\ 그리고\ d\ne0이다.
$$
$d\nmid n$이라는 표기법은 "$n$은 $d$"로 나누어떨어지지 않는다($d$ dose not divide $n$)고 읽는다.



**4.4.1 Proving Properties of Divisibility**

**Theorem 4.4.1 [A Positive Divisor of a Positive Integer]**

모든 정수 $a$와 $b$에 대하여, $a$와 $b$가 양수이고 $b$가 $a$로 나누어떨어지면 $a\le b$.

**Proof**

$a$와 $b$가 $b는\ a로\ 나누어떨어진다$를 만족하는 그러한 양의 정수라고 하자. divisibility의 정의에 의하여, $b=ak$를 만족하는 정수 $k$가 존재한다. 

$a$와 $b$ 모두 양수이므로 $k$도 양수이다. 이는 다음과 같은 실수의 property(A-T25)로부터 도출된다.
$$
ab>0이면\ a와\ b는\ 둘\ 다\ 양수이거나, 둘\ 다\ 음수이다.
$$
모든 양의 정수는 1보다 크거나 같으므로 다음이 도출된다.
$$
1\le k
$$
$a$를 양변에 곱하면 다음과 같다.
$$
a\le ka =b
$$
양수로 inequality한 양변을 곱하는 것은 inequality를 보존하기 때문이다. 이는 다음과 같은 실수의 property(A-T20)로부터 도출된다.
$$
a<b이고\ c>0이면,\ ac<bc이다.
$$
그러므로 $a\le b$이다.



**Theorem 4.4.2 Divisor of 1**

1의 약수는 1과 -1뿐이다.

**Proof**

$1\cdot 1 = 1$이고 $-1\cdot -1 = 1$이므로 1과 -1은 1의 divisor(약수)이다. $m$이 1의 약수인 정수라고 하자. $1=mn$을 만족하는 그러한 정수 $n$이 존재한다. $m$과 $n$은 둘 다 양수이거나, 둘 다 음수이므로(A-T25),  $m$과 $n$이 둘 다 양수라면, $m$은 1의 양의 정수인 약수이다. 정리 [4.4.1] 에 의하여, $m\le 1$이다. 또한 1보다 작거나 같은 양의 정수는 오직 1 그 자신밖에 없으므로 $m=1$이다. 반대로 $m$과 $m$이 둘 다 음수라면, $(-m)(-n) = mn = 1$이다. 이는 다음과 같은 실수의 property(A-T12)로부터 도출된다.

*Rule for Multiplication with Negative Signs*
$$
(-a)b = a(-b) = -(ab),\quad(-a)(-b) = ab
$$

$$
-\frac{a}{b}=\frac{-a}{b}=\frac{a}{-b}
$$

이 경우 $-m$은 1의 정수 양수 약수이며, 같은 이유로 $-m=1$이다. 그러므로 오직 두 가능성만이 존재한다: $m=1$이거나 $m=-1$이다. 그러므로 1의 약수는 오직 1과 -1뿐이다.



**4.4.2 Proving Properties of Divisibility**

**Theorem 4.4.3 [Transitivity of Divisibility]**

정수 $a$, $b$, $c$에 대하여, $b$가 $a$로 나누어떨어지고 $c$가 $b$로 나누어떨어진다면 $c$는 $a$로 나누어떨어진다.

**Proof**

$a$, $b$, $c$가 $b$는 $a$로 나누어떨어지고 $c$가 $b$로 나누어떨어지는 모든 *[particular but arbitrarily chosen]* 정수라고 하자. divisibility의 정의에 의하여,
$$
어떤\ 정수\ r과\ s에\ 대하여,\ b=ar\ 이고\ c=bs이다.
$$
치환하면
$$
\begin{align*}
c &=bs\\
&=(ar)s\\
&=a(rs)
\end{align*}
$$
$k=rs$라고 하자. $k$는 정수의 곱이므로 정수이다. 그러므로
$$
c=ak\quad 여기서\ k는\ 정수이다.
$$
그러므로 divisibility의 정의에 의하여 $c$는 $a$로 나누어떨어진다.



**Theorem 4.4.4 Divisibility by a Prime**

정수(any integer) $n>1$은 소수에 의해 나누어떨어질 수 있다.

**Proof**

$n$이 1보다 큰 정수라고 하자.

(1) $n$이 소수이면, $n$은 소수로 divisible하다. $n$이 소수가 아니라면,  다음과 같다.
$$
n=r_0s_0\quad r_0과\ s_0은\ 정수이며\ 1<r_0<n\ 그리고\  1<s_0<n이다.
$$
(2) $r_0$이 소수이면, $r_0$은 $n$을 나눌 수 있는 소수이다. $r_0$이 소수가 아니면, 다음과 같다.
$$
r_0=r_1s_1\quad r_1과\ s_1은\ 정수이며\ 1<r_1<r_0\ 그리고\  1<s_1<r_0이다.
$$
이것은 $r_1|r_0$인 divisibility의 정의로부터 도출된다. $r_0|n$은 알고있으므로, transitivity of divisibility에 의하여 $r_1|n$이다.

(3) $r_1$이 소수이면, $r_1$은 $n$을 나눌 수 있는 소수이다. $r_1$이 소수가 아니면 다음과 같다.
$$
r_1=r_1s_2\quad r_2과\ s_2은\ 정수이며\ 1<r_2<r_1\ 그리고\  1<s_2<r_1이다.
$$
이것은 $r_2|r_1$인 divisibility의 정의로부터 도출된다. $r_1|n$은 알고있으므로, transitivity of divisibility에 의하여 $r_2|n$이다.

(4) $r_2$이 소수이면, $r_2$은 $n$을 나눌 수 있는 소수이다. $r_2$이 소수가 아니라면, $r_3s_3$으로 $r_2$를 인수분해하여 위와 같은 과정을 반복한다.

이 과정을 반복하면 다음과 같은 sequence를 얻을 수 있다.
$$
r_0,r_1,r_2,...,r_k
$$
여기서 $k\ge 0,\ 1<r_k<r_{k-1}<...<r_2<r_1<r_0<n$그리고 각각의 $i=0, 1, ..., k$에 대하여 $r_i|n$이다. termination의 조건은 $r_k$가 소수여야한다. 그러므로 $r_k$는 $n$을 나눌 수 있는 소수이다.



**4.4.3 Counterexamples and Divisibility**

**Proposed Divisibility Property**

모든 정수 $a, b$에 대하여, $a|b$이고 $b|a$이면 $a=b$이다.

**Counterexample**

$a=2$이고 $b=-2$라고 하자. $-2=(-1)\cdot 2$ 그리고 $2 = (-1)\cdot (-2)$이다. 그러므로
$$
a|b\ 그리고\ b|a,\ 하지만\ 2\ne -2이므로\ a\ne b이다.
$$


**4.4.4 The Unique Factorization of Integers Theorem**

**Theorem 4.4.5 Unique Factorization of Integers Theorem(Fundamental Theorem of Arithmetic)**

주어진 정수(any integer) $n>1$에 대하여, 다음을 만족하는 양의 정수 $k$와 서로 다른 유리수 $p_1,p_2,...p_k$, 양의 정수 $e_1,e_2,...,e_k$가 존재한다.
$$
n=p_1^{e_1}p_2^{e_2}p_3^{e_3}...p_k^{e_k}
$$
또한 소수의 곱으로서의 $n$에 대한 다른 expression은 인수들이 쓰여진 순서를 제외하면 동일하다.



**Definition[standard factored form]**

주어진 정수(any integer) $n>1$에 대하여, $b$의 **standard factored form**은 다음과 같은 형태의 expression이다.
$$
n=p_1^{e_1}p_2^{e_2}p_3^{e_3}...p_k^{e_k}
$$
여기서 $k$는 양의 정수, $p_1,p_2,...p_k$는 prime number, $e_1,e_2,...,e_k$는 양의 정수, $p_1<p_2<...<p_k$이다.



**4.5 Direct Proof and Counterexample 5: Division into Cases and the Quotient-Remainder Theorem**

**Theorem 4.5.1 The Quotient-Remainder Theorem**

주어진 정수(any integer) $n$과 양의 정수 $d$에 대하여, 다음을 만족하는 유일한 정수 $q$와 $r$이 존재한다.
$$
n=dq+r\quad 그리고\quad 0\le r< d
$$


**4.5.1 div and mod(나눗셈과 나머지)**

**Definition[div, mod]**

주어진 정수 $n$과 양의 정수 $d$에 대하여
$$
\begin{align*}
n\ div\ d &= n이\ d에\ 의해\ 나누어질때\ 정수인\ 몫을\ 얻는다. \\
n\ mod\ d &= n이\ d에\ 의해\ 나누어질때\ 음수가\ 아닌\ 정수인\ 나머지를\ 얻는다.
\end{align*}
$$
기호화하면, $n$과 $d$가 정수이고 $d>0$이면,
$$
n\ div\ d = q\quad 그리고\quad n\ mod\ d = r\Leftrightarrow n=dq+r
$$
이때 $q$와 $r$은 정수이며 $0\le r< d$이다.



**4.5.2 Representations of Integers**

(a) 짝수는 어떤 정수의 두 배이다. 홀수는 짝수가 아닌 수이다. (4.1) 

(b) 또는, 홀수는 어떤 정수의 두 배 더하기 1이다.



**quotient-remainder theorem 증명하기**

**(a)로 증명하기**

$n$이 (any) 정수라고 하고 2로 나누어보자. 몫-나머지 정리에 의하여(이때 $d=2$), 다음을 만족하는 유일한 정수 $q$와 $r$이 있다.
$$
n=2q+r\quad 그리고\quad 0\le r\le 2
$$
그러나 $0\le r\le 2$을 만족하는 정수는 $r=0$과 $r=1$ 뿐이다.

**(b)로 증명하기**

주어진 (any) 정수 $n$에 대하여, 다음을 만족하는 정수 $q$가 존재한다.
$$
n=2q+0\quad\mathrm{or}\quad n=2q+1
$$
$n=21+0=2q$의 경우, $n$은 짝수이다. $n=2q+1$의 경우, $n$은 홀수이다. 그러므로 $n$은 정수이거나 홀수이며, $q$와 $r$의 uniqueness(고유성) 때문에 짝수이면서 홀수일 수 없다.

정수의 ***parity***는 정수가 홀수인지 짝수인지를 가리킨다. 예를 들어, 5는 odd parity이며 20는 even parity이다. 



**Theorem 4.5.2 The Parity Property**

두 개의 consecutive(연속적인) 정수는 opposite(서로 다른) parity를 가진다.

**Proof**

두 개의 연속적인 정수 $m, m+1$이 있다 하자. parity property에 의해, $m$은 짝수이거나 $m$은 홀수 이다.

***Case1 ($m$이 짝수인 경우)***: 이 경우, 어떤 정수 $k$에 대하여 $m=2k$이고 $m+1 = 2k+1$이며 이것은 홀수의 정의에 의하여 홀수이다. 그러므로 $m$과 $m+1$ 둘 중 하나는 짝수이고 다른 하나는 홀수이다.

***Case2 ($m$이 홀수인 경우)***: 이 경우, 어떤 정수 $k$에 대하여 $m=2k+1$이고 $m+1 = (2k+1) +1 = 2k+2 = 2(k+1)$이다. 그런데 $k+1$은 두 정수의 합이므로 정수이다. 그러므로, $m+1$은 어떤 정수의 두 배와 같으므로, $m+1$은 짝수이다, 그러므로 $m$과 $m+1$ 둘 중 하나는 짝수이고 다른 하나는 홀수이다.



- proof의 case로 나누는 것은 computer program의 **if-then-else** statement와 같다.

**Method of Proof by Division into Cases**

"만약 $A_1, A_2,..., A_n이면,\ C이다.$" 형태의 statement를 증명하기 위해서 다음을 모두 증명해야한다.
$$
\mathrm{If\ }A_1,\mathrm{\ then\ }C, \\
\mathrm{If\ }A_2,\mathrm{\ then\ }C, \\
\vdots \\
\mathrm{If\ }A_n,\mathrm{\ then\ }C.
$$
이것은 $A_1, A_2,..., A_n$가 case였는지의 여부에 상관없이 $C$가 참이라는 것을 보여준다.



**Theorem 4.5.3**

홀수 정수(any odd integer)의 제곱은 어떤 정수 $m$에 대하여 $8m+1$과 같은 형태를 가진다.

**Proof**

$n$을 홀수 정수라고 하자. 약수가 4와 같을 때 몫-나머지 정리에 의하면, $n$은 어떤 정수 $q$에 대하여 다음과 같은 형태로 쓸 수 있다.
$$
4q\quad 혹은\quad 4q+1\quad 혹은 \quad4q+2\quad 혹은\quad4q+3
$$
그런데 $n$은 홀수이고 $4q$와 $4q+2$는 짝수이므로, $n$은 다음과 같은 형태를 가진다.
$$
4q+1\quad 혹은\quad 4q+3
$$
***Case1(어떤 정수 $q$에 대하여 $n=4q+1$)***: $n=4q+1$이므로,
$$
\begin{matrix}
n^2 &=& (4q+1)^2\quad\quad\quad\quad\quad\quad\quad\quad\quad\quad치환 \\
	&=& (4q+1)(4q+1)\quad\quad제곱의\ 정의에\ 의하여 \\
	&=& 16q^2 + 8q+1\quad\quad\quad\quad\quad\quad\quad\quad\quad\quad \\
	&=& 8(2q^2+q)+1\quad\quad 대수학의\ 법칙에\ 의하여
\end{matrix}
$$
$m=2q^2+q$라고 하자. 2와 $q$는 정수이고 정수의 합과 곱은 정수이므로 $m$은 정수이다. 그러므로 치환하면
$$
m이\ 정수이며,\ n^2=8m+1이다.
$$
***Case2(어떤 정수 $q$에 대하여 $n =  4q+3$)***: $n=4q+3$이므로,
$$
\begin{align*}
n^2 &= (4q+3)^2 &치환 \\
	&= (4q+3)(4q+3) &제곱의\ 정의에\ 의하여 \\
	&= 16q^2 + 24q+9 \\
	&= 16q^2 + 24q+(8+1) \\
	&= 8(2q^3+q+1)+1 &대수학의\ 법칙에\ 의하여
\end{align*}
$$
$m=2q^2+3q+1$라고 하자. 1, 2, 3 그리고 $q$는 정수이고 정수의 합과 곱은 정수이므로 $m$은 정수이다. 그러므로 치환하면
$$
m은\ 정수이며,\ n^2=8m+1이다. 
$$
Case 1과 2는 주어진 홀수 정수에 대하여, $4q+1$의 형태이든지 $4q+3$의 형태이든지 어떤 정수 $m$에 대하여 $n^2=8m+1$이라는 것을 보여준다.



- 결론 다른 말로 : 모든 홀수 정수 $n$에 대하여, $n^2\ mod\ 8=1$이다.
- 일반적으로, 몫-나머지 정리에 의하여, 정수 $n$이 정수 $d$에 의해 나누어떨어질 수 있으면, 가능한 나머지는 0, 1, 2,...($d-1$)이다. 이것은 $n$을 다음과 같은 형태로 쓸 수 있다는 것을 의미한다.

$$
어떤\ 정수\ q에\ 대하여,\ dq,\ dq+1,\ dq+2,\ ...,\ dq+(d-1)
$$



**4.5.3 Absolute Value and the Triangle Inequality**

**Definition[Absolute Value]**

실수(any real number) $x$에 대하여, $x$의 **absolute value(절대값)**은 $|x|$로 표기하며 다음과 같이 정의한다.
$$
|x|=
\begin{cases}
x &(x\ge 0) \\
-x &(x < 0) \\
\end{cases}
$$
**lemma**

- **lemma**는 그리 중요하지는 않지만(much intrinsic interest) 다른 결론을 이끌어내는 데 도움이 되는 문장이다.



**Lemma 4.5.4**

모든 실수 $r$에 대하여, $-|r|\le r\le |r|$

**Proof**

$r$이 실수(any real number)라고 하자. 

***Case1(r=0)*** : 이 경우, 절대값의 정의에 의하여, $|r| =r = 0$이다. $0=-0$이기 때문에 $-0 = -|r| = 0 =r = |r|$이다. 따라서 다음은 참이다.
$$
-|r|\le r\le |r|
$$
***Case2(r>0)***: 이 경우, 절대값의 정의에 의하여, $|r|=r$이다. 또한 $r$이 양수이고 $-|r|$이 음수이므로 $-|r|< r$이다. 그러므로 다음은 참이다.
$$
-|r|\le r\le |r|
$$
***Case3(r<0)***: 이 경우, 절대값의 정의에 의하여, $|r|=-r$이다. 양변을 $-1$로 곱하면 $-|r|=r$이다. 또한, $r$이 음수이고 $|r|$이 양수이므로, $r<|r|$이다. 그러므로 다음은 참이다.
$$
-|r|\le r\le |r|
$$
그러므로 모든 경우에서 다음은 참이다.
$$
-|r|\le r\le |r|
$$


**Lemma 4.5.5**

모든 실수 $r$에 대하여, $|-r|=|r|$이다.

**Proof**

$r$을 실수(any real number)라고 하자. 다음은 A-T23의 내용이다.
$$
a<b이고\ c<0이면,\ ac>bc이다.
$$
이에 따르면, $r>0$이면 $-r<0$이다. $r<0$이면 $-r>0$이다. 그러므로
$$
\begin{align*}
|-r|&=
\begin{cases}
-r & (-r>0) \\
0 & (-r=0) \\
-(-r) & (-r<0) \\
\end{cases}\\

&=
\begin{cases}
-r & (-r>0) \\
0 & (r=0) \\
r & (-r<0) \\
\end{cases}\\

&=
\begin{cases}
-r & (r<0) \\
0 & (r=0) \\
r & (r>0) \\
\end{cases}\\

&=
\begin{cases}
r & (r\ge 0) \\
-r & (r<0) \\
\end{cases}\\

&=
|r|
\end{align*}
$$
**Lemma 4.5.6**

실수(all real numbers) $x$와 $y$에 대하여, $|x+y|\le |x|+|y|$이다.

**Proof**

$x$와 $y$가 실수(any real numbers)라고 가정한다.

***Case1($x+y\ge0$)***: 이 경우, $|x+y|= x+y$이고, [Lemma 4.5.4]에 의하여
$$
x\le |x|\quad그리고\quad y\le |y|.
$$
한편 다음은 A-T26의 내용이다.
$$
0<a<c이고\ \ 0<b<d이면,\ 0<ab<cd이다.
$$
A-T26에 의하여,
$$
|x+y|=|x+y|\le |x|+|y|
$$


***Case2($x+y<0$)***: 이 경우, $|x+y| = -(x+y) = (-x)+(-y)$이다. 또한 [Lemma 4.5.4와 4.5.5]에 의하여
$$
-x\le |-x| = |x|\quad그리고\quad -y\le|-y|=|y|.
$$
A-T26에 의하여,
$$
|x+y| = (-x)+(-y)\le |x|+|y|.
$$
그러므로 두 경우 모두에서 $|x+y|\le |x|+|y|$가 성립한다.



**4.6 Direct Proof and Counterexample 6: Floor and Ceiling**

**Definition[Floor]**

주어진 실수(any real number) $x$에 대하여, $x$의 **floor**은 $\lfloor x\rfloor$로 표기하며 다음과 같이 정의된다.
$$
\lfloor x\rfloor=n\mathrm{은\ }n\le x< n+1을\ 만족하는\ 유일한\ 정수
$$
기호화하면 다음과 같다. $x$가 실수이고 $n$이 정수이면,
$$
\lfloor x\rfloor=n\quad\Leftrightarrow\quad n\le x< n+1
$$
**Definition[Ceiling]**

주어진 실수 $x$에 대하여, $x$의 **ceiling​**은 $\lceil x\rceil$로 표기하며 다음과 같이 정의된다.
$$
\lceil x\rceil=n\mathrm{은\ }n-1< x\le n을\ 만족하는\ 유일한\ 정수
$$
기호화하면 다음과 같다. $x$가 실수이고 $n$이 정수이면,
$$
\lceil x\rceil=n\quad\Leftrightarrow\quad n-1< x\le n
$$


**Theorem 4.6.1**

실수 $x$와 정수 $m$에 대하여, $\lfloor x+m \rfloor=\lfloor x\rfloor+m$이다.

**Proof**

주어진 실수 $x$와 정수 $x$에 대하여 $n=\lfloor x \rfloor$이라고 하자. floor의 정의에 의하여, $n$은 정수이며 $n\le x <n+1$이다.

각 변에 $m$을 더하면 다음을 얻을 수 있다.
$$
n+m\le x+m <n+m+1
$$
$n,m$이 정수이며 정수의 합은 정수이므로 $n+m$은 정수이다. 그러므로, floor의 정의에 의하여 항등식의 좌변은 다음과 같이 볼 수 있다.
$$
\lfloor x+m \rfloor = n+m
$$
그런데 $n=\lfloor x\rfloor$이므로, 치환에 의하여 항등식의 우변은 다음과 같이 볼 수 있다.
$$
n+m=\lfloor x \rfloor +m
$$
그러므로 $\lfloor x+m \rfloor=\lfloor x\rfloor+m$이다.



**Theorem 4.6.2 [The Floor of n/2]**

정수 $n$에 대하여,
$$
\lfloor\frac{n}{2}\rfloor=
\begin{cases}
\frac{n}{2} &\mathrm{(n은\ 짝수)} \\
\frac{n-1}{2} &\mathrm{(n은\ 홀수)}
\end{cases}
$$
**Proof**

$n$은 정수라고 하자. 몫-나머지 정리에 의하여, $n$은 짝수이거나 $n$은 홀수이다.

**Case 1($n$은 홀수이다)**: 이 경우, 어떤 정수 $k$에 대하여 $n=2k+1$이다. $k$는 정수이며 $k\le k+1/2<k+1$이므로, 좌변은 다음과 같이 나타낼 수 있다.
$$
\lfloor\frac{n}{2}\rfloor
=\lfloor\frac{2k+1}{2}\rfloor
=\lfloor\frac{2k}{2}+\frac{1}{2}\rfloor
=\lfloor k+\frac{1}{2}\rfloor
=k
$$
우변 또한 다음과 같이 나타낼 수 있다.
$$
\frac{n-1}{2}
=\frac{(2k+1)-1}{2}
=\frac{2k}{2}
=k
$$
그러므로 좌변과 우변은 $k$와 같으므로, 서로도 같다.즉, $\lfloor\frac{n}{2}\rfloor=\frac{n-1}{2}$이다.

**Case2($n$은 짝수이다)**: 이 경우, 어떤 정수 $k$에 대하여 $n=2k$이다.

!! 이 뒤는 연습으로 풀어보기



**Theorem 4.6.3**

$n$이 정수이고 $d$가 양의 정수이면, 또한 $q=\lfloor n/d\rfloor$이고 $r=n-d\cdot\lfloor n/d\rfloor$이면, $n=dq+r$이고 $0\le r<d$이다.

**Proof**

$n$이 정수, $d$가 양의 정수, $q=\lfloor n/d\rfloor$이고 $r=n-d\cdot\lfloor n/d\rfloor$이라고 하자. 치환에 의하여,
$$
dq+r=d\cdot\lfloor\frac{n}{d}\rfloor+(n-d\cdot\lfloor\frac{n}{d}\rfloor)=n
$$
따라서 $q=\lfloor n/d\rfloor$는 증명된다. 

floor의 정의에 의하면,
$$
q\le \frac{n}{d}<q+1
$$
이다. 그리고
$$
\begin{align*}
dq&\le n < dq+d &d\mathrm{로\ 각\ 변을\ 곱한다} \\
0&\le n-dq <d &\mathrm{각\ 변에서\ }dq\mathrm{를\ 추출한다}
\end{align*}
$$
그런데
$$
r=n-d\lfloor\frac{n}{d}\rfloor=n-dq
$$
이다. 그러므로
$$
0\le r <d\quad 치환
$$
**4.7 Indirect Argument: Contradiction and Contraposition**

- indirect argument의 종류 (1) proof by contradiction (2) proof by contraposition

- *모순에 의한 논증(argument by contradiction)*은 statement가 참이거나 거짓이지만 참이면서 거짓일 수 없다는 사실에 기초한다.



**Method of Proof by Contradiction**

(1) 증명할 statement가 거짓이라고 가정한다. 즉, statement의 부정을 참이라고 가정한다.

(2) 위 가정이 논리적으로 모순임을 보인다.

(3) 증명할 statement는 참이다.



**Theorem 4.7.1**

가장 큰 정수는 없다(There is no greatest integer).

**Proof**

가장 큰 정수가 있으며, 모든 정수 $n$에 대하여 $N\ge n$이라고 하자. 또한 $M=N+1$이라고 하자. $M$은 정수의 합이므로 정수이다. 또한 $M=N+1$이므로 $M >N$이다. 그러므로 $M$은 $N$보다 큰 정수이다. 그리하여 $N$은 가장 큰 정수이며 $N$은 가장 큰 정수가 아니기도 한데 이것은 모순이다.



**Theorem 4.7.2**

짝수이면서 동시에 홀수인 정수는 없다(There is no integer that is both even and odd).

**Proof**

짝수이면서 동시에 홀수인 정수 $n$이 적어도 하나가 있다고 하자. 짝수의 정의에 의하여, 어떤 정수 $a$에 대하여 $n=2a$이며 홀수의 정의에 의하여, 어떤 정수 $b$에 대하여 $n=2b+1$이다. 결론적으로
$$
2a=2b+1\quad n\mathrm{에\ 대한\ 두\ expression을\ 등호로\ 표시한다}
$$
이므로
$$
\begin{align*}
2a-2b &= 1	\\
2(a-b) &= 1 \\
a-b&=1/2 &대수학에\ 의하여 \\
\end{align*}
$$
$a$와 $b$가 정수이므로, $a-b$의 차 또한 정수여야한다. 그러나 $a-b$는 $1/2$로 정수가 아니다. 그러므로 $a-b$는 정수이며 $a-b$는 정수가 아니게 되므로 이는 모순이다.



**Theorem 4.7.3**

유리수와 무리수의 합은 무리수이다(The sum of any rational number and any irrational number is irrational).

**Proof**

유리수 $r$과 무리수 $s$의 합이 유리수라고 하자. 유리수의 정의에 의하여, 어떤 정수 $b\ne0$이고 $d\ne0$인  $a,b,c,d$에 대하여 $r=a/b$와 $r+s=c/d$이다. 치환하면
$$
\frac{a}{b} +s=\frac{c}{d}
$$
그러므로
$$
\begin{align*}
s&=\frac{c}{d}-\frac{a}{b} \\
&=\frac{bc-ad}{bd}
\end{align*}
$$
$a,b,c,d$가 정수이고 정수의 합과 곱은 정수이므로 $bc-ad$와 $b-d$는 정수이다. 또한 zero product property에 의하여 $bd\ne0$이다. 그리하여 $s$는 두 정수 $bc-ad$와 $bd\ne0$인 $bd$의 몫이다. 그러므로, 유리수의 정의에 의하여, $s$가 무리수라는 가정은 모순이며 $s$는 유리수이다.



**4.7.1 Argument by Contraposition**

*대우에 의한 논증(argument by contraposition)*은 statement와 그것의 대우 간의 논리적 동등성(equivalence)에 기초한다.



**Method of Proof by Contraposition**

(1) 증명할 statement를 다음과 같은 형태로 표현한다.
$$
\forall x\mathrm{\ in\ D,\ if\ }P(x)\mathrm{\ then\ }Q(x)
$$
(2) 이 statement를 대우의 형태로 다시 쓴다.
$$
\forall x\mathrm{\ in\ D, if\ }Q(x)\mathrm{\ is\ false\ then\ }P(x)\mathrm{\ is\ false}
$$
(3) direct proof를 통해 contrapositive를 증명한다.

​	(a) $x$가 $Q(x)$를 거짓이게 하는 $D$의 요소라고 가정한다.

​	(b) $P(x)$가 거짓임을 보인다.



**Proposition(명제) 4.7.4**

모든 정수 $n$에 대하여, $n^2$이 짝수이면 $n$은 짝수이다.

**Proof(by contraposition)**

$n$이 홀수 정수(any odd integer)라고 하자. 홀수의 정의에 의하여, 어떤 정수 $k$는 $n=2k+1$이다. 치환과 대수학에 의하여,
$$
\begin{align*}
n^2&=(2k+1)^2 \\
&=4k^2+4k+1 \\
&=2(2k^2+2k)+1
\end{align*}
$$
정수의 곱과 합은 정수이므로 $2k^2+2k$는 정수이다. 그러므로 $n^2=2(정수)+1$이므로, 홀수의 정의에 의하여, $n^2$는 홀수이다.



**4.7.2 Relation between Proof by Contradiction and Proof by Contraposition**

- Proof by Contraposition
  - $x$가 $\sim Q(x)$를 만족하는 $D$의 임의의 요소라고 하자
  - $\sim P(x)$를 보인다.
- Proof by Contradiction
  - $P(x)$와 $\sim Q(x)$를 만족하는 $x$가 $D$에 존재한다고 하자
  - Contradiction: $P(x)$이며 $\sim P(x)$임을 보인다. 



**4.8 Indirect Argument: Two Famous Theorems**

**4.8.1 The Irrationality of $\sqrt{2}$**

**Theorem 4.8.1 [Irrationality of $\sqrt{2}$]**

$\sqrt{2}$는 무리수이다.

**Proof(by contradiction)**

$\sqrt{2}$를 유리수라고 가정하자. 공통 인수(common factor)가 없는 정수 $m$과 $n$이 다음을 만족한다고 하자.
$$
\begin{align*}
\sqrt{2}&=\frac{m}{n} &4.8.1\\
2&=\frac{m^2}{n^2} &4.8.1에서\ 양변을\ 제곱하였음 \\
m^2 &= 2n^2 &4.8.2
\end{align*}
$$
항등식 (4.8.2)는 짝수의 정의에 의하여 $m^2$가 짝수라는 것을 암시한다. 또한 Proposition 4.7.4에 의하여 $m$은 짝수다.
$$
\begin{align*}
m&=2k &k는\ 정수,\ 4.8.2 \\
m^2&=(2k)^2=4k^2=2n^2 &(4.8.3)으로\ 치환 \\
n^2&=2k^2 &양변을\ 2로\ 나눈다
\end{align*}
$$
그러므로, $n^2$은 짝수이며, Proposition 4.7.4에 의하여 $n$은 짝수이다. $m$도 짝수이다. 그리하여 $m$과 $n$은 공통 인수로 2를 가진다. 이것은 $m$과 $n$이 공통 인수를 가지지 않는다는 전제에 모순된다.



**Proposition 4.8.2**

$1+3\sqrt{2}$는 무리수이다.

**Proof**

$1+3\sqrt{2}$가 유리수라고 하자. 유리수의 정의에 의하여, 어떤 정수 $a$와 $b\ne 0$인 정수 $b$에 대하여
$$
\begin{align*}
1+3\sqrt{2}&=\frac{a}{b} \\
3\sqrt{2}&=\frac{a}{b}-1 &양변에\ 1을\ 더한다 \\
&=\frac{a}{b}-\frac{b}{b} &치환 \\
&=\frac{a-b}{b} &\mathrm{rule\ for\ subtracting\ fractions} \\
&&\mathrm{\ with\ a\ common\ denominator}
\end{align*}
$$
그리하여
$$
\begin{align*}
\sqrt{2}&=\frac{a-b}{3b} &양변을\ 3으로\ 나눈다
\end{align*}
$$
$a, b$는 정수이며 정수의 차와 곱은 정수이므로 $a-b$와 $3b$는 정수이다. 또한 zero product property에 의하여 $3b\ne 0$이다. 그리하여 $\sqrt{2}$은 두 정수 $a-b$와 $3b\ne 0$인 $b$의 몫이며, 유리수의 정의에 의하여 $\sqrt{2}$는 유리수이다. 이것은 $\sqrt{2}$가 무리수라는 사실에 모순된다. 그러므로 $1+3\sqrt{2}$는 무리수이다.



**4.8.2 Are there Infinitely Many Prime Numbers?**

**Proposition 4.8.3**

정수 $a$와 소수 $p$에 대하여, $p\mid a$이면 $p\nmid (a+1)$이다.

**Proof(by contradiction)**

$p|a$와 $p\nmid (a+1)$을 만족하는 정수 $a$와 소수 $p$가 존재한다고 하자. divisibility의 정의에 의하여, $a=pr$과 $a+1=ps$를 만족하는 정수 $r$와 $s$가 존재한다. 이에 다음이 도출된다.
$$
1=(a+1)-1=ps-pr=p(s-r)
$$
$s-r$이 정수이므로 $p|1$이다. 그러나, [정리 4.4.2]에 의하여, 1의 정수 divisor는 오직 1과 -1이며, $p$는 소수이므로 $p>1$이다. 그러므로 $p\le1$이고 $p>1$인데, 이것은 모순이다. 그러므로 명제 4.8.3은 참이다.



**Theorem 4.8.4 [Infinitude of the Primes]**

소수의 집합은 무한하다.

**Proof(by contradiction)**

소수의 집합이 유한하다고 하자. 그리고 어떤 소수 $p$는 모든 소수 중 가장 크다고 하자. 그리하여 소수는 다음과 같이 오름차순으로 나열할 수 있다.
$$
2,3,5,7,11,...,p
$$
모든 소수를 곱한 것에 1을 더한 것을 $N$이라고 하자.
$$
N=(2\cdot3\cdot5\cdot7\cdot11\cdot...\cdot p)+1
$$
그러면 $N>1$이며, [정리 4.4.2]에 의하여 $N$은 어떤 소수 $q$에 의하여 divisible하다. $q$는 소수이므로, $q$는 소수 2, 3, 5, 7, ..., $p$ 중 하나이다. 그러므로, divisibility의 정의에 의하여, $2\cdot3\cdot5\cdot7\cdot11\cdot...\cdot p$는 $q$에 의해 나누어진다(divides). 그리하여 [명제 4.8.3]에 의하여, $q$는 $(2\cdot3\cdot5\cdot7\cdot11\cdot...\cdot p)+1$ 곧 $N$을 나눌 수 없다. 그리하여 $N$은 $q$에 의하여 divisible하고 divisible하지 않다. 이는 모순이므로, 소수의 집합은 무한하다.

