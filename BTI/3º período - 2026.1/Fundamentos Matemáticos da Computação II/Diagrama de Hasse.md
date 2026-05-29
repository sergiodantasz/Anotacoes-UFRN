# Definição

...

# Cadeia

Com quaisquer dois elementos ordenados corretamente numa cadeia de relações do diagrama, conseguimos relacionar o que está à esquerda com o que está à direita, não importando quantos elementos há entre ambos.

[exemplo da foto]

Por exemplo, considere a cadeia de $R_1$ dada por $d\ R_1\ b\ R_1\ a\ R_1\ g$. Temos as relações:

- $d\ R_1\ b$;
- $d\ R_1\ g$;
- $b\ R_1\ g$;
- $b\ R_1\ a$;
- E assim por diante...

## Formalização

Seja $R \subseteq A \times A$ uma poset.

Um subconjunto $B \subseteq A$ é chamado de cadeia se, e somente se, quaisquer dois elementos de $B$ são comparáveis.

# Ordenação Topológica

[foto]

# Reticulado (Lattice)

Um reticulado é uma estrutura em que quaisquer dois elementos possuem Inf e Sup.

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
