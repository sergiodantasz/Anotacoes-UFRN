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
