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

Suponha, por contradição, que $u \nsubseteq A \cup \overline{A}$.

Ou seja, existe $x \in u$ tal que $x \notin A \cup \overline{A}$. Logo $x \notin A \iff x \in \overline{A}$ ou $x \notin \overline{A} \iff x \in A$.

Em ambos os casos, isso é um absurdo, pois $x \in u$ e $u \nsubseteq A \cup \overline{A}$. Assim, $u \subseteq A \cup \overline{A}$.

Logo $A \cup \overline{A} = u$. $\blacksquare$

## Ex. 5

> [!example] Proposição
> $A \cap \overline{A} = \emptyset$

Suponha, por contradição, que $A \cap \overline{A} \neq \emptyset$.

Logo existe $x \in A \cap \overline{A}$, isto é, $x \in A$ e $x \notin A$.

Absurdo, pois é impossível um elemento pertencer e não pertencer a um mesmo conjunto simultaneamente.

Portanto $A \cap \overline{A} = \emptyset$. $\blacksquare$

## Ex. 6

> [!example] Proposição
> $A \setminus B \subseteq A$

Seja $x \in A \setminus B$. Pela definição de diferença, $x \in A$ e $x \notin B$. Logo $x \in A$.

Assim, $A \setminus B \subseteq A$. $\blacksquare$

## Ex. 7

> [!example] Proposição
> $A \subseteq A \setminus B$

Refutaremos essa afirmação.

Tome $A = \{ 1, 2 \}$ e $B = \{ 2 \}$. Note que $A \setminus B = \{ 1 \}$.

Como $2 \in A$ e $2 \notin A \setminus B$, logo $A \nsubseteq A \setminus B$. $\blacksquare$

## Ex. 8

> [!example] Proposição
> $A \cap (B \setminus A) = \emptyset$

Suponha, por contradição, que $A \cap (B \setminus A) \neq \emptyset$.

Logo existe $x \in A \cap (B \setminus A)$, ou seja, $x \in A$ e $x \in B \setminus A$. Por definição de diferença, $x \in B$ e $x \notin A$.

Isso é um absurdo, pois não é possível que $x \in A$ e $x \notin A$. Portanto, $A \cap (B \setminus A) = \emptyset$. $\blacksquare$

## Ex. 9

> [!example] Proposição
> $A \cup (B \setminus A) = A \cup B$

Calculamos:

$$
\begin{align}
A \cup (B \setminus A) &= \{ x \mid x \in A \cup (B \setminus A) \} \\
                       &= \{ x \mid x \in A \lor x \in (B \setminus A) \} \\
                       &= \{ x \mid x \in A \lor (x \in B \land x \notin A) \} \\
                       &= \{ x \mid (x \in A \lor x \in B) \land (x \in A \lor x \notin A) \} \\
                       &= \{ x \mid x \in A \cup B \land x \in u \} \\
                       &= \{ x \mid x \in ((A \cup B) \cap u) \} \\
                       &= \{ x \mid x \in A \cup B \} \\
                       &= A \cup B
\end{align}
$$

Logo concluímos a demonstração. $\blacksquare$

## Ex. 10

> [!example] Proposição
> $A \setminus B = \overline{B \setminus A}$

Vamos refutar essa afirmação.

Considere o universo $u = \{ 1, 2\}$. Tome $A = \{ 1, 2 \}$ e $B = \{ 2 \}$.

Note que $A \setminus B = \{ 1 \}$ e $B \setminus A = \emptyset$. Logo $\overline{B \setminus A} = u = \{ 1, 2\}$.

Sendo assim, $A \setminus B \neq \overline{B \setminus A}$. Portanto a afirmação é falsa. $\blacksquare$
