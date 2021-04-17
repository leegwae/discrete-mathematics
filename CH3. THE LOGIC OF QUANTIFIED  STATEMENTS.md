# CH3. THE LOGIC OF QUANTIFIED STATEMENTS

- **predicate calculus**: predicates(술어)와 quantified statement의 symbolic analysis(기호적 분석)
- **statement calculus** (혹은 **propositional calculus(명제 논리)**): ordinary compound statement의 기호적 분석



**3.1 Predicates and Quantified Statements 1**

$P$: is a student at UOS.

$Q$: is a student at

$P(x)$ : $x$는 서울시립대의 학생이다.

$Q(x,y)$ : $x$는 $y$의 학생이다.

*predicate symbols*: $P, Q$

*predicate variables*: $x, y$



**predicate**

$P(x),\ Q(x,y)$ 등

- *predicate*: 적절한 predicate variable과 predicate symbol로 이루어져있다.
- **propositional functions(명제 함수)** 혹은 **open sentences**라고 한다.



**Definition[predicate]**

**predicate(술어)**는 유한한 수의 변수를 가지며, 특정한 값이 변수로 치환될 때 statement가 되는 sentence(문장)이다. predicate variable의 **domain**(논의 영역)는 변수로 치환될 수 있는 모든 값의 집합이다.



**Definition[Truth set]**

$P(x)$가 predicate이고 $x$가 domain $D$를 가졌을 때, $P(x)$의 **truth set**은 $x$로 치환될 때 $P(x)$를 참이게 하는 $D$의 모든 element의 집합이다. $P(x)$의 truth set은 다음과 같이 표기한다.
$$
\{x \in D\ |\ P(x)\}
$$


**3.1.1 The Universal Quantifier: $\forall$**   

- **quantifier(양화사)**: "어떤" 혹은 "모든"과 같이 quantities(양)을 가리키는 단어이며, 주어진 술어가 참인 element가 몇 개 인지 알려준다.
- **보편 양화사(universal quantifier)**: "모든 ~에 대하여(for  every)", "각각에 대하여(for each)", "for any(어떤 것에 대해서도)", "given any(주어진 어떤 것이라도)", "for all(모든 것에 대해)" $\forall$



**Definition[Univeral Statement]**

$Q(x)$가 predicate이고, $D$가 $x$의 domain이라 하자. **universal statement(보편적 진술)**은 "$\forall x \in D, Q(x)$ " 형태의 statement이다. 이 진술은 $Q(x)$가 $D$의 각각의 $x$에 대하여 참일 때, 그리고 오직 이 경우에만 참이라고 정의된다. $Q(x)$가 $D$의 $x$ 중 적어도 하나에 대해서라도 거짓일 때, 그리고 오직 이 경우에만 거짓이라고 정의된다. $Q(x)$가 거짓인 $x$의 값은 보편적 진술의 **counterexample(반례)**라고 한다.



**moethod of exhaustion**

예시



**3.1.2 The Existential Quantifier: $\exists$**

- **존재 양화사(existential quantifier)**: "~가 있다", $\exists$
  - there exists are there is $a$
  - we can find $a$
  - there is at least one
  - for some
  - for at least one.

**Definition[Existential Statement]**

$Q(x)$가 predicate이고, $D$가 $x$의 domain이라 하자. **existential statement**는 "$\exist x \in D\ \mathrm {such\ that}\ Q(x)$($Q(x)$가 참인 그러한 $x$가 존재한다)" 형태의 statement이다. 이 진술은 $Q(x)$가 $D$의 $x$ 중 적어도 하나에 대하여 참일 때, 그리고 오직 이 경우에만 참이다. $D$의 모든 $x$에 대하여 거짓일 때, 그리고 오직 이 경우에만 거짓이다.



**3.1.3 Universal Conditional Statements**

**universal conditional statement**
$$
\forall x,\ \mathrm {If\ }P(x)\ \mathrm {then}\ Q(x)
$$
모든 $x$에 대하여, $P(x)$가 참이라면 $Q(x)$는 참이다.



**3.1.4 Equivalent Forms of Universal and Existential Statements**

$\forall$ 실수 $x$에 대하여, $x$가 정수라면 $x$는 유리수이다(rational).

$\forall$ 정수 $x$에 대하여, $x$는 유리수이다.

모든 정수는 유리수이다.



$\forall x \in U,\ \mathrm {If\ }P(x)\ \mathrm {then}\ Q(x)$

$\forall x \in D,\ Q(x)$

$\forall x,\ \mathrm {if\ } x\ \mathrm {is\ in\ }D\ \mathrm {then\ }Q(x)$



**3.1.5 Bound Vairables and Scope**

(1) For every integer $x$, $x^2\ge 0$

(2) There exists a real number $x$ such that $x^3 =8$

- 변항(variable) $x$는 $x$를 제어하는 양화사에 의해 **bound**되었다.
- $x$의 **scope(범위)**는 양화사가 $x$를 도입할 때부터 quantified statment가 끝날 때까지이다.

```c
int foo() {
    int x;
    
    return 0;
}
```

`x`는 그것이 정의된 함수에 대하여 **local(지역적이다)**.



**3.1.6 Implicit Quantification**

예) implicit universal quantification
$$
\mathrm {If\ a\ number\ is\ an\ integer,\ then\ it\ is\ a\ rational\ number.}
$$
예) implicit existential quantification
$$
\mathrm {If\ }x>2\mathrm{\ then\ }x^2>4
$$

$$
\mathrm {For\ every\ real\ number\ }x\mathrm {\ if\ }x>2\mathrm {\ then\ }x^2 >4
$$

$$
x>2 \implies x^2>4
$$



**Notation[$\implies$, $\iff$]**

$P(x), Q(x)$는 predicate이며, $x$의 common domain은 $D$라고 한다.

- $P(x) \implies Q(x)$: $P(x)$의 truth set의 모든 element가 $Q(x)$의 truth set에 속한다는 것을 의미한다. $\forall x,\ P(x) \to Q(x)$

- $P(x)\iff Q(x)$: $P(x)$와 $Q(x)$가 동일한 truth set을 가지고 있다는 것을 의미한다. $\forall x, P(x) \leftrightarrow Q(x)$



**3.2 Predicates and Quantified Statement 2**

**3.2.1 Negations of Quantified Statements**

- universal statement의 부정의 보편적인 form은 negation의 정의와 universal statement, existential statement에 대한 truth values의 정의를 따른다.

  

**Theorem[3.2.1 Negation of a Universal Statement]**
$$
\forall x\mathrm {\ in\ }D,\ Q(x)
$$
형태의 statement의 negation은 다음 형태의 statement와 논리적으로 동등하다.
$$
\exist x\mathrm{\ in\ }D\mathrm{\ such\ that}\sim Q(x)
$$

기호로 표현하면
$$
\sim (\forall x\mathrm {\ in\ }D,\ Q(x))\equiv \exist x\mathrm{\ in\ }D\mathrm{\ such\ that}\sim Q(x)
$$




**local equivalence for quantified statements**

**universal statement("all are(모든 것은 ~이다)")의 부정은 existential statement("some are not(어떤 것은 ~이 아니다.)" 혹은 "there is at least one that is not(~이 아닌 것이 적어도 하나 있다.)")와 논리적으로 동등하다(logically equivalent).**



- existential statement의 부정의 보편적인 form은 negation의 정의와 existential statement와 universal statement에 대한 truth valeus의 정의를 따른다.

**Theorem[3.2.2 Negation of an Existential Statement]**
$$
\exist x\mathrm{\ in\ }D\mathrm{\ such\ that}\ Q(x)
$$
형태의 statement의 negation은 다음 형태의 statement와 논리적으로 동등하다.
$$
\forall x\mathrm {\ in\ }D,\ \sim Q(x)
$$
기호로 표현하면
$$
\sim (\exist x\mathrm{\ in\ }D\mathrm{\ such\ that}\ Q(x)) \equiv \forall x\mathrm {\ in\ }D,\ \sim Q(x)
$$



**local equivalence for quantified statements**

**existential statement("어떤 것은 ~이다.")의 부정은 univeral statement("none are(어떤 것도 ~이 아니다)" 혹은 "all are not(모든 것은 ~이 아니다)")와 논리적으로 동등하다.**



**3.2.2 Negations of Universal Conditional Statements**

- *for all* statement의 부정의 정의에 따르면

$$
\sim (\forall x,\ P(x)\to Q(x))\equiv \exist x\mathrm {\ such\ that\ }\sim (P(x)\to Q(x))\quad 3.2.1
$$

- if-then statement의 부정은 *and* statement와 논리적으로 동등하다.

$$
\sim (P(x) \to Q(x))\equiv P(x)\and \sim Q(x)\quad 3.2.2
$$

- (3.2.1)을 (3.2.2)로 바꾸면

$$
\sim (\forall x,\ P(x)\to Q(x))\equiv \exist x\mathrm {\ such\ that\ }P(x)\and \sim Q(x)\quad 3.2.1
$$



**Negation of a Universal Conditional Statement**
$$
\sim (\forall x,\ P(x)\mathrm {\ then\ } Q(x))\equiv \exist x\mathrm {\ such\ that\ }P(x)\mathrm {\ and\ } \sim Q(x).
$$



**3.2.3 The Relation among $\forall$, $\exist$, $\and$, $\or$**

- *for all* statement의 부정은 *there exists* statement이고, *there exists* statement의 부정은 *for all* statement이다.
- $Q(x)$가 predicate이고, $x$의 domain $D$가 집합 $\{ x_1, x_2, ..., x_n\}$일 때, 다음 두 statement는 논리적으로 동등하다.

$$
\forall x \in D,\ Q(x)\quad그리고\quad Q(x_1)\and Q(x_2)\and \cdots\and Q(x_n)
$$

- $Q(x)$가 predicate이고, $x$의 domain $D$가 집합 $\{ x_1, x_2, ..., x_n\}$일 때, 다음 두 statement는 논리적으로 동등하다.

$$
\exist x \in D\mathrm {\ such\ that\ }Q(x)\quad 그리고\quad Q(x_1)\or Q(x_2)\or\cdots\or Q(x_n)
$$



**3.2.4 Vacuous Truth of Universal Statements**

- 다음 형태의 statement는 $P(x)$가 $D$의 모든 $x$에 대하여 거짓인 경우, 그리고 오직 이 경우에만 **vacuously true** 혹은 **true by default**라고 한다.

$$
\forall x \in D,\mathrm {\ if\ }P(x)\mathrm{\ then\ }Q(x)
$$



**3.2.5 Variants of Universal Conditional Statement**

**Definition[Contrapositive, Converse, Inverse]**

$\forall x \in D,\mathrm {\ if\ }P(x)\mathrm{\ then\ }Q(x)$에 대하여,

1. **contrapositive(대우)**는 $\forall x \in D,\mathrm {\ if\ }\sim Q(x)\mathrm{\ then\ }\sim P(x)$
2. **converse**는 $\forall x \in D,\mathrm {\ if\ }P(x)\mathrm{\ then\ }Q(x)$
3. **inverse(역)**는 $\forall x \in D,\mathrm {\ if\ }\sim P(x)\mathrm{\ then\ }\sim Q(x)$



**3.2.6 Necessary and Sufficient Conditions, Only If**

**Definition[Sufficient Condition, Necessary Condition, Only If]**

- "$\forall x,\ r(x)$은 $s(x)$의 **sufficient condition(충분조건)**이다"는 다음을 의미한다 : "$\forall x,\mathrm{if\ }r(x)\mathrm{\ then\ }s(x).$"
- "$\forall x,\ r(x)$은 $s(x)$의 **necessary condition(필요조건)**이다"는 다음을 의미한다 : "$\forall x,\mathrm{if\ }\sim r(x)\mathrm{\ then\ }\sim s(x).$" 혹은 "$\forall x,\mathrm{\ if\ }s(x)\mathrm{\ then\ }r(x)$."
- "$\forall x,\ r(x)\mathbf{\ only\ if\ }s(x)$는 다음을 의미한다 : "$\forall x,\mathrm{if\ }\sim s(x)\mathrm{\ then\ }\sim r(x).$" 혹은 "$\forall x,\mathrm{if\ }r(x)\mathrm{\ then\ }s(x).$"



**3.3 Statements with Multiple Quantifiers**

**statement가 한 종류 이상의 quantifier를 가지고 있을 때, quantifier에 의해 일어나는 action이 순서대로 수행된다고 생각한다.**



**3.3.1 Translating from Informal to Formal Language**

예시



**3.3.2 Ambiguous Language**



**3.3.3 Negations of Statements with More Than One Quantifier(한 개 이상의 양화사를 가진 statements의 부정)**
$$
\sim (\forall x\mathrm{\ in}\ D, \exist y\mathrm{\ in\ }E\mathrm{\ such\ that\ }P(x,y))\equiv \exist x\mathrm{\ in\ }D\mathrm{\ such\ that\ }\forall y\mathrm{\ in\ }E,\ \sim P(x,y)
$$

$$
\sim (\exist x\mathrm{\ such\ that}\ \forall y\mathrm{\ in\ }E, P(x,y))\equiv \forall x\mathrm{\ in\ }D,\ \exist y\mathrm{\ in\ }E\mathrm{\ such\ that} \sim P(x,y)
$$



**3.3.4 Order of Quantifiers(양화사의 순서)**

- $\forall, \exist$ 를 모두 가진 statement에서 양화사의 순서를 바꾸는 것은 statement의 의미를 상당히 바꿀 수 있다.
- 한 개의 양화사가 같은 종류의 다른 양화사 바로 뒤에 오는 경우, 양화사의 순서를 의미에 영향을 미치지 않는다. (예)

$\forall$ 실수 $x$와 $\forall$ 실수 $y$, $x+y=y+x$

$\forall$ 실수 $y$와 $\forall$ 실수 $x$, $x+y=y+x$



**3.3.5 Formal Logical Notation**

- "$\forall x$ in $D, P(x)$"는 다음과 같이 쓸 수 있다: "$\forall x\ (x\mathrm{\ in\ }D\to P(x))$"
- "$\exist x$ in $D$ such that $P(x)$"는 다음과 같이 다시 쓸 수 있다: "$\exist x\ (x\mathrm{\ in\ }D\and P(x))$"



**fully formal notation의 장점과 단점**

- 단점: 복잡하고 intuitive(직관적인) 이해로부터 기인하기 때문에, 사용할 때 인지되지 않은 오류를 일으킬 수 있다.
- 장점: operation은 완벽하게 기계적이며, 컴퓨터에서 프로그래밍될 수 있다. 형식적인 조작을 통해 우리의 직관을 검사하기에 좋다.



**language of first-order logic**

- 양화사, 변항, 술어, 논리적 연결사의 기호들로 이루어진 것을 **language of first-order logic**이라고 한다.



**3.3.6 Prolog**

예시



**3.4 Arguments with Quantified Statements**

**Universal Instantiation**

- property가 집합의 *전부(everything)*에 있어 참일 때, 집합의 *어떤 특정한 것(any particular)*에 대해서도 참이다.
- univeral instantiation은 deductive reasoning(연역적 추론)의 핵심적인 도구이다.

$$
\begin{matrix}
r^{k+1}\cdot r &=& r^{k+1}\cdot r^1 \\
       &=& r^{(k+1) +1}\\
       &=& r^{k+2}
\end{matrix}
$$

[Step1]

모든 실수 $x$에 대하여, $x^1 = x$이다.		universal truth

$r$는 특정 실수이다.										particular instance

$\therefore r^1=r$														conclusion

[Step2]

모든 실수 $x$와 모든 정수 $m$에 대하여, $x^m\cdot x^n = x^{m+n}$이다.		universal truth

$r$는 특정 실수이고 $k+1$과 1은 특정 정수이다.									particular instance

$\therefore r^{k+1}\cdot r^1=r^{(k+1)+1}$																			conclusion



**3.4.1 Universal Modus Ponens**

- universal instantiation의 법칙은 타당한 argument의 형태를 포함한 modus ponens로 결합될 수 있는데, 이것은 *universal modus ponens*라고 한다.

- Formal Version

$\forall x$, if $P(x)$ then $Q(x)$

$P(a)$ for a particular $a$.

$\therefore Q(a)$.

- Informal Version

If $x$ makes $P(x)$ true, then $x$ makes $Q(x)$ true.

$a$ makes $P(x)$ true.

$\therefore a$ makes $Q(x)$ true.



**3.4.2 Use of Universal Modus Ponens in a Proof**

예시



**3.4.3 Universal Modus Tollens**

- *univeral modus tollens*: univeral instantiation과 modus tollens를 결합한 것으로부터 타당성이 비롯된다.
- Formal Version

$\forall x$, if $P(x)$ then $Q(x)$

$\sim Q(a)$, for a particular $a$.

$\therefore\ \sim P(a)$.

- Informal Version

If $x$ makes $P(x)$ true, then $x$ makes $Q(x)$ true.

$a$ makes $P(x)$ true.

$\therefore\ a$ makes $Q(x)$ true.



**3.4.4 Use of Universal Modus Ponens in a Proof**

예시



**3.4.5 Proving Validity of Arguments with Quantified Statements**

**Definition[Valid, Sound]**

*argument form*이  **valid(타당하다)**는 것은 다음을 의미한다: 전제의 어떤 술어가 술어 기호로 치환되든, resulting premise statements가 모두 참이라면, 결론 또한 참이다.

*argument*가 **valid(타당하다)**는 것은 그것의 form이 타당한 경우, 그리고 오직 이 경우에만 참이다. 이것이 **sound(건전하다)**는 것은 이것의 form이 타당하고 이것의 전제가 참일 때, 그리고 오직 이 경우에만 참이다.



**3.4.6 Using Diagrams to Test for Validity**

**Converse Error (Quantified Form)**

$\forall x$, if $P(x)$ then $Q(x)$.

$Q(x)$ for a particular $a$.

$\therefore P(a)$.

**Inverse Error (Quantified Form)**

$\forall x$, if $P(x)$ then $Q(x)$.

$\sim P(a)$, for a particular $a$.

$\therefore\ \sim Q(a)$.



**3.4.7 Creating Additional Forms of Argument**

- univeral modus ponens과 modus tollens는 univeral instantiation과 modus ponens, 그리고 modus tollens를 결합한 것을 포함한다.
- 마찬가지로 universally quantified statements를 포함한 argument의 additional form도 univeral instantiation과 다른 형태의 valid argument를 결합한 것을 포함한다. (예)

$p\to q$

$q\to r$

$\therefore p\to r$



**Univeral Transitivity**

$\forall x\ P(x)\to Q(x)$

$\forall x\ Q(x)\to R(x)$

$\therefore\forall x\ P(x)\to R(x)$

