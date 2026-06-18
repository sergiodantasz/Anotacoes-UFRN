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

# Diagrama de Hasse

## Definição

O diagrama de Hasse é uma forma gráfica de representar um conjunto finito parcialmente ordenado (*poset*).

Seja um *poset* definido por $(A, \preceq)$, onde a relação é reflexiva, antissimétrica e transitiva.

O diagrama de Hasse simplifica as conexões entre os elementos do conjunto eliminando os grafos da reflexividade e da transitividade, além de atribuir o sentido de baixo para cima nas ligações.

Dizemos que $y$ cobre $x$ se $x \prec y$ (isto é, $x \preceq y$ e $x \neq y$) e não existe $z \in A$ tal que $x \prec z \prec y$.

## Cadeia

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

> Veja o exemplo [[Discrete Mathematics with Applications, 5th Edition by Susanna S. Epp (2020).pdf#page=579&selection=195,0,197,6|8.5.11]] do livro 6.

# Reticulados (Lattices)

## Definição

Um reticulado é uma estrutura em que quaisquer dois elementos possuem *Inf* e *Sup*.

## Reticulados Isomórficos

Dois reticulados são isomórficos quando ambos têm a mesma estrutura algébrica e de ordem, mesmo que seus elementos sejam diferentes.

Sejam $(L, R_L)$ e $(M, R_M)$ dois reticulados. Eles são isomórficos se existe uma função bijetiva $f : L \to M$ (dita isomorfismo de reticulados) tal que, para quaisquer $a, b \in L$, temos:

$$
f(a \land_{L} b) = f(a) \land_{M} f(b) \quad \text{e} \quad f(a \lor_{L} b) = f(a) \lor_{M} f(b)
$$

Ou, equivalentemente:

$$
a\ R_L\ b \iff f(a)\ R_M\ f(b)
$$

## Ínfimo e Supremo

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

Um reticulado é limitado se, e somente se, existe um maior e um menor elemento globais, denotados por $1$ e $0$, respectivamente.

### Reticulado Distributivo

Um reticulado é distributivo se, e somente se, para todo $a, b, c \in L$, temos:

$$
a \land (b \lor c) = (a \land b) \lor (a \land c) \quad \text{e} \quad a \lor (b \land c) = (a \lor b) \land (a \lor c)
$$

### Reticulado Complementado

Um reticulado é complementado se, e somente se, ele é limitado e para todo $a, a' \in A$, $a'$ é o complementar de $a$ (e vice-versa) se, e somente se:

$$
a \land a' = 0 \quad \text{e} \quad a \lor a' = 1
$$

> Note que $0' = 1$ e $1' = 0$.

## Top e Bottom

Em um reticulado limitado, 1 é o maior elemento global (top) e 0 é o menor elemento global (bottom). Em outras palavras, eles denotam o *Sup* e o *Inf* do reticulado como um todo e são únicos.

### Propriedades

Para todo $x \in L$, valem:

$$
0 \leq x \leq 1
$$

$$
\displaylines{
x \lor 0 = x \\
x \land 0 = 0
}
$$

$$
\displaylines{
x \lor 1 = 1 \\
x \land 1 = x
}
$$

# Álgebra Booleana

## Definição

Um *poset* $(A, R)$ é uma álgebra booleana se, e somente se, ele é um reticulado limitado, distributivo e complementado.

> Como o complementado já é limitado por definição, podemos dizer que ele é simplesmente distributivo e complementado.

## Funções Booleanas

Uma função booleana é uma função cujas variáveis e resultados pertencem ao conjunto $\{0,1\}$. Essas funções podem ser representadas por expressões booleanas utilizando operações como AND ($\land$), OR ($\lor$) e NOT ($'$ ou $\lnot$).

As funções booleanas podem ser descritas de diferentes formas equivalentes, incluindo expressões algébricas, tabelas-verdade, mapas de Karnaugh e circuitos lógicos.

![[Funções Booleanas.png|556]]

**Exemplo:**

A função $f(x,y) = x \land y$ possui a seguinte tabela-verdade:

| $x$ | $y$ | $f(x,y)$ |
| :-: | :-: | :------: |
|  0  |  0  |    0     |
|  0  |  1  |    0     |
|  1  |  0  |    0     |
|  1  |  1  |    1     |

## Mapa de Karnaugh

Os mapas de Karnaugh fornecem uma representação gráfica da tabela-verdade, permitindo simplificar expressões booleanas e obter implementações mais eficientes.

# Exercícios

## Livro 5

### Teorema 1

Sejam $L$ um reticulado e $a, b \in L$.

> [!example] Proposição (a)
> $a \lor b = b \iff a \leq b$

**Parte ($\implies$):**

Suponha que $a \lor b = b$. Como $a \leq a \lor b = b$, logo $a \leq b$.

**Parte ($\impliedby$):**

Suponha que $a \leq b$. Disso e de $b \leq b$, segue que $b$ é um limitante superior de $a$ e de $b$. Pela definição de menor limitante superior, temos $a \lor b \leq b$. Como $a \lor b$ é um limitante superior, logo $b \leq a \lor b$ e, consequentemente, $a \lor b = b$. $\blacksquare$

> [!example] Proposição (b)
> $a \land b = a \iff a \leq b$

**Parte ($\implies$):**

Suponha que $a \land b = a$. Como $a = a \land b \leq b$, logo $a \leq b$.

**Parte ($\impliedby$):**

Suponha que $a \leq b$. Segue que, disso e de $a \leq a$, $a$ é um limitante inferior de $a$ e de $b$. Pela definição de maior limitante inferior, então $a \leq a \land b$. Isto é, $a \land b$ é um limitante inferior. Assim, $a \land b \leq a$ e, por consequência, $a \land b = a$. $\blacksquare$

> [!example] Proposição (c)
> $a \land b = a \iff a \lor b = b$

**Parte ($\implies$):**

Suponha que $a \land b = a$. Pela proposição (b), temos $a \leq b$. Pela proposição (a), obtemos $a \lor b = b$.

**Parte ($\impliedby$):**

Suponha que $a \lor b = b$. Pela proposição (a), segue que $a \leq b$. Pela proposição (b), temos $a \land b = a$. $\blacksquare$
