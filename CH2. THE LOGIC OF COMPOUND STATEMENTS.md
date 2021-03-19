# CH2. THE LOGIC OF COMPOUND STATEMENTS

**2.1 Logical Form and Logical Equivalence**

**Argument**

- argument은 주장의 참을 입증하는데 초점을 맞춘 statement의 연속이다.
- 가장 마지막 statement을 *conclusion*(결론), 선행하는 statement들을 *premise*(전제)라고 한다.

**Form of argument**

- form of argument는 그것의 내용과 구분된다.
- 결론의 참은 반드시 전제의 참으로부터 비롯된다.



**2.1.1 Statement**

**Definition[Statement]**

**statement(진술)** (혹은 **proposition(명제)**)는 참이나 거짓이거나, 혹은 참도 거짓도 아닌 sentence(문장)을 뜻한다.



$x^2 + 2 = 11$은 $x$의 값에 따라 진리값이 참 또는 거짓이므로 statement가 아니다.



**2.1.2 Compound Statements**

| symbol             | meaning |
| ------------------ | ------- |
| $\sim$ 혹은 $\neg$ | not     |
| $\and$             | and     |
| $\or$              | or      |



**order of operation**

- 대수학에서와 연산 순위가 같다.



기호를 사용하여 번역하기
$$
p\ \mathrm {but}\ q\quad\mathrm {means}\quad p\ \mathrm {and}\ q
$$

$$
\mathrm {neither}\ p\ \mathrm {nor}\ q\quad \sim p\ \mathrm {and} \sim q
$$



**2.1.3 Truth Values**

**Definition[Negation]**

$p$가 statement variable일 때, $p$의 **negation(부정)**은 "$p$가 아니다(not $p$)" 혹은 "$p$는 사실이 아니다(It is not the case that $p$)"이며, $\sim p$로 표기한다. 이것은 $p$와 반대의 진리값을 가지고 있다: 만약 $p$가 참이면, $\sim p$는 거짓이다; 만약 $p$가 거짓이라면, $\sim p$는 참이다.

| $p$  | $q$  |      |
| ---- | ---- | ---- |
|      |      |      |



**Definition[Conjunction]**

$p$와 $q$가 statement variable일 때, $p$와 $q$의 **conjunction(연연)**은 "$p$그리고 $q$이다($p\ \mathrm {and}\ q$)"이며, $p\and q$라고 표기한다. 이것은 $p$와 $q$가 모두 참일 때, 그리고 오직 이 경우에만 참이다. 만약 $p$ 혹은 $q$가 거짓이라면, 혹은 둘 다 거짓이라면 $p\and q$는 거짓이다.

| $p$  | $q$  |      |
| ---- | ---- | ---- |
|      |      |      |



**Definition[Disjunction]**

$p$와 $q$가 statement variable일 때, $p$와 $q$의 **disjunction(선언)**은 "$p$이거나 $q$이다($p$ or $q$)"이며, $p\or q$로 표기한다. 이것은 $p$가 참이거나, 혹은 $q$가 참이거나, 혹은 $p$와 $q$ 모두 참일 때 참이다; 이것은 $p$와 $q$ 모두가 거짓일 때 거짓이다.

| $p$  | $q$  |      |
| ---- | ---- | ---- |
|      |      |      |



**2.1.4 Evaluating the Truth of More General Compound statements**

**Definition[Statement form]**

**statement form** (혹은 **propositional form**)은 $p,\ q,\ r$과 같은 statement variable들과 $\sim,\ \and,\ \or$과 같은 논리적 연결사(logical connectives)들로 이루어진 expression이다. (이것은 acutal statements가 component statement varialbe로 치환될 때 statement가 된다.) 주어진 statement form에 대한 **truth table(진리표)**은 그것의 component statement variable에 대한 진리값의 모든 가능한 조합에 대응하는 truth values를 보여준다.

 

**XOR**

| $p$  | $q$  |      |
| ---- | ---- | ---- |
|      |      |      |



**2.1.5 Logical Equivalence**

**Definition[Logically equivalent]**

두 개의 *statement forms*는 그것들의 statement variable에 대해 가능한 statement의 각각의 치환에 대하여 동일한 진리값을 가지고 있을 때, 그리고 오직 이 경우에만 **논리적으로 동등하다(logically equivalent)**. $P$ 와 $Q$ statement form의 logical equivalence는 $P\equiv Q$라고 표기한다.

두 *statements*는 동일한 component statement variable이 동일한 copmonent statement를 치환할 때 논리적으로 동등한 경우, 그리고 오직 이 경우에만 **logically equivalent**하다고 한다.



**De Morgan's laws**

$and$ statement의 부정은 각각의 component가 부정된 $or$ statement와 논리적으로 동등하다.

$or$ statement의 부정은 각각의 component가 부정된 $and$ statement와 논리적으로 동등하다.



**2.1.6 Tautologies and Contradictions**

**tautology**는 statement variable로 치환된 개별적인 statement의 진리값에 상관없이 언제나 참인 statement form이라고 한다. 그것의 form이 tautology인 statement는 **tautological statement**라고 한다.

**contradication**는 statement variable로 치환된 개별적인 statement의 진리값에 상관없이 항상 거짓인 statement form이라고 한다. 그것의 form이 contradiction인 statement를 **contradictory statement**라고 한다.



**2.1.7 Summary of Logical Equivalences**

이미지



**2.2 Conditional statements**

**Definition[Conditional]**

$p$와 $q$가 statement variable일 때, $p$에 의한 $q$의 **conditional**은 "$p$이면 $q$이다(If $p$ then $q$)" 혹은 "$p$은 $q$를 암시한다($p$ imples $q$)"이며,  $p\to q$로 표기한다. 이 조건문은 $p$가 참이고 $q$가 거짓일 때 거짓이며, 그밖의 경우는 참이다. $p$를 조건문의 **hypothesis(가설)** (혹은 **전제(antecedent)**)라고 하며, $q$는 **결론(conclusion)** (혹은 **consequent**)이라 한다.



**vacuously true(true by default)**

그것의 가설이 거짓이라는 사실에 의하여 참인 조건문은 **vacuously true** 혹은 **true by default**라고 한다.



| $p$  | $q$  | $p\to q$ |
| ---- | ---- | -------- |
| T    | T    | T        |
| T    | F    | F        |
| F    | T    | T        |
| F    | F    | T        |

전체가 참일 때 결론이 거짓일 수는 없다. 이 경우를 제외하면 conditional은 모두 참이다.



**2.2.1 Logical Equivalences Involving $\to$**

**2.2.2 Representation of If-Then as Or**
$$
p\to q\ \equiv\ \sim p\and q
$$

| $p$  | $q$  | $q\to q$ | $\sim p\and q$ |
| ---- | ---- | -------- | -------------- |
|      |      |          |                |



**2.2.3 The Negation of a Conditional Statement**

정의에 의하여, $p\to q$는 그것의 가설 $p$가 참이고 그것의 결론 $q$가 거짓인 경우, 그리고 오직 이 경우에만 거짓이다.

"$p$이면 $q$이다"의 부정은 "$p$이고 $q$가 아니다"와 논리적으로 동등하다.
$$
\sim(p\to q)\equiv p\and\sim q
$$

$$
\begin{matrix}
\sim(p\to q) &\equiv& \sim(p\or\sim q) \\
       &\equiv& \sim(\sim p)\and(\sim q) \\
       &\equiv& p\and\sim q
\end{matrix}
$$



**2.2.4 The Contrapositive of a Conditional Statement**

**definition[Contrapositive]**

"$p$이면 $q$이다" 형태의 조건문의 **contrapositive(대우)**는
$$
\sim q이면\ \sim p이다.
$$

$$
p\to q의\ \mathrm {contrapositive}는\ \sim q\to \sim p이다.
$$

조건문은 그것의 대우와 논리적으로 동등하다.



**2.2.5 The Converse and Inverse of a Conditional Statement**

**Definition[Converse, Inverse]**

"$p$이면 $q$이다" 형태의 조건문이 주어졌을 때,

1. **converse**는 "$q$이면 $p$이다"
2. **inverse**는 "$\sim p$이면 $\sim q$이다"

$$
p\to q의\ \mathrm {converse}는\ \sim q\to \sim p이다.
$$

$$
p\to q의\ \mathrm {converse}는\ \sim p\to \sim q이다.
$$

**2.2.6 Only If and the Biconditional**

**Definition[Only If]**

"$p$이면 $q$이다"가 statement일 때,
$$
p\ \mathbf {only\ if}\ q\quad q가\ 아니면,\ p가\ 아니다.\ 혹은\ p이면\ q이다.
$$


**Definition[Biconditional]**

$p$와 $q$가 statement variable로 주어졌을 때, **$p$ 그리고 $q$의 biconditional**은 "$p$는 $q$인 경우, 그리고 오직 그러한 경우에만 참이다."이며, $p\leftrightarrow q$로 표기한다. 이것은 $p$와 $q$ 모두가 동일한 값을 가질 경우 참이고, 서로 다른 값을 가질 경우 거짓이다. *if and only if​는* **iff**로 축약한다.

| $p$  | $q$  | $p\to q$ | $q\to p$ | $p\leftrightarrow q$ |
| ---- | ---- | -------- | -------- | -------------------- |
|      |      |          |          |                      |



**Order of Operations for Logical Operators**

| 순위 | 연산자                  |
| ---- | ----------------------- |
| 1    | $\sim$                  |
| 2    | $\and,\ \or$            |
| 3    | $\to,\ \leftrightarrow$ |



**2.2.7 Necessary and Sufficient Conditions**

**Definition[Sufficient and Necessary Condition]**

$r$과 $s$가 statement일 때,

$r$은 $s$의 **subfficient condition(충분조건)**이다.		"$r$이면 $s$이다."

$r$은 $s$의 **necessary condition(필요조건)**이다.		"$r$이 아니면, $s$가 아니다."



**필요충분조건**

$r$은 $s$의 필요충분조건이다.		"$r$은 $s$인 경우, 그리고 오직 이 경우에만 참이다."



**2.3 Valid and Invalid Arguments**

**Definition[Argument]**

**argument(논증)**은 statement의 연속이며, **argument form**은 statement form의 연속이다. 논증의 모든 statement와 argument form의 모든 statement form는 가장 마지막 것을 제외하고 **premises(전제)** (혹은 **assumptions(가정)** 혹은 **hypotheses(가설)**)이라고 한다. 마지막 statement나 statement form은 **conclusion(결론)**이다. $\therefore$은 결론 앞에 붙는다.

$argument\ form$이 **타당하다**는 그것의 전제 속 어떤 statement를 statement variable로 바꾸든, 결과 전제가 모두 참이라면, 결론 역시 참이라는 것을 뜻한다. *argument*​가 **타당하다**는 그것의 form이 타당하다는 것을 뜻한다.



**2.3.1 Modus Ponens and Modus Tollens**

- 두 개의 전제와 결론으로 이루어진 논증을 **syllogism(삼단 논법)**이라고 한다.
- 첫번째 전제를 **major premise**, 두번째 전제를 **minor premise**라고 한다.



**modus ponens**

- 가장 유명한 삼단논법

$p$이면 $q$이다.

$p$이다.

$\therefore$ $q$이다.



| $p$  | $q$  | $p\to q$ | $p$  | $q$  |
| ---- | ---- | -------- | ---- | ---- |
|      |      |          |      |      |

이 arguemnt form은 타당하다.



**modus tollens**

$p$이면 $q$이다.

$\sim p$이다.

$\therefore$ $\sim q$이다.

| $p$  | $q$  | $p\to q$ | $\sim p$ | $\sim q$ |
| ---- | ---- | -------- | -------- | -------- |
|      |      |          |          |          |

이 arguemnt form은 타당하다.



**2.3.2 Additional Valid Argument Forms: Rules of Inference**

- **rule of inference**는 타당한 form of argument이다. modus ponens와 modus tollens도 form of argument이다.



**Generalization**

| (a)                           | (b)                           |
| ----------------------------- | ----------------------------- |
| $p$<br />$\therefore p\or\ q$ | $q$<br />$\therefore p\or\ q$ |



**Specialization**

| (a)                            | (b)                            |
| ------------------------------ | ------------------------------ |
| $p\and\ q$<br />$\therefore p$ | $p\and\ q$<br />$\therefore q$ |



**Elimination**



| (a)                                         | (b)                                         |
| ------------------------------------------- | ------------------------------------------- |
| $p\or\ q$<br />$\sim q$<br />$\therefore p$ | $p\or\ q$<br />$\sim p$<br />$\therefore q$ |

**Transivity**

| (a)                                             |
| ----------------------------------------------- |
| $p\to q$<br />$q\to r$<br />$\therefore p\to r$ |



**Proof by Division into Cases**

| (a)                                                      |
| -------------------------------------------------------- |
| $p\or q$<br />$p\to r$<br />$q\to r$<br />$\therefore r$ |



**2.3.3 Fallacies**

**fallacy(오류)**는 타당하지 않은 논증을 초래하는 추론 속 오류이다(A fallacy is an error in reasoning that results in an invalid argument).

- **using ambiguous premises**(애매모호한 전제의 사용)
- **circular reasoning**(순환적 추론)
- **jumping to a conclusion**(결론으로 비약)



**Converse Error**

예시

**Inverse Error**

예시



**Definition[Sound, Unsound]**

- **건전한(sound)** 논증은 그것이 타당하고, 그것의 전제가 모두 참인 논증이다.
- **건전하지 않은(sound)** 논증은 건전한 논증이 아닌 논증이다.



**2.3.4 Contradictions and Valid Arguments**

**Contradiction Rule**

$p$가 참이라고 해보자. 명제 $p$가 거짓이다는 논리적으로 contradiction(모순)으로 이어진다는 것을 증명한다면, $p$가 참이라는 결론을 이끌어낼 수 있다.



**Contraidction Rule**

예시





