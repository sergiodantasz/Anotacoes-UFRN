# Exercícios

> Demonstre ou refute as proposições abaixo.

## Ex. 1

> [!example] Proposição
> $\overline{A} \cup \overline{B} = \overline{A \cap B}$

Calculamos:

$$
\begin{align}
\overline{A} \cup \overline{B}
                  &= \{ x \mid x \in \overline{A} \cup \overline{B} \} \\
                  &= \{ x \mid x \in \overline{A} \lor x \in \overline{B} \} \\
                  &= \{ x \mid x \notin A \lor x \notin B \} \\
                  &= \{ x \mid \lnot(x \in A \land x \in B) \} \\
                  &= \{ x \mid \lnot(x \in A \cap B) \} \\
                  &= \{ x \mid x \notin A \cap B \} \\
                  &= \{ x \mid x \in \overline{A \cap B} \} \\
                  &= \overline{A \cap B}
\end{align}
$$

Portanto $\overline{A} \cup \overline{B} = \overline{A \cap B}$. $\blacksquare$

## Ex. 2

> [!example] Proposição
> $\overline{A} \cap \overline{B} = \overline{A \cap B}$

Vamos refutar essa afirmação por meio de um contra-exemplo.

Tome $A = \{ 1 \}$, $B = \{ 2 \}$ e $u = \{ 1, 2 \}$. Note que $\overline{A} = \{ 2 \}$ e $\overline{B} = \{ 1 \}$.

Agora veja que:

$$
\displaylines{
\overline{A} \cap \overline{B} = \{ 2 \} \cap \{ 1 \} = \emptyset \\
\text{e} \\
\overline{A \cap B} = \overline{\emptyset} = u
}
$$

Como $\overline{A} \cap \overline{B} \neq \overline{A \cap B}$, logo a afirmação é falsa. $\blacksquare$

## Ex. 3

> [!example] Proposição
> $\overline{\overline{A}} = A$

Calculamos:

$$
\begin{align}
\overline{\overline{A}} &= \overline{\{x \mid x \in \overline{A} \}} \\
                        &= \{ x \mid x \notin \overline{A} \} \\
                        &= \{ x \mid x \in A \} \\
                        &= A
\end{align}
$$

Portanto $\overline{\overline{A}} = A$. $\blacksquare$

## Ex. 4

> [!example] Proposição
> $A \cup \overline{A} = u$

Vou demonstrar em duas partes:

**Parte $A \cup \overline{A} \subseteq u$:**

Seja $x \in A \cup \overline{A}$.

Por definição, $x \in A$ ou $x \in \overline{A} \iff x \notin A$.

Se $x \in A$, como $x \in u$ é dado, então $x \in u$.
Se $x \notin A$, como $x \in u$ também é dado, logo $x \in u$.

**Parte $u \subseteq A \cup \overline{A}$:**

Seja $x \in u$.

Se $x \in A$, pela definição de união, $x \in A \cup \overline{A}$.
Se $x \notin A$, então, pela definição de complemento, $x \in \overline{A}$. Logo $x \in A \cup \overline{A}$.

Logo $A \cup \overline{A} = u$.

## Ex. 5

> [!example] Proposição
> $A \cap \overline{A} = \emptyset$

...

## Ex. 6

> [!example] Proposição
> $A \setminus B \subseteq A$

...

## Ex. 7

> [!example] Proposição
> $A \subseteq A \setminus B$

...

## Ex. 8

> [!example] Proposição
> $A \cap (B \setminus A) = \emptyset$

...

## Ex. 9

> [!example] Proposição
> $A \cup (B \setminus A) = A \cup B$

...

## Ex. 10

> [!example] Proposição
> $A \setminus B = \overline{B \setminus A}$

...
