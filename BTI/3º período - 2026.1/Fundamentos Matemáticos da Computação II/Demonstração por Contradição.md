Na demonstração por contradição nós mantemos a premissa e negamos a conclusão. Ou seja, supomos que vale a premissa e a negação da conclusão:

$$
\lnot (P \implies Q) \equiv P \land \lnot Q
$$

Isso irá gerar um absurdo.

> É diferente da demonstração por contraposição.

**Exemplo 1:** $\sqrt{2}$ é irracional.

> Note que este exemplo não tem premissa, apenas conclusão. [adicionar isso ao arquivo anterior]

Suponha, por contradição, que $\sqrt{2}$ é racional.

Por definição de número racional, existem inteiros $p$ e $q$, com $q \neq 0$, tais que $\sqrt{2} = \frac{p}{q}$.

Calculamos:

\sqrt 2 = p/q
2 = p^2/q^2
2q^2 = p^2 (I)

Logo, por definição de número par, p^2.
Como p^2 é par, logo p é par.
Isto é, existe x inteiro tal que p = 2x.

Substituindo em (I):

2q^2 = (2x)^2
2q^2 = 4x^2
q^2 = 2x^2

Logo q^2 é par e, de forma análoga, q é par.

Absurdo, pois se p e q são pares, p/q não é irredutível.

Portanto, \sqrt 2 é racional.

**Exemplo 2:** Pelo menos 4 de 22 dias quaisquer caem em cada dia de uma mesma semana.

Suponha, por contradição, que no máximo 3 dias caem em cada dia da semana.

Como são 7 dias na semana, teremos, no máximo, 21 dias distribuídos.

Absurdo, pois temos um total de 22 dias.

**Exemplo 3:** Se 3n + 2 é par, então n é par.

[fizemos por contraposição na aula passada]

Seja n inteiro.

Suponha que **3n + 2 é par** (hipótese). (1)

Suponha que **n é ímpar** (negação da conclusão). (2)

Pela definição de ímpar, existe k \in Z tal que **n = 2k + 1**. (3)

Substituindo (3) em (1):

$3n + 2 = 3(2k + 1) + 2 = 6k + 3 + 2 = 6k + 4 + 1 = 2(3k + 2) + 1$

Como 3k + 2 \in Z, logo 3n + 2 é ímpar, o que contradiz (1).

Portanto, n é par.

---

**Demonstrando equivalências:**

**Exemplo 4:** Dado um inteiro n, n é par se, e somente se, n^2 é par.

Separamos em duas partes:
- Se n é par,então n^2 é par.
- Se n^2 é par, então n é par.

**Exemplo 5:** Seja n \in Z. As seguintes afirmações são equivalentes:

1. n é par
2. n - 1 é ímpar
3. n^2 é par
4. 3n + 2 é par

**Exemplo 6:** Seja n um inteiro positivo. Se n \leq 4, então (n + 1)^3 \geq 3^n.

Separo em 4 casos:
- n = 1: (1 + 1)^3 = 2^3 = 8 \geq 3^1 = 3
- n = 2: ...
- n = 3: ...
- n = 4: ...

**Exemplo 7:** Seja n \in Z. Demonstre que n^2 \geq n.

Separo em 3 casos:
- n = 0:  0^2 = 0 \geq 0
- n \geq 1: n^2 \geq n [só multiplicar por n nos dois lados de n \geq 1]
- n \leq 1: n \leq -1 \leq 0 \leq n^2 [lema 1]

Por os três casos, vemos que n^2 \geq n para todo inteiro n.

--
**Lema 1:** para todo n inteiro, n^2 \geq 0

Separo em dois casos:
1. n \geq 0: n^2 \geq 0
2. n \leq 0: n^2 \leq 0

Por (1) e (2), n^2 \geq 0 para todo n inteiro.

--

**Exemplo 8:** Todo número primo é ímpar.

Vamos apresentar um contra-exemplo, isto é, uma testemunha de que a afirmação é falsa.

> Negação: Pelo menos um número primo é par.

A afirmação é falsa, pois 2 é primo e par.

**Exemplo 9:** Todo número primo é par.

A afirmação é falsa pois 11 é primo e não é par.

**Exemplo 10:** Existe um número par que é ímpar.

Precisaríamos demonstrar que não existe tal número, ou seja, que todo número que é par não é ímpar e vice-versa.

**Exemplo 11:** Se n = ab, com a e b inteiros positivos, então a \leq \sqrt n ou b \leq \sqrt n. [por contraposição, por casos e por contradição]

**Exemplo 12:** Sejam a, b \in R. As seguintes afirmações são equivalentes:
1. a < b
2. (a + b)/2 > a
3. (a + b)/2 < b

**Exemplo 13:** Pelo menos um dos números reais a_1, a_2, e a_3 é maior ou igual à média desses números.

**Exemplo 14:** O produto de dois números irracionais é irracional.

**Exemplo 15:** Seja n inteiro. As seguintes afirmações são equivalentes:
1. n é par
2. n + 1 é ímpar
3. 3n + 1 é ímpar
4. 3n é par
