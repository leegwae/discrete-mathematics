# CH1. SPEAKING MATHMEATICALLY

**1.1 Variables**

**변수는 언제 사용하는가?**

- 하나 이상의 값이라고 생각하였으나, 무엇인지 알 수 없을 때
- 주어진 집합의 모든 elements에 대하여 equally true하여, 특정 값으로 지정하고 싶지 않을 때



**첫번째 : 하나 이상의 값이라고 생각하였으나, 무엇인지 알 수 없을 때**

- 예: 2x + 3 = x^2
- 장점: temporary name을 주어 가능한 값을 찾아내는 데 도움이 되어 정확한 연산을 수행할 수 있다.



**변수는 수학적인 변수와 비슷하다**

- value가 위치할 수 있는 computer memory 안의 위치에 만들어지기 때문



**두번째: 주어진 집합의 모든 elements에 대하여 equally true하여, 특정 값으로 지정하고 싶지 않을 때 **

- 예: 2보다 크고 그 제곱이 4보다 크면 어떤 값이 선택되었든 상관없다.
- 단점: temporary name을 주는 것은 애매모함을 발생시킬 수 있다. (??)
  - No matter what number n might be chosen, if n is greater than 2, then  n2 is greater than 4.



**1.1.1 수학적 statement의 종류**

- **universal statement** : 특정 값이 집합의 모든 elements에 대하여 참이다.
  - 예: 모든 양수는 zero보다 크다.
- **conditional statement**: 하나가 참이면, 다른 모두가 참이다.
  - 예: 378을 18로 나눌 수 있다면, 378은 6으로도 나눌 수 있다.
- **existential statement**: 주어진 property가 참일 수도, 참이 아닐 수도 있을 때, 적어도 하나의 property는 참이다.
  - 예: even(짝수)인 prime number(소수)가 있다.



**1.1.2 Universal Conditional Statements**

- universal statement : "for every"라는 단어의 variation을 포함한다.
- conditional statement: "if-then"이라는 단어의 version을 포함한다.
- **universal conditional statement**: universal하고 conditional한 statement
  - 예: 모든 동물 a에 대하여, 만일 a가 강아지라면, a는 포유류이다.
- <u>중요한 특징: 순수하게 universal하거나 순수하게 conditional한 statement로 다시 쓸 수 있다.</u>
  - conditional nature가 명시적이고 universal nature가 암시적인 예: 
    - a가 강아지라면, a는 포유류이다.
    - 그 동물이 강아지라면, 그 동물은 포유류이다.
  - universal nature가 명시적이고, conditional nature가 암시적인 예:
    - 모든 강아지 a에 대하여, a는 포유류이다.
    - 모든 강아지는 포유류이다.
- universal conditional statement를 여러가지 방법으로 번역할 수 있는 능력은 수학과 CS에서 엄청나게 유용하다.



**1.1.3 Universal existential statements**

- **universal existential statement**: universal하고 existential하다.
  - universal하다: 첫번째 part가 주어진 type의 모든 object에 대하여 특정 property가 참이라고 하고 있으므로.
  - existential하다: 두번째 part가 무언가의 존재(existence)를 주장하고 있으므로.
- 예: 모든(every) 실수는 additive inverse(??)를 가진다.
  - property "has an additive inverse"는 모든 실수에 대하여 보편적으로 적용된다.
  - 또한 각각의 실수에 대하여 무언가—additive inverse—의 존재가 있음을 주장한다.
  - 그런데, additive inverse의 nature는 실수에 의존한다. 그러므로, 서로 다른 실수는 서로 다른 additive inverse를 가진다.
  - additive inverse가 실수임을 안다면 이 statement를 여러 방법으로 덜 formal하게, 혹은 더 formal하게 다시 쓸 수 있다.
    - 모든(all) 실수는 additive inverse를 가진다.
    - 모든 실수 r에 대하여, r에 대한 additive inverse가 있다.
    - 모든 실수 r에 대하여, r에 대하여 additive inverse인 실수 s가 있다.
    - (나중에) When r is positive,  s is negative, when r is negative, s is positive, and when r is zero, s is also zero.(??)
  - 수학에서 변수를 쓰는 가장 큰 이유: One of the most important reasons for using variables in mathematics is that it gives you  the ability to refer to quantities unambiguously throughout a lengthy mathematical argument, while not restricting you to consider only specific values for them.(??)



**1.1.4 Existential Universal statements**

- **existential universal statement**
  - existential하다: 첫번째 part가 "특정 object가 존재한다"고 주장하고 있으므로.
  - universal하다: 두번째 part가 "object가 특정 종류의 모든 것에 대하여 특정 property를 만족한다"고 하고 있으므로.
- 예: 모든(every) 양의 정수보다 작거나 같은 양의 정수가 존재한다.
  - 다음과 같이 더 formal하게, 혹은 덜 formal하게 적을 수 있다.
    - 어떤(some) 양의 정수는 모든(every) 양의 정수보다 작거나 같다.
    - 모든(every) 양의 정수보다 작거나 같은 양의 정수 m이 존재한다.
    - 모든(every) 양의 정수가 m보다 크거나 같은, 그러한 양의 정수 m이 존재한다.
    - 모든(every) 양의 정수 n에 대하여, m이 n보다 작거나 같은 property를 가진 양의 정수 m이 존재한다.



**1.2 The Language of Sets**

**Set-Roster Notation**

**(1)**

S가 집합일 때,
$$
x \in S
$$
x는 S의 element이다.
$$
x \notin S
$$
x는 S의 element가 아니다.

**(2)** set-roaster notation

집합은 중괄호 안의 모든 elements를 집어넣는 **set-roaster notation**으로 명시해야한다.
$$
\{1, 2, 3\}
$$
element로 1, 2, 3을 가진다.
$$
\{1, 2, 3, ..., 100\}
$$
1부터 100까지의 모든 정수의 집합이다.
$$
\{1, 2, 3, ...\}
$$
infinite set을 표현할 수 있다.

**(3) ...**

...는 **ellipsis**라고 불리며, '등등'이라고 읽는다.



**Axiom of Extension**

- set는 elements가 무엇인지로 완전히 결정된다. element의 순서나, 한 번 이상 들어갔는지는 상관하지 않는다.



**Symbol**

- **R** : 모든 실수의 집합
- **Z** : 모든 정수의 집합
- **Q** : the set of all rational numbers, or quotients of integers (??)
- **+** or **-** or ***nonneg*** : 양수 혹은 음수 혹은 nonnegative로만 이루어진 elements의 집합
- **N** : nonnegative 정수의 집합 = natural numbers의 집합. 어떤 사람들은 양의 정수만 자연수라 하기도 한다. (이 책에서는 ***natural numbers***로 nonnegative integer와 구분한다.)
- 예:

$$
R^+
$$

양의 실수의 집합
$$
Z^{nonneg}
$$
nonnegative 정수(0, 1, 2, 3, 4, ...)의 집합



**line에서 집합 표시하기**

- number 0은 middle point와 상응하며, *origin*이라고 부른다.
- 실수의 집합은 세 부분으로 나눌 수 있다.
  - 양의 실수의 집합
  - 음의 실수의 집합
  - 숫자 0 : neither positive nor negative
- *continuous*: 실수 line은 어떤 hole도 없으므로 *continuous*(연속적)라고 불린다.
- 정수의 집합은 실수 line에서 일정한 간격에 위치한 point의 모임과 대응하므로, 모든 정수는 실수이다.
- *discrete*: 정수 line은 모든 서로 다른 것들과 분리되어있으므로 *discrete*(불연속적)라고 불린다.



**Set-Builder Notation**

S는 집합이고, P(x)는 S의 집합이거나 집합이 아닐 수 있는 특징을 가진다고 하자.

**P(x)가 참인 모든 S의 element x의 집합**
$$
\{x \in S\ |\ P(x)\}
$$

$$
\{ x \in S\}
$$



**1.2.1 Subsets**

**Definition[Subset]**

A와 B가 집합일 때, A의 모든 element가 B의 element인 경우, 그리고 오직 이 경우에만 A는 B의 **subset(부분집합)**이다.
$$
\{ A\subseteq B\}\quad 모든\ \mathbf {element}\ x에\ 대하여\ x \in A이면\ x \in B이다.
$$
모든 element x에 대하여, x가 A에도 속하고 B에도 속함을 의미한다.

"A는 B에 포함된다"와 "B는 A를 포함한다"는  phrases은 A가 B의 부분집합이라는 것을 의미한다.



- 정의에 따르면 "A는 B의 부분집합이 아니다"는 A의 element 중 적어도 하나가 B의 element가 아니라는 것을 의미한다.

$$
\{ A\nsubseteq B\} \quad x \in A이며\ x \notin B인\ x가\ 적어도\ 하나는\ 존재한다.
$$



**Definition[Proper Subset]**

A와 B가 집합이라고 하자. A의 모든 element가 B에 속하고, B의 element 중 적어도 하나가 A에 속하지 않는 경우, 그리고 오직 이 경우에만 A는 B의 **proper subset(진부분집합)**이다.



**1.2.2 Cartesian Products**

- 순서가 있는 쌍은 다음과 같은 형태의 집합이다.

$$
\{\{a\}, \{a, b\}\}
$$

a가 b가 아니라면, 두 집합 {a}와 {a, b}는 서로 다른 집합이다.

a가 b라면, 위 순서쌍은 {{a}, {a, a}}가 될 테고, 이는 {{a}}와 같다.



**Notation[ordered pair]**

주어진 element a, b에 대하여 *(a, b)*는 a와 b로 이루어져 있는 **ordered pair(순서쌍)**이며, a가 첫번째 element이고 b가 두번째 element라고 명시한다.

두 순서쌍 *(a, b)*와 *(c, d)*는 *a* = *c* 이고 *b* = *d*인 경우, 그리고 오직 이 경우에만 동일하다. 
$$
(a, b) = (c,d) \quad a=c\ 그리고\ b=d이다.
$$


**Definition[ordered n-tuple]**

n이 양의 정수이고, x1, x2, ..., xn이 element라고 하자. **ordered n -tuple(x1, x2, ..., xn)**은 첫번째가 x1이고, 두번째가 x2이고, n번째가 xn인 x1, x2, ..., xn으로 이루어져있다.

ordered 2-tuple은 **ordered pair(순서쌍)**이라고 하며, ordered 3-tuple은 **ordered triple**이라고한다.

두 ordered n-tuple (x1, x2, ..., xn)과 (y1, y2, ..., yn)은 x1 = y1이고 x2 = y2, ...xn = yn인 경우, 그리고 오직 이 경우에만 **동일하다(equal)**.
$$
(x_1, x_2, ..., x_n)=(y_1, y_2, ..., y_n)\Longleftrightarrow x_1=y_1,\ x_2=y_2,\ x_n=y_n
$$


**Definition[Cartesian product]**

주어진 집합 A1, A2, ..., An에 대하여, A1, A2, ..., An의 **Cartesian product**(A1 X A2 X ... X An)은 a1이 A1에 속하고, ..., an이 An에 속하는, 모든 ordered n-tuple (a1, a2, ..., an)의 집합이다.
$$
A_1\times A_2\times ...\times A_n = \{(a_1, a_2, ..., a_n)\ |\ a_1 \in A_1, a_2\in A_2, a_n\in A_n\}
$$
이때,
$$
A_1 \times A_2 = \{(a_1, a_2)\ |\ a_1 \in A_1\ 그리고\ a_2 \in A_2\}
$$
는 A1과 A2의 Cartesian product라고 한다.



**Cartesian plane**

cartesian plane을 CS에서 *strings*라고 부르는 객체로 표현한다.



**Definition**

n이 양의 정수라고 한다. 주어진 유한한 집합 A에 대하여,  **string of length n over A**는  괄호나 콤마 없이 쓰인 A의 element의 ordered n-tuple이다.

A의 element를 string의 **characters**라고 한다. 

**null string** over A는 character가 없는 "string"으로 정의된다. 길이가 0이며, 다음과 같은 기호로 표시된다.
$$
\lambda
$$
만약 A = {0, 1}이면 string over A는 **bit string**이라고 불린다.



**1.3 The Language of Relations and Functions**

**Definition[Relation]**

A와 B가 집합이라고 하자. **relation R from A to B**는 A X B의 부분집합이다. 주어진 A X B의 ordered pair (x, y)에 대하여, R 안에 (x,y)인 경우 그리고 오직 이 경우에만 **R에 의하여 x는 y와 연관된다**. x R y라고 쓴다. 집합 A는 R의 **domain(정의역)**이라고 하며 집합 B는 **co-domain(공집합)**이라고 한다.
$$
x\ R\ y \quad (x,y) \in R를\ 의미한다.
$$

$$
x\ R\ y \quad (x,y) \notin R를\ 의미한다.
$$

**1.3.1 Arrow Diagram of a Relation**

(나중에)



**1.3.2 Functions**

**Definition[Function]**

**집합 A부터 B까지의 함수 F**는 domain A와 co-domain B 간의 relation이며, 다음과 같은 두 property를 만족한다.

(1) A의 모든 element x에 대하여, "(x, y)가 F에 속한다"를 만족하는 element y가 B에 존재한다.

(2) A의 모든 element x와 B의 y 그리고 z에 대하여,
$$
만약\ (x,y) \in F\ 그리고\ (x,z) \in F이면,\ y=z이다.
$$


위 (1), (2)를 다음과 같이 덜 formal하게 바꿀 수 있다.

A부터 B까지의 관계 F(relation *F* from *A* to *B*)는 다음과 같은 경우에, 그리고 오직 이 경우에만 함수이다.

(1) A의 모든 element는 F의 ordered pair의 첫번째 element이다.

(2) 어떤 F의 서로 다른 ordered pair도 동일한 첫번째 element를 가지지 않는다.



- 함수 정의에 따르면, 정의역 안 각각의 element는 co-domain의 element와 일대일대응한다.
- 더 정확히는 F가 집합 A부터 B까지의 함수이면, 주어진 A의 모든 element에 대하여 다음과 같은 두 property를 보장한다.
  - 함수 정의에 의하여, B의 element 중 적어도 하나는 F에 의하여 x와 연관되어 있다.
  - 이 element는 기껏해야 하나 존재한다.



**Function Notation**

A와 B가 집합이고, F가 A부터 B까지의 함수라고 할 때, 주어진 A의 모든 element x에 대하여, F에 의해 x에 연관된 B 안의 unique한 element는 "**F of x**"라고 읽는 **F(x)**로 표기한다.



**1.4 The Language of Graphs**

- dot는 *vertex*라고 한다.
- vertices를 잇는 line segment는 *edge*라고 한다.



**Definition[Graph]**

**graph(그래프)** G는 두 개의 유한한 집합으로 구성된다: 비어있지 않은 **vertices**의 집합 *V(G)*과 **edges**의 집합 E(G)인데, 각각의 edge는 **endpoints**라고 불리는 한 개 혹은 두 개의 vertices로 이루어진 집합과 연관되어있다. edges부터 endpoint까지의 대응을 **edge-endpoint function**이라고 부른다.

한 개의 endpoint만을 가진 edge를 **loop**라고 하며, 동일한 endpoints의 집합을 가진 두 개 이상의 서로 다른 edges를 **parallel**하다고 한다. edge는 그것의 endpoints와 **connect(연결)**되어있다고도 한다. edge에 의하여 연결된 두 개의 vertices는 **adjacent(인접하다)**라고 하며, loop의 endpoint인 vertex를 **adjacent to itself(그 자체에 인접하다)**라고 한다.

edge는 그것의 endpoints 각각에 **incident on**되어 있다고 하며, 동일한 endpoint에 incident on 한 두 개의 edges는 **adjacent**라고 한다. 어떤 edges도 incident하지 않은 vertex는 **isolated**되었다고 한다.



**Definition[Diagraph]**

**directed graph(방향 그래프)** 혹은 **digraph**는 두 개의 유한한 집합으로 이루어져있다: 비어있지 않은 vertices의 집합 V(G)와 directed edges의 집합 D(G)인데, 각각은 그것의 **endpoints**라고 불리는 vertices의 ordered pair와 연관되어있다. edge *e*가 vertices pair (u, w)와 연관되어있다면, *e*는 u부터 w까지의 **(directed) edge**라고 불린다.