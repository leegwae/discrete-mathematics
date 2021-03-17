#  CH4. ELEMENTARY NUMBER  THEORY AND METHODS  OF PROOF

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



**Generalizing from the Generic Particular**

집합의 *every(모든)*  element가 특정 property를 만족한다는 것을 증명하려면, $x$를 집합의 *particular(특정)*하지만 *arbitrarily chosen(임의로 선택)* 한 element로 가정하고, $x$가 그 property를 만족한다는 것을 보여야한다.



**Existential Instantiation**

만약 특정 종류의 object의 존재가 가정되거나 추론되었다면, 동일한 논의에서 다른 것을 위하여 쓰이지 않는 한 어떠한 이름을 object에 붙일 수 있다.



예시