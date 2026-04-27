# Introdução

Considere:

$$
A \times B = \{ (a, b) \mid a \in A \land b \in B \}
$$

Uma relação $R$ é qualquer subconjunto de $A \times B$.

# Representação

A relação $R$ pode ser representada nas formas:

- $(a, b) \in R$
- $a\ R\ b$
- $R\ a\ b$
- $R(a, b)$

# Exemplos

Considerando $A = B = \mathbb{Z}$, temos:

- $R_1 = \emptyset$
- $R_2 = \{(a, b) \mid a \text{ divide } b\}$
- $R_3 = \{ (a, b) \mid a \leq b \}$
- $R_4 = \{ (a, b) \mid a > b \}$
- $R_5 = \{ (a, b) \mid a = b \}$
- $R_6 = \{ (a, b) \mid a = b \lor a = -b \}$
- $R_7 = \{ (a, b) \mid a = b + 1 \}$
- $R_8 = \{ (a, b) \mid a + b \leq 3 \}$

Mais exemplos com $A \times B = \{ 1, 2, 3, 4\}$:

- $R_9 = \{ (1, 1), (1, 2) \}$
[mais exemplos]
# Propriedades

## Reflexividade

Uma relação $R \subseteq A \times A$ é reflexiva se, e somente se, para todo $a \in R$, $a\ R\ a$.

> Exemplos: $R_3$, $R_5$, $R_6$, $R_{13}$

## Simetria

Uma relação $R \subseteq A \times A$ é simétrica se, e somente se, para todo $a, b \in R$, $a\ R\ b \implies b\ R\ a$.

> Exemplos: $R_{13}$, $R_{10}$, $R_1$, $R_5$, $R_6$, $R_8$

## Antissimetria

Uma relação $R \subseteq A \times A$ é antissimétrica se, e somente se, para todo $a, b \in R$, $a\ R\ b \land b\ R\ a \implies a = b$.

> Exemplos: $R_1$, $R_2$, $R_3$, $R_4$, $R_5$, $R_6$, $R_7$, $R_{11}$, $R_{12}$

## Transitividade

Uma relação $R \subseteq A \times A$ é transitiva se, e somente se, para todo $a, b, c \in R$, $a\ R\ b \land b\ R\ c \implies a\ R\ c$.

> Exemplos: $R_1$, $R_2$, $R_3$, $R_4$, $R_5$, $R_6$, $R_{11}$, $R_{12}$, $R_{13}$

# Composição

Sejam $R \subseteq A \times B$ e $S \subseteq B \times C$. A composição de $R$ com $S$ é:

$$
S \circ R = \{ (a, c) \mid \exists b \in B, a\ R\ b \land b\ S\ c \}
$$

# Inversa

Seja $R \subseteq A \times B$.

$$
R^{-1} = \{ (b, a) \mid (a, b) \in R \}
$$

$$
Dom(R) = \{ a \in A \mid \exists b \in B, (a, b) \in R \}
$$

$$
Ran(R) = Img(R) = \{ b \in B \mid \exists a \in A, (a, b) \in R \}
$$

# Propriedades (pt. 2)

### Injetividade

$R$ é injetiva se, e somente se, para todo $a_1, a_2 \in A$, para todo $b \in B$:

$$
a_1\ R\ b \land a_2\ R\ b \implies a_1 = a_2
$$

### Funcionalidade

$R$ é funcional se, e somente se, para todo $b_1, b_2 \in B$, para todo $a \in A$:

$$
a\ R\ b_1 \land a\ R\ b_2 \implies b_1 = b_2
$$

### Sobrejetividade

$R$ é sobrejetiva se, e somente se, para todo $b \in B$, existe $a \in A$ tal que $(a, b) \in R$.

### Totalidade

$R$ é total se, e somente se, para todo $a \in A$, existe $b \in B$ tal que $(a, b) \in R$.

# Ordem

[foto]

## Ordem Parcial

$R \subseteq A \times A$ é uma relação de ordem parcial se, e somente se, $R$ é:

- Reflexiva;
- Antissimétrica;
- Transitiva.

> Exemplos: $R_1$, $R_3$, $R_4$, $R_6$

## Ordem Total

$R \subseteq A \times A$ é uma relação de ordem total se, e somente se, $R$ é parcial e:

$$
\forall a, b \in A, a\ R\ b \lor b\ R\ a
$$

> Exemplos: $R_6$

# Definições

Sejam $R \subseteq A \times A$ uma relação de ordem parcial, $B \subseteq A$, $a \in A$ e $b \in B$.

## Mínimo

$b$ é o menor elemento (ou o elemento mínimo) de $B$ se, e somente se:

$$
\forall x \in B, b\ R\ x
$$

## Minimal

$b$ é o elemento minimal de $B$ se, e somente se:

$$
\nexists x, x\ R\ b \land x \neq b
$$

## Máximo

...

## Maximal

...

## Limitante Inferior

$a$ é limitante inferior de $B$ se, e somente se:

$$
\forall x \in B, a\ R\ x
$$

## Maior Limitante Inferior

Sejam $L = \{ x \mid x \text{ é limitante inferior de } B \}$ e $l \in L$.

$l$ é o maior limitante inferior de $B$ se, e somente se:

$$
\forall x \in L, x\ R\ l
$$

## Limitante Superior

...

## Menor Limitante Superior

...

# Exercícios

Sejam $R_1 \subseteq A \times A$ e $R_2 \subseteq B \times B$.

## Ex. 1

> [!example] Proposição
> Se $R_1$ e $R_2$ são reflexivas, então $R_1 \cup R_2$ é reflexiva.

**Demonstração:**

Sejam $R_1$ (H1) e $R_2$ (H2) relações reflexivas.

Seja $x \in A \cup B$. Logo $x \in A$ ou $x \in B$.

**Caso $x \in A$:**

Por (H1), $(x, x) \in R_1$. Logo $(x, x) \in R_1 \cup R_2$.

**Caso $x \in B$:**

Pela (H2), $(x, x) \in R_2$. Logo $(x, x) \in R_1 \cup R_2$.

De ambos os casos, $(x, x) \in R_1 \cup R_2$. Portanto, $R_1 \cup R_2$ é reflexiva. $\blacksquare$

## Ex. 2

> [!example] Proposição
> Se $R_1$ e $R_2$ são simétricas, então $R_1 \cup R_2$ é simétrica.

**Demonstração:**

Sejam $R_1$ (H1) e $R_2$ (H2) relações simétricas.

Sejam $a, b \in A \cup B$.

Suponha $(a, b) \in R_1 \cup R_2$.

**Caso $(a, b) \in R_1$:**

Por (H1), $(b, a) \in R_1$. Logo $(b, a) \in R_1 \cup R_2$.

**Caso $(a, b) \in R_2$:**

Por (H2), $(b, a) \in R_2$. Logo $(b, a) \in R_1 \cup R_2$.

De ambos os casos, $(b, a) \in R_1 \cup R_2$. Portanto $R_1 \cup R_2$ é simétrica. $\blacksquare$

## Ex. 3

> [!example] Proposição
> Se $R_1$ e $R_2$ são transitivas, então $R_1 \cup R_2$ é transitiva.

**Refutação:**

Considere $A = B = \{ a, b, c \}$.

Tome $R_1 = \{(a, b)\}$ e $R_2 = \{(b, c)\}$. Note que ambas as relações são transitivas. No entanto, $R_1 \cup R_2 = \{(a, b), (b, c)\}$ não é transitiva.

Portanto, $R_1 \cup R_2$ não é transitiva. $\blacksquare$

## Ex. ?

> [!example] Proposição
> $R$ é transitiva se, e somente se, $R \circ R \subseteq R$.

**Demonstração:**

**Parte 1 ($\implies$):**

Suponha que $R$ é transitiva.

Seja $(x,y) \in R \circ R$.

Pela definição de composição, existe $i \in A$ tal que $(x,i) \in R$ e $(i,y) \in R$.

Pela hipótese, $(x,y) \in R$.

**Parte 2 ($\impliedby$):**

Suponha que $R \circ R \subseteq R$.

Sejam $x, y, z \in R$.

Suponha $R(x, y)$ e $R(y, z)$.

Por composição, $(x, z) \in R \circ R$.

Pela hipótese, $(x, z) \in R$.

## Ex. 4

> [!example] Proposição
> ...

[foto]

# Exercícios (pt. 2)

## Ex. 1

Considere $R \subseteq A \times B$. Demonstre as seguintes proposições.

> [!example] Proposição
> $(R^{-1})^{-1} = R$

...

> [!example] Proposição
> $Dom(R^{-1}) = Ran(R)$

...

> [!example] Proposição
> $(S \circ R)^{-1} = R^{-1} \circ S^{-1}$

...

> [!example] Proposição
> $Dom(S \circ R) \subseteq Dom(R)$

...

## Ex. 2

Considere:

- $A = \{ 1, 2, 3 \}$;
- $B = \{ 4, 5, 6 \}$;
- $R = \{ (1, 4), (1, 5), (2, 5), (3, 6) \} \subseteq A \times B$;
- $S = \{ (4, 5), (4, 6), (5, 4), (6, 6) \} \subseteq B \times B$.

**a)** Encontre:

> [!example] Exercício
> $S \circ R$

...

> [!example] Exercício
> $S \circ S^{-1}$

...

**b)** Verifique quais das relações $R$, $S$, $S \circ R$ e $S \circ S^{-1}$ são injetivas, funcionais, sobrejetivas e totais.

...

## Ex. 3

Considere $R \subseteq A \times B$. Suponha $R$ funcional.

> [!example] Proposição
> $R^{-1}$ é funcional se, e somente se, $R$ é injetiva.

...

## Ex. 4

Considere $R \subseteq A \times B$ e $S \subseteq B \times C$.

> [!example] Proposição
> Se $R$ e $S$ são funcionais, então $S \circ R$ é funcional.

...

> [!example] Proposição
> Se $R$ e $S$ são totais, então $S \circ R$ é total.

...

# Exercícios (pt. 3)

Sejam $R \subseteq A \times A$ uma relação de ordem parcial e $B \subseteq A$.

## Ex. 1

> [!example] Proposição
> Se $B$ possui um menor elemento, então esse elemento é único.

...

## Ex. 2

> [!example] Proposição
> Se $b$ é o menor elemento de $B$, então $b$ é o elemento minimal de $B$. Além disso, $b$ é o único elemento minimal de $B$.

...

## Ex. 3

> [!example] Proposição
> Se $R$ é uma ordem total e $b$ é um elemento minimal de $B$, então $b$ é o único elemento minimal de $B$.

...

## Ex. 4

> [!example] Proposição
> Se $R$ é uma ordem total e $b$ é um elemento minimal de $B$, então $b$ é o menor elemento de $B$.

...

# Exercícios (pt. 4)

## Ex. 1

Sejam $R \subseteq A \times B$ e $S, T \subseteq B \times C$.

> [!example] Proposição
> $(S \cap T) \circ R \subseteq (S \circ R) \cap (T \circ R)$

**Demonstração:**

Seja $(a, c) \in (S \cap T) \circ R$.

Pela definição de composição, existe $b \in B$ tal que $(a, b) \in R$ (1) e $(b, c) \in S \cap T$ (2).

De (2), pela definição de interseção, então $(b, c) \in S$ (3) e $(b, c) \in T$ (4).

Pela definição de composição, de (1) e (3), temos que $(a, c) \in S \circ R$ (5).

De (1) e (4), temos que $(a, c) \in T \circ R$ (6).

Pela definição de interseção, de (5) e (6), segue que $(a, c) \in (S \circ R) \cap (T \circ R)$. $\blacksquare$

> [!example] Proposição
> $(S \circ R) \cap (T \circ R) \subseteq (S \cap T) \circ R$

**Refutação:**

Vamos apresentar um contra-exemplo.

Tome $A = B = C = \{1,2,3\}$.

Considere:

- $R = \{ (1, 1), (1, 2) \}$;
- $S = \{(1, 2\}$;
- $T = \{(2, 1)\}$.

Note que $S \circ R = \{(1, 2)\}$ e $T \circ R = \{(1, 2\}$, logo $(S \circ R) \cap (T \circ R) = \{(1, 1)\}$.

Veja também que $S \cap T = \emptyset$, logo $(S \cap T) \circ R = \emptyset$.

Portanto $(S \circ R) \cap (T \circ R) \nsubseteq (S \cap T) \circ R$. $\blacksquare$

## Ex. 2

Seja $R \subseteq A \times A$ tal que $R$ é simétrica e transitiva.

> [!example] Proposição
> $\forall x \in A, \exists y \in A, x\ R\ y \implies R \text{ é reflexiva}$

**Demonstração:**

Suponha que, para todo $x \in A$, existe $y \in A$ tal que $x\ R\ y$.

Seja $a \in A$.

Pela hipótese inicial, existe $a' \in A$ tal que $a\ R\ a'$.

Como $R$ é simétrica, logo $a'\ R\ a$. Como $R$ é transitiva, logo $a\ R\ a$.

Portanto $R$ é reflexiva. $\blacksquare$

## Ex. 3

Ache os fechos de:

**a)**

[foto]

**b)** $R = \{ (x, y) \in \mathbb{R} \times \mathbb{R} \mid x < y \}$

Fecho reflexivo: $R_r = \{ (x, y) \in \mathbb{R} \times \mathbb{R} \mid x \leq y \}$.
Fecho simétrico: $R_s = \{ (x, y) \in \mathbb{R} \times \mathbb{R} \mid x \neq y \}$.
Fecho transitivo: $R_t = R$.

## Ex. 4

Sejam $R_1, R_2 \subseteq A \times A$, $R_1 \subseteq R_2$, $B \subseteq A$ e $b \in B$.

> [!example] Proposição
> $b \text{ menor elemento em } R_1 \implies b \text{ menor elemento em } R_2$

Suponha que $b$ é o menor elemento de $B$ em $R_1$, isto é, $\forall x \in B, b\ R_1\ x$.

Seja $b' \in B$. Logo $b\ R_1\ b'$.

Como $R_1 \subseteq R_2$, então $b\ R_2\ b'$. $\blacksquare$
