# Ordem Parcial

Sejam $R \subseteq A \times A$ uma relação de ordem parcial, $B \subseteq A$, $a \in A$ e $b \in B$.

## Mínimo

$b$ é o menor elemento (ou o elemento mínimo) de $B$ se, e somente se:

$$
\forall x \in B, b\ R\ x
$$

## Minimal

$b$ é o elemento minimal de $B$ se, e somente se:

$$
\forall x \in B, x\ R\ b \implies x = b
$$

> Nenhum elemento se relaciona com $b$ além dele mesmo.

## Máximo

$b$ é o maior elemento (ou o elemento máximo) de $B$ se, e somente se:

$$
\forall x \in B, x\ R\ b
$$

## Maximal

$b$ é o elemento maximal de $B$ se, e somente se:

$$
\forall x \in B, b\ R\ x \implies x = b
$$

## Limitante Inferior

$a$ é limitante inferior de $B$ se, e somente se:

$$
\forall x \in B, a\ R\ x
$$

## Maior Limitante Inferior (Ínfimo)

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

## Limitante Superior

$a$ é limitante superior de $B$ se, e somente se:

$$
\forall x \in B, x\ R\ a
$$

## Menor Limitante Superior (Supremo)

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

## Complementar

Dados dois elementos $a, a' \in A$, $a'$ é o complementar de $a$ (e vice-versa) se, e somente se:

$$
a \land a' = 0 \quad \text{e} \quad a \lor a' = 1
$$
