# Função Totiente de Euler

Seja $n : Int$ tal que $n > 0$.

$$
\phi(n) ≝ |\{i \in \{1,2,3\ldots,n\} \mid mdc(i,n) = 1\}|
$$

>Os "$||$" de fora significam "cardinalidade do conjunto". O conjunto de fora significa "conjunto de todos os coprimos de $n$".

*Ex.:* O totiente de $n = 14$ é 6 (6 primos no conjunto).

> [!quote] Números coprimos
> Dois números são **coprimos** se, e somente se, o único divisor comum positivo entre eles é 1.

## Propriedades

**Propriedade 1:** Se $p$ é primo, então $\phi(p) = p - 1$.

Dem.:

Seja $p$ primo. Então $\forall i$ tal que $1 \leq i < p$ e $mdc(i,p) = 1$, pois $p$ é primo.
Se $i = p$ e $mdc(i,p) = 0$, então $i = p$ não pertence ao conjunto de coprimos de $p$.
Logo $\phi(p) = p - 1$.

---

**Lema:** Quantos múltiplos de $a$ existem em $\{1,2,3,\ldots,a^n\}$?

Múltiplos de $a$: $\{a,2a,3a,\ldots,Ka = a^n\}$
$Ka = a^n \implies K = a^{n - 1}$
$K \in \mathbb{Z}$

---

**Propriedade 2:** $p$ é primo $\implies$ $\phi(p^a) = p^a - p^{a - 1}$, em que $a : Int$ e $a > 0$.

Dem.:

$\phi(p^a) =$ (todos os números entre $1$ e $p^a$) - (todos os múltiplos de $p$ entre p e $p^a$) [uso do lema]
$\phi(p^a) = p^a - p^{a - 1} = p^{a - 1}(p - 1)$

Ex.:
Com p = 5 e a = 10
x, 5, x, 10, x, 15, x, 20, x, ..., $5^{10}$

Ex.:
$p$ é primo e $k \in \mathbb{Z}$
Calcular somatório de $\phi(p^i)$ com $i = 0$ até $k$.

$$
\displaylines{
\begin{align*}
\sum_{i=0}^k{\phi(p^i)} &= \phi(p^0) + \sum_{i=1}^k{\phi(p^i)} \\
&= \phi(1) + \sum_{i=1}^k{p^i - p^{i - 1}} \\
&= 1 + \sum_{i=1}^k{p^i} - \sum_{i=1}^k{p^{i - 1}} \\
&= 1 + \sum_{i=1}^k{p^i} - \sum_{i=0}^{k - 1}{p^i} \qquad (IndexShift) \\
&= 1 + p^k + \sum_{i=1}^{k-1}{p^i} - p^0 - \sum_{i=1}^{k - 1}{p^i} \\
&= 1 + p^k - p^0 \\
&= p^k
\end{align*}
}
$$

**Teorema:** Se $mdc(a,b) = 1$, então $\phi(a \cdot b) = \phi(a) \cdot \phi(b)$.
[SEM DEMO]

**Teorema de Euler:** Sejam $a, m \in \mathbb{Z}$ com $mdc(a,m) = 1$, então $a^{\phi(m)} \equiv 1 \pmod m$.

Dem.:

Seja o conjunto $R = \{r_1,r_2,r_3,\ldots,r_{\phi(m)}\}$. [conjunto dos coprimos de m]
Como $mdc(a,m) = 1$, então os elementos do conjunto $S = \{ar_1,ar_2,ar_3,\ldots,ar_{\phi(m)}\}$ são coprimos com m.

OBS.:
Se $ar_i \equiv ar_j \pmod m$, então:

$$
\displaylines{
\begin{align*}
a(r_i - r_j) \equiv 0 \pmod m
&\iff r_i - r_j \equiv 0 \pmod m \qquad (pois\ existe\ a^{-1}) \\
&\iff r_i \equiv r_j \pmod m \qquad (ABSURDO)
\end{align*}
}
$$

Então os elementos de $S$ são distintos de $mod\ m$.

Como $|R| = |S|$, então os conjuntos $R$ e $S$ possuem os mesmos elementos $mod\ m$.
Multiplicando os termos dos conjuntos:
$$
\displaylines{
\begin{align*}
& (ar_1)(ar_2)\ldots(ar_{\phi(m)}) \equiv r_1r_2\ldots r_{\phi(m)} \pmod m \\
\iff& a^{\phi(m)}(r_1r_2\ldots r_{phi(m)}) \equiv r_1r_2\ldots r_{\phi(m)} \pmod m \\
\iff& a^{\phi(m)} \equiv 1 \pmod m
\end{align*}
}
$$

trocar n por m

---
PTF: Caso específico m = p primo

$$
\displaylines{
\begin{align*}
& a^{\phi(p)} \equiv 1 \pmod m \\
\iff& a^{p - 1} \equiv 1 \pmod m \\
\iff& a^p \equiv a \pmod m
\end{align*}
}
$$
