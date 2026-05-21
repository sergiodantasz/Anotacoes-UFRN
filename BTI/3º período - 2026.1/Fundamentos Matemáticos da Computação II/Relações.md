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

# Propriedades

## Reflexividade

Uma relação $R \subseteq A \times A$ é reflexiva se, e somente se, para todo $a \in A$, $a\ R\ a$.

> Exemplos: $R_3$, $R_5$, $R_6$

## Simetria

Uma relação $R \subseteq A \times A$ é simétrica se, e somente se, para todo $a, b \in A$, $a\ R\ b \implies b\ R\ a$.

> Exemplos: $R_1$, $R_5$, $R_6$, $R_8$

## Antissimetria

Uma relação $R \subseteq A \times A$ é antissimétrica se, e somente se, para todo $a, b \in A$, $a\ R\ b \land b\ R\ a \implies a = b$.

> Exemplos: $R_1$, $R_2$, $R_3$, $R_4$, $R_5$, $R_6$, $R_7$

## Transitividade

Uma relação $R \subseteq A \times A$ é transitiva se, e somente se, para todo $a, b, c \in A$, $a\ R\ b \land b\ R\ c \implies a\ R\ c$.

> Exemplos: $R_1$, $R_2$, $R_3$, $R_4$, $R_5$, $R_6$

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

# Relações

Seja $R \subseteq A \times B$.

### Injetividade

$R$ é injetiva se, e somente se, para todo $a_1, a_2 \in A$, para todo $b \in B$:

$$
a_1\ R\ b \land a_2\ R\ b \implies a_1 = a_2
$$

### Funcionalidade

$R$ é funcional se, e somente se, para todo $a \in A$, para todo $b_1, b_2 \in B$:

$$
a\ R\ b_1 \land a\ R\ b_2 \implies b_1 = b_2
$$

### Sobrejetividade

$R$ é sobrejetiva se, e somente se, para todo $b \in B$, existe $a \in A$ tal que $(a, b) \in R$.

### Totalidade

$R$ é total se, e somente se, para todo $a \in A$, existe $b \in B$ tal que $(a, b) \in R$.

# Relações de Ordem

## Ordem Parcial

$R \subseteq A \times A$ é uma relação de ordem parcial se, e somente se, $R$ é:

- Reflexiva;
- Antissimétrica;
- Transitiva.

## Ordem Total

$R \subseteq A \times A$ é uma relação de ordem total se, e somente se, $R$ é parcial e:

$$
\forall a, b \in A, a\ R\ b \lor b\ R\ a
$$

## Elementos

Sejam $R \subseteq A \times A$ uma relação de ordem parcial, $B \subseteq A$, $a \in A$ e $b \in B$.

### Mínimo

$b$ é o menor elemento (ou o elemento mínimo) de $B$ se, e somente se:

$$
\forall x \in B, b\ R\ x
$$

### Minimal

$b$ é o elemento minimal de $B$ se, e somente se:

$$
\nexists x \in B, x\ R\ b \land x \neq b
$$

$$
\forall x \in B, x\ R\ b \implies x = b
$$

### Máximo

$b$ é o maior elemento (ou o elemento máximo) de $B$ se, e somente se:

$$
\forall x \in B, x\ R\ b
$$

### Maximal

$b$ é o elemento maximal de $B$ se, e somente se:

$$
\forall x \in B, b\ R\ x \implies x = b
$$

### Limitante Inferior

$a$ é limitante inferior de $B$ se, e somente se:

$$
\forall x \in B, a\ R\ x
$$

### Maior Limitante Inferior (Ínfimo)

Sejam $L = \{ x \in A \mid x \text{ é limitante inferior de } B \}$ e $l \in L$.

$l$ é o maior limitante inferior de $B$ se, e somente se:

$$
\forall x \in L, x\ R\ l
$$

### Limitante Superior

$a$ é limitante superior de $B$ se, e somente se:

$$
\forall x \in B, x\ R\ a
$$

### Menor Limitante Superior (Supremo)

Sejam $L = \{ x \in A \mid x \text{ é limitante superior de } B \}$ e $l \in L$.

$l$ é o maior limitante superior de $B$ se, e somente se:

$$
\forall x \in L, l\ R\ x
$$

# Relação de Equivalência

Uma relação $R \subseteq A \times A$ é uma relação de equivalência se, e somente se, $R$ é:

- Reflexiva;
- Transitiva;
- Simétrica.

# Fechos

Dado que uma relação $R$ não satisfaz uma propriedade $P$, o fecho de $R$ com respeito a $P$ é a menor relação que contém $R$ e satisfaz $P$.

Ou seja, o fecho é exatamente a relação original $R$ "somada" ao número mínimo estritamente necessário de novos pares para satisfazer $P$.

## Fecho Reflexivo

$$
R_{ref} = R \cup i_A
$$

> Basta unir com o conjunto de todos os pares onde $x$ se relaciona com ele mesmo.

## Fecho Simétrico

$$
R_{sim} = R \cup R^{-1}
$$

> Basta garantir que, para cada "ida" que já existe em $R$, também existirá a "volta".

## Fecho Transitivo

$$
R_{trans} = \cup_{i=1}^{\infty}{R^i}
$$

Onde:

- $R^1 = R$;
- $R^n = R^{n-1} \circ R$.

## Fecho de Equivalência

É a menor relação de equivalência possível que contém $R$.

# Partição

Uma partição é um conjunto formado por subconjuntos (sem números repetidos que já estão em outros subconjuntos) cuja união é o conjunto no qual a partição se baseia.

> Toda relação de equivalência define uma partição.

Seja $A$ um conjunto e $F \subseteq P(A)$.

$F$ é uma partição de $A$ se, e somente se:

- $\cup_{X \in F}{X} = A$ (a união de todos os blocos é o próprio conjunto $A$);
- $\forall X, Y \in F, X \neq Y \implies X \cap Y = \emptyset$ (os blocos são dois a dois disjuntos);
- $\forall X \in F, X \neq \emptyset$ (nenhum bloco é vazio).

**Exemplo:**

$A = \{1, 2, 3, 4, 5\}$

$P_1 = \{\{1\}, \{2, 3, 4\}, \{5\}\}$
$P_2 = \{\{1, 2, 3\}, \{4, 5\}\}$

# Classe de Equivalência

A classe de equivalência de $x$ com respeito a $R$ é dada por:

$$
[x]_R = \{ y \mid (x, y) \in R \}
$$

$[x]_R$ é o conjunto de todos os elementos com os quais $x$ se relaciona por $R$.

# Conjunto Quociente

O conjunto de todas as classes de equivalência de $A$ por $R$ é o conjunto quociente de $A$ módulo $R$:

$$
\begin{align}
A / R &= \{ [x]_R \mid x \in A \} \\
      &= \{ X \subseteq A \mid \exists x \in A, X = [x]_R \}
\end{align}
$$

# Exercícios (2.1)

Sejam $R_1 \subseteq A \times A$ e $R_2 \subseteq B \times B$. Demonstre ou refute:

## Ex. (a)

> [!example] Proposição
> Se $R_1$ e $R_2$ são reflexivas, então $R_1 \cup R_2$ é reflexiva.

**Demonstração:**

Suponha que $R_1$ (H1) e $R_2$ (H2) são reflexivas.

Seja $x \in A \cup B$. Logo $x \in A$ ou $x \in B$.

**Caso $x \in A$:**

Por (H1), $(x, x) \in R_1$. Logo $(x, x) \in R_1 \cup R_2$.

**Caso $x \in B$:**

Pela (H2), $(x, x) \in R_2$. Logo $(x, x) \in R_1 \cup R_2$.

De ambos os casos, $(x, x) \in R_1 \cup R_2$. Portanto $R_1 \cup R_2$ é reflexiva. $\blacksquare$

## Ex. (b)

> [!example] Proposição
> Se $R_1$ e $R_2$ são simétricas, então $R_1 \cup R_2$ é simétrica.

**Demonstração:**

Suponha que $R_1$ (H1) e $R_2$ (H2) são simétricas.

Sejam $a, b \in A \cup B$.

Suponha $(a, b) \in R_1 \cup R_2$.

**Caso $(a, b) \in R_1$:**

Por (H1), $(b, a) \in R_1$. Logo $(b, a) \in R_1 \cup R_2$.

**Caso $(a, b) \in R_2$:**

Por (H2), $(b, a) \in R_2$. Logo $(b, a) \in R_1 \cup R_2$.

De ambos os casos, $(b, a) \in R_1 \cup R_2$. Portanto $R_1 \cup R_2$ é simétrica. $\blacksquare$

## Ex. (c)

> [!example] Proposição
> Se $R_1$ e $R_2$ são transitivas, então $R_1 \cup R_2$ é transitiva.

**Refutação:**

Considere $A = B = \{ a, b, c \}$.

Tome $R_1 = \{(a, b)\}$ e $R_2 = \{(b, c)\}$. Note que ambas as relações são transitivas. No entanto, $R_1 \cup R_2 = \{(a, b), (b, c)\}$ não é transitiva.

Portanto $R_1 \cup R_2$ não é transitiva. $\blacksquare$

## Ex. (d)

> [!example] Proposição
> Se $R_1$ e $R_2$ são reflexivas, então $R_1 \cap R_2$ é reflexiva.

**Demonstração:**

Sejam $R_1$ e $R_2$ relações reflexivas.

Seja $x \in A \cap B$. Logo $x \in A$ e $x \in B$.

Pelas hipóteses iniciais, temos $(x, x) \in R_1$ e $(x, x) \in R_2$. Pela definição de interseção, segue que $(x, x) \in R_1 \cap R_2$.

Portanto $R_1 \cap R_2$ é reflexiva. $\blacksquare$

## Ex. (e)

> [!example] Proposição
> Se $R_1$ e $R_2$ são simétricas, então $R_1 \cap R_2$ é simétrica.

**Demonstração:**

Suponha que $R_1$ e $R_2$ são simétricas.

Sejam $x, y \in A \cap B$. Logo $x \in A$, $x \in B$, $y \in A$ e $y \in B$.

Pelas hipóteses iniciais, temos $(x, y) \in R_1 \implies (y, x) \in R_1$ e $(x, y) \in R_2 \implies (y, x) \in R_2$.

Suponha $(x, y) \in R_1 \cap R_2$. Logo $(x, y) \in R_1$ e $(x, y) \in R_2$.

Disso e das implicações, segue que $(y, x) \in R_1$ e $(y, x) \in R_2$. Pela definição de interseção, $(y, x) \in R_1 \cap R_2$.

Portanto $R_1 \cap R_2$ é simétrica. $\blacksquare$

## Ex. (f)

> [!example] Proposição
> Se $R_1$ e $R_2$ são transitivas, então $R_1 \cap R_2$ é transitiva.

**Demonstração:**

Suponha que $R_1$ e $R_2$ são transitivas.

Sejam $x, y, z \in A \cap B$. Logo $x \in A$, $x \in B$, $y \in A$, $y \in B$, $z \in A$ e $z \in B$.

Suponha que $(x, y) \in R_1 \cap R_2$ e $(y, z) \in R_1 \cap R_2$. Logo $(x, y) \in R_1$, $(x, y) \in R_2$, $(y, z) \in R_1$ e $(y, z) \in R_2$.

Disso e das hipóteses iniciais, segue que $(x, z) \in R_1$ e $(x, z) \in R_2$. Sendo assim, temos $(x, z) \in R_1 \cap R_2$.

Portanto $R_1 \cap R_2$ é transitiva. $\blacksquare$

## Ex. (g)

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

Pela hipótese inicial, $(x, z) \in R$.

Portanto, pelas duas partes, concluímos a demonstração. $\blacksquare$

# Exercícios (4.1)

## Ex. 1

Considere $R \subseteq A \times B$ e $S \subset B \times C$. Demonstre as seguintes proposições.

> [!example] Proposição
> $(R^{-1})^{-1} = R$

**Parte $(R^{-1})^{-1} \subseteq R$:**

Seja $(x, y) \in (R^{-1})^{-1}$.

Pela definição de inversa, $(y, x) \in R^{-1}$. Novamente pela definição, temos $(x, y) \in R$.

**Parte $R \subseteq (R^{-1})^{-1}$:**

Seja $(x, y) \in R$.

Pela definição de inversa, $(y, x) \in R^{-1}$. Mais uma vez aplicando a definição, segue que $(x, y) \in (R^{-1})^{-1}$.

Portanto, pelas duas partes, concluímos que $(R^{-1})^{-1} = R$. $\blacksquare$

> [!example] Proposição
> $Dom(R^{-1}) = Ran(R)$

**Parte $Dom(R^{-1}) \subseteq Ran(R)$:**

Note que $R^{-1} \subseteq B \times A$.

Seja $b \in Dom(R^{-1})$. Logo existe $a \in A$ tal que $(b, a) \in R^{-1}$. Pela definição de inversa, temos que $(a, b) \in R$.

Disso e da definição de imagem, concluímos que $b \in Ran(R)$.

**Parte $Ran(R) \subseteq Dom(R^{-1})$:**

Seja $b \in Ran(R)$. Logo existe $a \in A$ tal que $(a, b) \in R$. Pela definição de inversa, temos $(b, a) \in R^{-1}$.

Disso e da definição de domínio, segue que $b \in Dom(R^{-1})$.

Portanto, pelas duas partes, $Dom(R^{-1}) = Ran(R)$. $\blacksquare$

> [!example] Proposição
> $(S \circ R)^{-1} = R^{-1} \circ S^{-1}$

**Parte $(S \circ R)^{-1} \subseteq R^{-1} \circ S^{-1}$:**

Seja $(c, a) \in (S \circ R)^{-1}$. Logo, pela definição de inversa, $(a, c) \in S \circ R$.

Pela definição de composta, existe $b \in B$ tal que $(a, b) \in R$ e $(b, c) \in S$. Disso temos que $(b, a) \in R^{-1}$ e $(c, b) \in S^{-1}$.

Logo, pela definição de composta, $(c, a) \in R^{-1} \circ S^{-1}$.

**Parte $R^{-1} \circ S^{-1} \subseteq (S \circ R)^{-1}$:**

Seja $(c, a) \in R^{-1} \circ S^{-1}$. Logo existe $b \in B$ tal que $(c, b) \in S^{-1}$ e $(b, a) \in R^{-1}$. Pela definição de inversa, $(b, c) \in S$ e $(a, b) \in R$.

Assim, pela definição de composta, segue que $(a, c) \in S \circ R$. Pela definição de inversa, temos $(c, a) \in (S \circ R)^{-1}$.

Portanto, pelas duas partes, $(S \circ R)^{-1} = R^{-1} \circ S^{-1}$. $\blacksquare$

> [!example] Proposição
> $Dom(S \circ R) \subseteq Dom(R)$

Seja $a \in Dom(S \circ R)$. Logo existe $c \in C$ tal que $(a, c) \in S \circ R$.

Pela definição de composta, existe $b \in B$ tal que $(a, b) \in R$ e $(b, c) \in S$. Disso e da definição de domínio, segue que $a \in Dom(R)$.

Portanto $Dom(S \circ R) \subseteq Dom(R)$. $\blacksquare$

## Ex. 2

Sejam os conjuntos $A = \{ 1, 2, 3 \}$ e $B = \{ 4, 5, 6 \}$ e as relações $R = \{ (1, 4), (1, 5), (2, 5), (3, 6) \} \subseteq A \times B$ e $S = \{ (4, 5), (4, 6), (5, 4), (6, 6) \} \subseteq B \times B$.

**a)** Encontre:

> [!example] Exercício
> $S \circ R$

$$
S \circ R = \{ (1, 5), (1, 6), (1, 4), (2, 4), (3, 6) \}
$$

> [!example] Exercício
> $S \circ S^{-1}$

$$
S^{-1} = \{ (5, 4), (6, 4), (4, 5), (6, 6) \}
$$

$$
S \circ S^{-1} = \{ (5, 5), (5, 6), (6, 5), (6, 6), (4, 4) \}
$$

**b)** Verifique quais das relações $R$, $S$, $S \circ R$ e $S \circ S^{-1}$ são injetivas, funcionais, sobrejetivas e totais.

$R$: não é injetiva, não é funcional, é sobrejetiva, é total.
$S$: não é injetiva, não é funcional, é sobrejetiva, é total.
$S \circ R$: não é injetiva, não é funcional, é sobrejetiva, é total.
$S \circ S^{-1}$: não é injetiva, não é funcional, é sobrejetiva, é total.

## Ex. 3

Seja $R \subseteq A \times B$.

> [!example] Proposição
> $R^{-1}$ é funcional se, e somente se, $R$ é injetiva.

**Parte ($\implies$):**

Suponha $R^{-1}$ funcional.

Sejam $a_1, a_2 \in A$ e $b \in B$.

Disso e da hipótese inicial, temos $(b, a_1) \in R^{-1} \land (b, a_2) \in R^{-1} \implies a_1 = a_2$ (1).

Suponha que $(a_1, b) \in R$ e $(a_2, b) \in R$. Pela definição de inversa, segue que $(b, a_1) \in R^{-1}$ e $(b, a_2) \in R^{-1}$.

Logo, disso e de (1), temos $a_1 = a_2$. Sendo assim, $R$ é injetiva.

**Parte ($\impliedby$):**

Suponha $R$ injetiva.

Sejam $b \in B$ e $a_1, a_2 \in A$.

Suponha que $(b, a_1) \in R^{-1}$ e $(b, a_2) \in R^{-1}$. Pela definição de inversa, $(a_1, b) \in R$ e $(a_2, b) \in R$.

Disso, da hipótese inicial e da definição de injetiva, obtemos $a_1 = a_2$. Logo $R^{-1}$ é funcional.

Portanto, pelas duas partes, concluímos a demonstração. $\blacksquare$

## Ex. 4

Considere $R \subseteq A \times B$ e $S \subseteq B \times C$.

> [!example] Proposição
> Se $R$ e $S$ são funcionais, então $S \circ R$ é funcional.

Suponha $R$ e $S$ funcionais.

Sejam $a \in A$ e $c_1, c_2 \in C$.

Suponha $(a, c_1) \in S \circ R$ (1) e $(a, c_2) \in S \circ R$ (2).

De (1), pela definição de composição, existe $b_1 \in B$ tal que $(a, b_1) \in R$ e $(b_1, c_1) \in S$.
De (2), existe $b_2 \in B$ tal que $(a, b_2) \in R$ e $(b_2, c_2) \in S$.

Como $R$ é funcional, $(a, b_1) \in R$ e $(a, b_2) \in R$, logo $b_1 = b_2$.
Como $S$ é funcional, $(b_1, c_1) \in S$ e $(b_2, c_2) \in S$, logo $c_1 = c_2$.

Portanto $S \circ R$ é funcional. $\blacksquare$

> [!example] Proposição
> Se $R$ e $S$ são totais, então $S \circ R$ é total.

Suponha $R$ e $S$ totais.

Seja $a \in A$.

Como $R$ é total e $a \in A$, logo existe $b \in B$ tal que $(a, b) \in R$ (1).
Como $S$ é total e $b \in B$, logo existe $c \in C$ tal que $(b, c) \in S$ (2).

Pela definição de composição, de (1) e (2) temos que $(a, c) \in S \circ R$.

Portanto $S \circ R$ é total. $\blacksquare$

# Exercícios (5.1)

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

# Exercícios (8.1)

## Ex. 1

Sejam $R \subseteq A \times B$ e $S, T \subseteq B \times C$.

> [!example] Proposição
> $(S \cap T) \circ R \subseteq (S \circ R) \cap (T \circ R)$

**Demonstração:**

Seja $(a, c) \in (S \cap T) \circ R$.

Pela definição de composição, existe $b \in B$ tal que $(a, b) \in R$ (1) e $(b, c) \in S \cap T$ (2).

Logo, de (2), temos $(b, c) \in S$ (3) e $(b, c) \in T$ (4).

Pela definição de composição, de (1) e (3) temos $(a, c) \in S \circ R$. Além disso, de (1) e (4), temos $(a, c) \in T \circ R$.

Assim, pela definição de interseção, segue que $(a, c) \in (S \circ R) \cap (T \circ R)$. $\blacksquare$

> [!example] Proposição
> $(S \circ R) \cap (T \circ R) \subseteq (S \cap T) \circ R$

**Refutação:**

Mostrarei agora que $(S \circ R) \cap (T \circ R) \nsubseteq (S \cap T) \circ R$ por meio de um contraexemplo.

Tome $A = \{ a \}$, $B = \{ b_1, b_2 \}$ e $C = \{ c \}$. Defino como relações $R = \{ (a, b_1), (a, b_2) \}$, $S = \{ (b_1, c) \}$ e $T = \{ (b_2, c) \}$.

Perceba que $S \circ R = \{ (a, c) \}$ e $T \circ R = \{ (a, c) \}$. Logo $(S \circ R) \cap (T \circ R) = \{ (a, c) \}$.

Agora note que $S \cap T = \emptyset$. Logo $(S \cap T) \circ R = \emptyset$. Como o conjunto vazio não possui elementos, é impossível $(a, c) \in (S \cap T) \circ R$ e a inclusão falha.

Assim, $(S \circ R) \cap (T \circ R) \nsubseteq (S \cap T) \circ R$.

Portanto, pela existência do contraexemplo, concluímos que $(S \cap T) \circ R \neq (S \circ R) \cap (T \circ R)$. $\blacksquare$

## Ex. 2

Seja $R \subseteq A \times A$ uma relação tal que $R$ é simétrica e transitiva.

> [!example] Proposição
> $\forall x \in A, \exists y \in A, x\ R\ y \implies R \text{ é reflexiva}$

**Demonstração:**

Suponha que, para todo $x \in A$, existe $y \in A$ tal que $(x, y) \in R$.

Seja $a \in A$.

Pela hipótese inicial, existe $a' \in A$ tal que $(a, a') \in R$.

Como $R$ é simétrica, logo $(a', a) \in R$. Como $R$ é transitiva, logo $(a, a) \in R$.

Portanto $R$ é reflexiva. $\blacksquare$

## Ex. 3

Ache os fechos de:

**a)** $A = \{ a, b, c, d\}$ e $R = \{ (a, a), (a, b), (b, c), (c, d) \}$

Fecho reflexivo: $R_r = \{ (a, a), (a, b), (b, c), (c, d), (b, b), (c, c), (d, d) \}$
Fecho simétrico: $R_s = \{ (a, a), (a, b), (b, a), (b, c), (c, b), (c, d), (d, c) \}$
Fecho transitivo: $R_t = \{ (a, a), (a, b), (b, c), (c, d), (a, c), (b, d), (a, d) \}$

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

> [!example] Proposição
> $b \text{ é minimal em } R_2 \implies b \text{ é minimal em } R_1$

Suponha que $b$ é minimal em $R_2$.

Seja $x \in B$.

Pela hipótese, se $(x, b) \in R_2$, então $x = b$ (1).

Suponha que $(x, b) \in R_1$.

Como $R_1 \subseteq R_2$, logo $(x, b) \in R_2$.

Portanto, de (1), temos que $x = b$. $\blacksquare$

# Exercícios (9.1)

## Ex. 1

> [!example] Exercício
> Seja $R$ uma relação em $A$. Prove que $R$ é simétrica e antissimétrica se, e somente se, $R \subseteq i_A$.

**Parte ($\implies$):**

Suponha que $R$ é simétrica (1) e antissimétrica (2).

Seja $(x, y) \in R$.

Logo, disso e de (1), $(y, x) \in R$.

Disso e de (2), temos $x = y$.

Pela definição de identidade, concluímos que $(x, y) \in i_A$.

**Parte ($\impliedby$):**

Suponha $R \subseteq i_A$.

**(I)** $R$ é simétrica:

Sejam $x, y \in A$.

Suponha que $(x, y) \in R$. Logo, pela hipótese inicial da parte, temos $(x, y) \in i_A$.

Dessa forma, pela definição de identidade, necessariamente $x = y$. Disso segue que $(x, y)$ é exatamente igual a $(y, x)$.

Sendo assim, como $(x, y) \in R$ e $(y, x) \in R$, concluímos que $R$ é simétrica.

**(II)** $R$ é antissimétrica:

Sejam $x, y \in A$.

Suponha que $(x, y) \in R$ e $(y, x) \in R$.

De forma análoga ao bloco (I), $(x, y) \in i_A$ e $(y, x) \in i_A$ e, consequentemente, $x = y$. Desse modo, $R$ é antissimétrica.

Portanto, pelas duas partes, concluímos a demonstração. $\blacksquare$

## Ex. 2

Suponha que $R_1$ e $R_2$ sejam ordens parciais em $A$. Para cada item, forneça uma prova ou um contraexemplo que justifique sua resposta.

> [!example] Exercício
> $R_1 \cap R_2$ deve ser uma ordem parcial em $A$?

...

> [!example] Exercício
> $R_1 \cup R_2$ deve ser uma ordem parcial em $A$?

...
