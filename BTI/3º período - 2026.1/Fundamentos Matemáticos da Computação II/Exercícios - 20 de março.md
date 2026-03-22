# Questões

## Questão 1

Dada uma função $f : \mathbb{U} \to \mathbb{U}$, subconjuntos $C, D \subseteq Dom(f)$, demonstre ou refute:

**a)** $f(D) \subseteq f(C) \implies D \subseteq C$

Vamos refutar essa afirmação.

Tome $f(x) = 0$, $C = \{ 1 \}$ e $D = \{ 2 \}$.

Note que $f(C) = \{ 0 \}$ e $f(D) = \{ 0 \}$. Logo $f(D) \subseteq f(C)$, mas $D \nsubseteq C$.

Sendo assim, a afirmação é falsa.

**b)** $D \subseteq C \implies f(D) \subseteq f(C)$

Suponha que $D \subseteq C$.

Seja $y \in f(D)$.

Pela definição de imagem, existe $x \in D$ tal que $f(x) = y$.

Como $x \in D$ e $D \subseteq C$, logo, pela definição de subconjunto, $x \in C$.

Como $x \in C$ e $f(x) = y$, então $y \in f(C)$.

Portanto, $f(D) \subseteq f(C)$.

## Questão 2

Sejam $A$, $B$, $C$ e $D$ conjuntos quaisquer.

Demonstre ou refute: $(A \cup C) \times (B \cup D) \subseteq (A \times B)\cup (C \times D)$.

**Refutação:**

Vamos refutar essa afirmação.

Tome $A = \{ 1 \}$, $B = \emptyset$, $C = \emptyset$ e $D = \{ 2 \}$.

Perceba que $A \cup C = \{ 1 \}$ e $B \cup D = \{ 2 \}$. Disso, temos:

$$
(A \cup C) \times (B \cup D) = \{ (1, 2) \}
$$

Agora, note que $A \times B = \emptyset$ e $C \times D = \emptyset$. Disso, segue que:

$$
(A \times B) \cup (C \times D) = \emptyset
$$

Como $\{ (1, 2) \} \nsubseteq \emptyset$, logo a afirmação é falsa.

## Questão 3

