# Ordem Parcial

## Definição

$R \subseteq A \times A$ é uma relação de ordem parcial se, e somente se, $R$ é:

- Reflexiva;
- Antissimétrica;
- Transitiva.

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
\forall x \in B, x\ R\ b \implies x = b
$$

$$
\nexists x \in B, x\ R\ b \land x \neq b
$$

> Nenhum elemento se relaciona com $b$ além dele mesmo.

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

$$
\nexists x \in B, b\ R\ x \land x \neq b
$$

> Nenhum elemento fica "acima" de $b$, exceto ele próprio.

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

**Notação:**

Seja $\{ m, n \} \subseteq B$.

$$
l \text{ é o maior limitante inferior de } \{m, n\} \overset{def}{\iff} l = x \land y
$$

### Limitante Superior

$a$ é limitante superior de $B$ se, e somente se:

$$
\forall x \in B, x\ R\ a
$$

### Menor Limitante Superior (Supremo)

Sejam $L = \{ x \in A \mid x \text{ é limitante superior de } B \}$ e $l \in L$.

$l$ é o menor limitante superior de $B$ se, e somente se:

$$
\forall x \in L, l\ R\ x
$$

**Notação:**

Seja $\{ m, n \} \subseteq B$.

$$
l \text{ é o menor limitante superior de } \{m, n\} \overset{def}{\iff} l = x \lor y
$$

# Diagramas de Hasse

## Definição

O diagrama de Hasse é uma forma gráfica de representar um conjunto finito parcialmente ordenado (*poset*).

Seja um *poset* definido por $(A, \preceq)$, onde a relação é reflexiva, antissimétrica e transitiva.

O diagrama de Hasse simplifica as conexões entre os elementos do conjunto eliminando os grafos da reflexividade e da transitividade, além de atribuir o sentido de baixo para cima nas ligações.

Dizemos que $y$ cobre $x$ se $x \prec y$ (isto é, $x \preceq y$ e $x \neq y$) e não existe $z \in A$ tal que $x \prec z \prec y$.

## Cadeias

### Definição Intuitiva

Com quaisquer dois elementos ordenados corretamente numa cadeia de relações do diagrama, conseguimos relacionar o que está à esquerda com o que está à direita, não importando quantos elementos há entre ambos.

![[R1.svg]]

Por exemplo, considere a cadeia de $R_1$ dada por $d\ R_1\ b\ R_1\ a\ R_1\ g$. Temos as relações:

- $d\ R_1\ b$;
- $d\ R_1\ g$;
- $b\ R_1\ g$;
- $b\ R_1\ a$;
- E assim por diante...

### Definição Formal

Seja $R \subseteq A \times A$ uma relação de ordem parcial.

Um subconjunto $B \subseteq A$ é chamado de cadeia se, e somente se, quaisquer dois elementos de $B$ são comparáveis, ou seja:

$$
(\forall a, b \in B)[(a, b) \in R \lor (b, a) \in R]
$$

**Exemplo:**

Considere o conjunto $P = \mathcal{P}(\{1,2,3\})$, que contém todos os subconjuntos de $\{1,2,3\}$, ordenado pela relação de inclusão de conjuntos $\subseteq$.

O subconjunto $C = \{\emptyset,\{1\},\{1,2\},\{1,2,3\}\}$ é uma cadeia, pois todos os seus elementos estão contidos uns nos outros formando uma linha direta: $\emptyset \subseteq \{1\} \subseteq \{1,2\} \subseteq \{1,2,3\}$.

## Ordenação Topológica

Seja $(A, \preceq)$ um poset, com $A \neq \emptyset$ e finito.

Para construir uma ordenação topológica, selecione um elemento minimal de $A$ e "remova" ele do diagrama. Agora temos um novo diagrama com novos elementos minimais. Retire mais mais um minimal. O processo deve ser repetido até o diagrama ficar vazio. A ordenação topológica é feita iniciando no primeiro elemento removido e finalizando no último.

> Veja o exemplo [[Discrete Mathematics with Applications, 5th Edition by Susanna S. Epp (2020).pdf#page=579&selection=195,0,197,6|8.5.11]].

# Reticulados (Lattices)

## Definição

Um reticulado é uma estrutura em que quaisquer dois elementos possuem *Inf* e *Sup*.

## Ínfimos e Supremos em Reticulados

Propriedades de $x \land y$ e $x \lor y$:

- $x \leq x \lor y$ e $y \leq x \lor y$ ($x \lor y$ é um limitante superior de $x$ e $y$);
- Se $x \leq z$ e $y \leq z$, então $x \lor y \leq z$ ($x \lor y$ é o menor limitante superior de $x$ e $y$);
- $x \land y \leq x$ e $x \land y \leq y$ ($x \land y$ é um limitante inferior de $x$ e $y$);
- Se $z \leq x$ e $z \leq y$, então $z \leq x \land y$ ($x \land y$ é o maior limitante inferior de $x$ e $y$).

## Propriedades

Seja $L$ um reticulado. Para todo $a, b, c \in L$, valem as seguintes propriedades.

### Teorema 1

$$
\displaylines{
a \lor b = b \iff a \leq b \\
a \land b = a \iff a \leq b
}
$$

$$
a \land b = a \iff a \lor b = b
$$

### Teorema 2

#### Idempotência

$$
\displaylines{
a \lor a = a \\
a \land a = a
}
$$

#### Comutatividade

$$
\displaylines{
a \lor b = b \lor a \\
a \land b = b \land a
}
$$

#### Associatividade

$$
\displaylines{
a \lor (b \lor c) = (a \lor b) \lor c \\
a \land (b \land c) = (a \land b) \land c
}
$$

#### Absorção

$$
\displaylines{
a \lor (a \land b) = a \\
a \land (a \lor b) = a
}
$$

### Teorema 3

$$
\displaylines{
a \leq b \implies a \lor c \leq b \lor c \\
a \leq b \implies a \land c \leq b \land c
}
$$

$$
\displaylines{
a \leq c \quad \text{e} \quad b \leq c \iff a \lor b \leq c \\
c \leq a \quad \text{e} \quad c \leq b \iff c \leq a \land b
}
$$

$$
\displaylines{
a \leq b \quad \text{e} \quad c \leq d \implies a \lor c \leq b \lor d \\
a \leq b \quad \text{e} \quad c \leq d \implies a \land c \leq b \land d
}
$$

## Tipos Especiais

### Reticulado Limitado

Um reticulado é limitado se, e somente se, existe um maior e um menor elemento.

### Reticulado Distributivo

Um reticulado é distributivo se, e somente se, para todo $x, y, z \in L$, temos:

- $x \land (y \lor z) = (x \land y) \lor (x \land z)$; e
- $x \lor (y \land z) = (x \lor y) \land (x \lor z)$.

### Reticulado Complementar

Para todo $a, a' \in A$, $a'$ é o complementar de $a$ (e vice-versa) se, e somente se:

$$
a \land a' = 0 \quad \text{e} \quad a \lor a' = 1
$$

> Note que $0' = 1$ e $1' = 0$.

# Exercícios

## Ex. 1

Apresente duas cadeias e duas ordenações topológicas para as seguintes relações.

> [!example] Exercício (a)
> $A = \{ 2, 3, 4, 6, 18, 24 \}$ e $R = \{ (a, b) \mid a \text{ divide } b \}$.

...

> [!example] Exercício (b)
> $(P(\{a, b, c\}), \subseteq)$

...

## Ex. 2

Caso as relações a seguir sejam de ordem parcial, faça o diagrama de Hasse, ache os extremos, apresente uma cadeia e uma ordem topológica.

> [!example] Exercício (a)
> $A = \mathbb{Z}$. $m\ R\ n$ se, e somente se, todo fator primo de $m$ é fator primo de $n$.

...

> [!example] Exercício (b.1)
> $A = \mathbb{Z}$. $m\ R\ n$ se, e somente se, $m + n$ é par.

...

> [!example] Exercício (b.2)
> Faça para o subconjunto $\{ 1, 2, 3, \ldots, 10\}$.

...

> [!example] Exercício (c)
> $S = \{0, 1\}$. $(S \times S, R)$ tal que $(a, b)\ R\ (c, d)$ se, e somente se:
> - $a < c$; ou
> - $a = c$ e $b \leq d$.

...

> [!example] Exercício (d)
> $A = \{ 2^0, 2^1, 2^2, 2^3, \ldots \}$ e $R = \{(a, b) \mid a \text{ divide } b\}$.

...
