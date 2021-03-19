#  CH4. ELEMENTARY NUMBER  THEORY AND METHODS OF PROOF

**4.1 Direct Proof and Counterexample 1 : Introduction**

**4.1.1 Even, Odd, Prime, and Composite Integers**

**Definitions[Even, Odd]**

정수 $n$이 **even(짝수)**이다는 $n$이 어떤 정수의 두 배와 같을 때, 그리고 오직 이 경우에만 참이다. 정수 $n$이 **odd(홀수)**이다는 $n$이 어떤 정수의 두 배에 1을 더한 것과 같을 때, 그리고 오직 이 경우에만 참이다.

기호로 표현하면, 모든 정수 n에 대하여,
$$
n\mathrm{은\ 짝수다}\quad\Leftrightarrow\quad\mathrm{어떤\ 정수\ }k\mathrm{에\ 대하여\ } n=2k\mathrm{이다}.
$$

$$
n\mathrm{은\ 홀수다}\quad\Leftrightarrow\quad\mathrm{어떤\ 정수\ }k\mathrm{에\ 대하여\ } n=2k+1\mathrm{이다}.
$$



**Definition[Prime, Composite]**

정수 $n$은 **prime(소수)**이다는 $n>1$이고 모든 양의 정수 $r$과 $s$에 대하여 $n=rs$일 때 $r$ 혹은 $s$이 $n$가 같은 경우, 그리고 오직 이 경우에만 참이다. 정수 $n$은 **composite(합성수)**이다는 $n>1$이고 어떤 정수 $r$과 $s$가 $1<r<n$이고 $1<s<n$인 경우, 그리고 오직 이 경우에만 참이다.

기호로 표현하면 다음과 같다: $n>1$인 정수 $n$에 대하여,
$$
\begin{matrix}
n\mathrm{은\ 소수다} &\Leftrightarrow& \forall\ 양의\ 정수\ r과\ s에\ 대하여, n=rs이면 \\
       && r=1이고\ s=n이거나\ r=n이고\ s=1이다.
\end{matrix}
$$

$$
\begin{matrix}
n\mathrm{은\ 합성수다} &\Leftrightarrow& \exist\ 양의\ 정수\ r과\ s에\ 대하여, n=rs이고 \\
       && 1<r<n이고\ 1<s<n이다.
\end{matrix}
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



**4.1.3 Disproving Universal Statements by Counterexample**

**Disproof by Counterexample**

$\forall x\in D,\ P(x)이면\ Q(x)이다.$ 형태의 statement가 틀리다는 것을 증명하려면, 가설 $P(x)$가 참이고 결론 $Q(x)$가 거짓인 $D$ 안의 $x$를 찾아야한다. 이러한 $x$를 **counterexample(반례)**라고 한다.



**4.1.4 Proving Universal Statement**

예시



**Theorem 4.1.1**

어떤 두 짝수의 합은 짝수이다.

**Proof**

$m$과 $n$이 *[particular but arbitrarily chosen]* 짝수 정수라고 하자.

짝수의 정의에 의하여, 어떤 $r$와 $s$에 대하여 $m=2r$ 그리고 $n=2s$이다.
$$
\begin{matrix}
m+n &=& 2r+2s\quad(ㄱ)\\
&=& 2(r+s)\quad(ㄴ)
\end{matrix}
$$
(ㄱ) 치환 (ㄴ) 2로 묶기

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

어떤 홀수 정수와 짝수 정수의 차는 홀수이다.

**proof**

1. $a$는 어떤 홀수 정수이고 $b$는 어떤 짝수 정수라고 하자.
2. 홀수의 정의에 의하여 어떤 정수 $r$에 대하여 $a=2r+1$이고, 어떤 정수 $s$에 대하여 $b=2s$이다.
3. $a-b=(2r+1)-2s\quad\quad(ㄱ)치환$
4. $\quad\quad\quad=2r-2s+1\quad\quad (ㄴ)\mathrm{by\ combining\ like\ terms}$
5. $\quad\quad\quad=2(r-s)+1\quad\quad (ㄷ)2로\ 묶기$
6. $\quad\quad t=r-s$
7. $t$는 정수의 차이므로 정수이다.
8. 치환하면, $t$가 정수인 곳에서 $a-b=2t+1$
9. 그러므로 $a-b$는 홀수이다.



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



**4.3.2 Proving Properties of Rational Numbers**

예제들



**Theorem 4.3.2**

어떤 두 유리수의 합은 유리수이다.

**Proof**

$r$과 $s$가 어떤 유리수라고 하자. 유리수의 정의에 의하여, $b\ne0$이고 $d\ne0$인 어떤 정수 $a,b,c,d$에 대하여 $r=a/b$이고  $s=c/d$이다. 그러므로
$$
\begin{matrix}
r+s&=&\frac{a}{b}+\frac{c}{d}\quad(ㄱ)치환 \\
&=&\frac{ad+bc}{bd}\quad (ㄴ) 대수학
\end{matrix}
$$
$p=ad$이고 $q=bd$라고 하자. 정수의 곱과 합은 정수이고 $a,b,c,d$는 정수이므로 $p$와 $q$도 정수이다. 또한 zero product property에 의하여 $q\ne0$이다. 그러므로
$$
r+s=\frac{p}{q}\quad 여기서\ p와\ q는\ 정수이고\ q\ne0이다.
$$
그러므로, 유리수의 정의에 따라서 $r+s$는 유리수이다.



**4.3.3 Deriving New Mathematics from Old**



**4.4 Direct Proof and Counterexample 4: Divisibility**

배수(divisibility, 의역)의 개념은 **number theory**의 중요한 개념 중 하나이다.



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

**Theorem 4.4.3[Transitivity of Divisibility]**

정수 $a$, $b$, $c$에 대하여, $b$가 $a$로 나누어떨어지고 $c$가 $b$로 나누어떨어진다면 $c$는 $a$로 나누어떨어진다.

**Proof**

$a$, $b$, $c$가 $b$는 $a$로 나누어떨어지고 $c$가 $b$로 나누어떨어지는 모든 *[particular but arbitrarily chosen]* 정수라고 하자. divisibility의 정의에 의하여,
$$
어떤\ 정수\ r과\ s에\ 대하여,\ b=ar\ 이고\ c=bs이다.
$$
치환하면
$$
\begin{matrix}
c &=&bs\\
&=&(ar)s\\
&=&a(rs)
\end{matrix}
$$
$k=rs$라고 하자. $k$는 정수의 곱이므로 정수이다. 그러므로
$$
c=ak\quad 여기서\ k는\ 정수이다.
$$
그러므로 divisibility의 정의에 의하여 $c$는 $a$로 나누어떨어진다.



**Theorem 4.4.1 A Positive Divisor of a Positive Integer**

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

$m$이 1의 양수인 어떤 정수라고 하자. $1=mn$을 만족하는 그러한 정수 $n$이 존재한다. $m$과 $n$은 둘 다 양수이거나, 둘 다 음수이다. (A-T25) $m$과 $n$이 둘 다 양수라면, $m$은 1의 양수 정수 약수이다. 정리 [4.4.1] 에 의하여, $m\le 1$이다. 또한 1보다 작거나 같은 양수 정수는 오직 1 그 자신밖에 없으므로 $m=1$이다. 반대로 $m$과 $m$이 둘 다 음수라면, $(-m)(-n) = mn = 1$이다. 이는 다음과 같은 실수의 property(A-T12)로부터 도출된다.

*Rule for Multiplication with Negative Signs*
$$
(-a)b = a(-b) = -(ab),\quad(-a)(-b) = ab
$$

$$
-\frac{a}{b}=\frac{-a}{b}=\frac{a}{-b}
$$

이 경우 $-m$은 1의 정수 양수 약수이며, 같은 이유로 $-m=1$이다. 그러므로 오직 두 가능성만이 존재한다: $m=1$이거나 $m=-1$이다. 그러므로 1의 약수는 오직 1과 -1뿐이다.



**4.4.2 Proving Properties of Divisibility**

**Theorem 4.4.4 Divisibility by a Prime**

어떤 정수 $n>1$은 유리수에 의해 나누어떨어질 수 있다.

**Proof**

$n$이 1보다 큰 정수라고 하자. 

(1) $n$이 유리수이면, $n$은 유리수에 의해 나누어 떨어질 수 있다. $n$이 유리수가 아니면 다음과 같다.
$$
n=r_0s_0\quad r_0과\ s_0은\ 정수이며\ 1<r_0<n\ 그리고\  1<s_0<n이다.
$$
이것은 $r_0|n$인 divisibility의 정의로부터 도출된다.

(2) $r_0$이 유리수이면, $r_0$은 $n$으로 나누어떨어지는 유리수이다. $r_0$이 유리수가 아니면 다음과 같다.
$$
r_0=r_1s_1\quad r_1과\ s_1은\ 정수이며\ 1<r_1<r_0\ 그리고\  1<s_1<r_0이다.
$$
이것은 $r_1|r_0$인 divisibility의 정의로부터 도출된다. $r_0|n$은 알고있으므로, transitivity of divisibility에 의하여 $r_1|n$이다.

(3) $r_1$이 유리수이면, $r_1$은 $n$으로 나누어떨어지는 유리수이다. $r_1$이 유리수가 아니면 다음과 같다.
$$
r_1=r_1s_2\quad r_2과\ s_2은\ 정수이며\ 1<r_2<r_1\ 그리고\  1<s_2<r_1이다.
$$
이것은 $r_2|r_1$인 divisibility의 정의로부터 도출된다. $r_1|n$은 알고있으므로, transitivity of divisibility에 의하여 $r_2|n$이다.

(4) $r_2$이 유리수이면, $r_2$은 $n$으로 나누어떨어지는 유리수이다. $r_2$이 유리수가 아니면 $r_3s_3$으로 $r_2$를 인수분해하여 위와 같은 과정을 반복한다.

이 과정을 반복하면 다음과 같은 sequence를 얻을 수 있다.
$$
r_0,r_1,r_2,...,r_k
$$
여기서 $k\ge 0,\ 1<r_k<r_{k-1}<...<r_2<r_1<r_0<n$그리고 각각의 $i=0, 1, ..., k$에 대하여 $r_i|n$이다. termination의 조건은 $r_k$가 유리수여야한다. 그러므로 $r_k$는 $n$으로 나누어떨어지는 유리수이다.



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

주어진 어떤 정수 $n>1$에 대하여, 다음을 만족하는 양수 정수 $k$와 서로 다른 유리수 $p_1,p_2,...p_k$, 양수 정수 $e_1,e_2,...,e_k$가 존재한다.
$$
n=p_1^{e_1}p_2^{e_2}p_3^{e_3}...p_k^{e_k}
$$
또한 유리리수의 곱으로서의 $n$에 대한 다른 expression은 인수들이 쓰여진 순서를 제외하면 동일하다.



**Definition[standard factored form]**

주어진 어떤 정수 $n>1$에 대하여, $b$의 **standard factored form**은 다음과 같은 형태의 exrpression이다.
$$
n=p_1^{e_1}p_2^{e_2}p_3^{e_3}...p_k^{e_k}
$$
여기서 $k$는 양수 정수, $p_1,p_2,...p_k$는 유리수, $e_1,e_2,...,e_k$는 양수 정수, $p_1<p_2<...<p_k$이다.