# Teoria dos Conjuntos

Um conjunto é uma coleção de elementos que a ordem não importa e não há elementos repetidos.

**Forma extensional:**

$$
B = \{\text{carrinho}, \text{bola}, \text{boneco}, \ldots\}
$$

**Foram intencional:**

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

A cardinalidade de um conjunto é a quantidade de elementos que o conjunto possui.

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

## Ex. 1

Sejam $A$, $B$, $C$ e $D$ conjuntos quaisquer. Demonstre ou refute:

**1)** $\emptyset \subseteq A$

Como o conjunto vazio é subconjunto de todo conjunto (exceto ele mesmo), então $\emptyset \subseteq A$.

**2)** $A \subseteq A$

Pela reflexividade, é imediato que $A \subseteq A$.

**3)** $A \subseteq A \cup B$

Pela definição de união, $x \in A \cup B$ se, e somente se, $x \in A$ ou $x \in B$. Como todos os elementos de $A$ pertencem a $A \cup B$, logo $A \subseteq A \cup B$.

**4)** $A \cup u = u$

**5)** $A \cap u = A$

**6)** $A \cup \emptyset = A$

**7)** $A \cap \emptyset = \emptyset$

**8)** $(A \cup B) \cup C = A \cup (B \cup C)$

**9)** $A \cap (B \cup C) = (A \cap B) \cup (A \cap C)$

**10)** $A \cap B = A \cup B$

**11)** $A \subseteq B \implies A \cap B = A$

**12)** $A \subseteq B \implies A \cup B = B$

**13)** $A \times (B \cup C) = (A \times B) \cup (A \times C)$

**14)** $P(A \cup B) = P(A) \cup P(B)$
