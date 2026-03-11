# Teoria dos Conjuntos

Um conjunto é uma coleção de elementos que a ordem não importa e não há elementos repetidos.

**Forma extensional:**

$$
B = \{\text{carrinho}, \text{bola}, \text{boneco}, \ldots\}
$$

**Forma intensional:**

$$
B = \{x \mid  x \text{ é brinquedo}\}
$$

# Pertinência

> **Símbolo:** $\in$

É a relação entre elemento e conjunto.

$$
\displaylines{
\text{bola} \in B \\
i \in V \\
\{1, 2\} \in C \\
t \notin V \\
1 \notin C
}
$$

# Subconjunto

> **Símbolos:** $\subset$ e $\subseteq$

$$
\displaylines{
\{\text{bola}\} \subseteq B \\
\{a, e\} \subseteq V \\
\{2\} \nsubseteq B
}
$$

> [!important] Subconjunto Próprio
> $A$ é um subconjunto próprio de $B$ (representado por $A \subset B$) se, e somente se, $A \subseteq B$ e $A \neq B$.

# Casos Particulares

- Conjunto vazio: $\{\}$ ou $\emptyset$
- Conjunto unitário: $\{\emptyset\}$, $\{1\}$, ...
- Conjunto universo: $u$

# Cardinalidade

A cardinalidade de um conjunto é a quantidade de elementos que o conjunto possui. É representado por $|C|$, onde $C$ é um conjunto.

$$
\displaylines{
|V| = 5 \\
|\{\emptyset\}| = 1 \\
|\emptyset| = 0
}
$$

# Conjunto das Partes

É o conjunto formado por todos os subconjuntos possíveis de um outro conjunto.

$$
P(A) = \{X \mid X \subseteq A\}
$$

A cardinalidade do conjunto das partes é dada por:

$$
|P(A)| = 2^{|A|}
$$

# Produto Cartesiano

$$
A \times B = \{ (a, b) \mid a \in A \land b \in B \}
$$

> Note que $A \times B \neq B \times A$.

Além disso, temos:

- $A \times \emptyset = \emptyset$
- $|A \times B| = |A| \times |B|$

# Operações

## União

$$
A \cup B = \{ x \mid x \in A \lor x \in B \}
$$

$$
x \in A \cup B \iff x \in A \lor x \in B
$$

## Interseção

$$
A \cap B = \{ x \mid x \in A \land x \in B \}
$$

$$
x \in A \cap B \iff x \in A \land x \in B
$$

# Diferença

$$
A \setminus B = \{ x \mid x \in A \land x \notin B \}
$$

$$
x \in A \setminus B \iff x \in A \land x \notin B
$$

# Complemento

> É em relação a um conjunto (por padrão, é o universo $u$).

$$
\overline{A} = A^C = \{ x \mid x \notin A \} = u \setminus A
$$

$$
x \in \overline{A} \iff x \notin A
$$

# Exercícios

> Sejam $A$, $B$, $C$ e $D$ conjuntos quaisquer. Demonstre ou refute as proposições abaixo.

## Ex. 1

> [!example] Proposição
> $\emptyset \subseteq A$

Suponha, por contradição, que $\emptyset \nsubseteq A$. Ou seja, existe $x$ tal que $x \in \emptyset$ e $x \notin A$. Isso é um absurdo, pois $\emptyset$ não possui nenhum elemento.

Logo $\emptyset \subseteq A$. $\blacksquare$

## Ex. 2

> [!example] Proposição
> $A \subseteq A$

Seja $x \in A$. Logo $x \in A$. $\blacksquare$

## Ex. 3

> [!example] Proposição
> $A \subseteq A \cup B$

Seja $x \in A$.

Pela definição de união, $x \in A$ ou $x \in B$.

Como $x \in A$, logo $A \subseteq A \cup B$. $\blacksquare$

## Ex. 4

> [!example] Proposição
> $A \cup u = u$

Seja $x \in A \cup u$. Pela definição de união, $x \in A$ ou $x \in u$.

Vamos separar a demonstração em duas partes:

**Parte $A \cup u \subseteq u$:**

Se $x \in A$, como $u$ é o universo, então $x \in u$.
Se $x \in u$, então já está em $u$.

**Parte $u \subseteq A \cup u$:**

Seja $x \in u$. Então $x \in A \cup u$, pois $x \in u$.

Pelas duas partes, temos $A \cup u = u$. $\blacksquare$

## Ex. 5

> [!example] Proposição
> $A \cap u = A$

Vamos separar em duas partes:

**Parte $A \cap u \subseteq A$:**

Se $x \in A \cap u$, então $x \in A$ e $x \in u$. Logo $x \in A$.

**Parte $A \subseteq A \cap u$:**

Se $x \in A$, então como $u$ é o universo, $x \in u$. Logo $x \in A \cap u$.

Pelas duas partes, $A \cap u = A$. $\blacksquare$

## Ex. 6

> [!example] Proposição
> $A \cup \emptyset = A$

**Parte $A \cup \emptyset \subseteq A$:**

Se $x \in A \cup \emptyset$, por definição, $x \in A$ ou $x \in \emptyset$.

Como $x \in \emptyset$ é impossível, logo $x \in A$.

**Parte $A \subseteq A \cup \emptyset$:**

Se $x \in A$, então, por definição, $x \in A \cup \emptyset$. 

Pelas duas partes, $A \cup \emptyset = A$. $\blacksquare$

## Ex. 7

> [!example] Proposição
> $A \cap \emptyset = \emptyset$

Suponha, por contradição, que $A \cap \emptyset \neq \emptyset$.

Então existe $x \in A \cap \emptyset$. Logo, por definição, $x \in A$ e $x \in \emptyset$. Absurdo, pois $\emptyset$ não tem nenhum elemento.

Logo $A \cap \emptyset = \emptyset$. $\blacksquare$

## Ex. 8

> [!example] Proposição
> $(A \cup B) \cup C = A \cup (B \cup C)$

Calculamos:

$$
\begin{align}
(A \cup B) \cup C &= \{ x \mid x \in A \cup B \lor x \in C \} \\
                  &= \{ x \mid (x \in A \lor x \in B) \lor x \in C \} \\
                  &= \{ x \mid x \in A \lor (x \in B \lor x \in C) \} \\
                  &= \{ x \mid x \in A \lor x \in B \cup C \} \\
                  &= A \cup (B \cup C)
\end{align}
$$

Logo a união é associativa. $\blacksquare$

## Ex. 9

> [!example] Proposição
> $A \cap (B \cup C) = (A \cap B) \cup (A \cap C)$

Calculamos:

$$
\begin{align}
A \cap (B \cup C) &= \{ x \mid x \in A \land x \in B \cup C \} \\
                  &= \{ x \mid x \in A \land (x \in B \lor x \in C) \} \\
                  &= \{ x \mid (x \in A \land x \in B) \lor (x \in A \land x \in C) \} \\
                  &= \{ x \mid (x \in A \cap B) \lor (x \in A \cap C) \} \\
                  &= (A \cap B) \cup (A \cap C)
\end{align}
$$

Logo a interseção distribui sobre a união. $\blacksquare$

## Ex. 10

> [!example] Proposição
> $A \cap B = A \cup B$

Vamos apresentar um contra-exemplo.

Tome $A = \{ 1 \}$ e $B = \{ 2 \}$. Veja que $A \cap B = \emptyset$ e $A \cup B = \{ 1, 2 \}$.

Como $A \cap B \neq A \cup B$, logo a afirmação é falsa. $\blacksquare$

## Ex. 11

> [!example] Proposição
> $A \subseteq B \implies A \cap B = A$

Suponha que $A \subseteq B$ (H).

Vamos mostrar que $A \cap B \subseteq A$ e $A \subseteq A \cap B$.

**Parte $A \cap B \subseteq A$:**

Seja $x \in A \cap B$. Pela definição de interseção, $x \in A$ e $x \in B$. Logo $x \in A$.

**Parte $A \subseteq A \cap B$:**

Seja $x \in A$. Por (H), temos que $x \in B$. Pela definição de interseção, $x \in A \cap B$.

Logo, pelas duas partes, segue que $A \cap B = A$. $\blacksquare$

## Ex. 12

> [!example] Proposição
> $A \subseteq B \implies A \cup B = B$

Suponha que $A \subseteq B$.

**Parte $A \cup B \subseteq B$:**

Seja $x \in A \cup B$.

Se $x \in A$, como $A \subseteq B$, então $x \in B$.
Se $x \in B$, é imediato.

**Parte $B \subseteq A \cup B$:**

Seja $x \in B$.

Pela definição de união, $x \in A$ ou $x \in B$. Como $x \in B$, logo $x \in A \cup B$.

Pelas duas partes, $A \subseteq B \implies A \cup B = B$. $\blacksquare$

## Ex. 13

> [!example] Proposição
> $A \times (B \cup C) = (A \times B) \cup (A \times C)$

Calculamos:

$$
\begin{align}
A \times (B \cup C) &= \{ (a, x) \mid a \in A \land x \in B \cup C \} \\
                    &= \{ (a, x) \mid a \in A \land (x \in B \lor x \in C) \} \\
                    &= \{ (a, x) \mid (a \in A \land x \in B) \lor (a \in A \land x \in C) \} \\
                    &= (A \times B) \cup (A \times C)
\end{align}
$$

Logo concluímos a demonstração. $\blacksquare$

## Ex. 14

> [!example] Proposição
> $P(A \cup B) = P(A) \cup P(B)$

Vamos refutar essa afirmação apresentando um contra-exemplo.

Tome $A = \{1\}$ e $B = \{2\}$. Veja que $A \cup B = \{1, 2\}$.

No entanto, temos:

$$
P(A) = \{\emptyset, \{1\}\}, \quad P(B) = \{\emptyset, \{2\}\} \quad \text{e} \quad P(A \cup B) = \{\emptyset, \{1\}, \{2\}, \{1, 2\}\}
$$

Agora, perceba que:

$$
P(A) \cup P(B) = \{ \emptyset, \{1\}, \{2\} \}
$$

Logo $P(A \cup B) \neq P(A) \cup P(B)$. $\blacksquare$
